# -*- mode: ruby -*-
# vi: set ft=ruby :

def local_cache(basebox_name)
  cache_dir = Vagrant::Environment.new.home_path.join('cache', basebox_name)
  FileUtils.mkpath cache_dir unless cache_dir.exist?
  cache_dir
end

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "centos6" do |machine|
    machine.vm.box = "box-cutter/centos64"
    machine.vm.hostname = "centos6"
  end

  config.vm.define "centos7" do |machine|
    machine.vm.box = "box-cutter/centos74"
    machine.vm.hostname = "centos7"
  end

  config.vm.define "ubuntu-precise" do |machine|
    machine.vm.box = "ubuntu/precise64"
    machine.vm.synced_folder local_cache(machine.vm.box), "/var/cache/apt/archives"
    machine.vm.hostname = "ubuntu-precise"
  end

  config.vm.define "ubuntu-trusty" do |machine|
    machine.vm.box = "ubuntu/trusty64"
    machine.vm.synced_folder local_cache(machine.vm.box), "/var/cache/apt/archives"
    machine.vm.hostname = "ubuntu-trusty"

    machine.vm.provision "ansible" do |ansible|
      ansible.playbook = "demo.yml"
      ansible.limit = 'all'
    end
  end
end
