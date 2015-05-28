# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.ssh.insert_key = false

  config.vm.define "ubuntu-trusty" do |m|
    m.vm.box = "ubuntu/trusty64"
    m.vm.hostname = "ubuntu-trusty"
  end

  config.vm.define "ubuntu-saucy" do |m|
    m.vm.box = "ubuntu/saucy64"
    m.vm.hostname = "ubuntu-saucy"
  end

  config.vm.define "ubuntu-raring" do |m|
    m.vm.box = "ubuntu/raring64"
    m.vm.hostname = "ubuntu-raring"
  end


  config.vm.define "ubuntu-quantal" do |m|
    m.vm.box = "ubuntu/quantal64"
    m.vm.hostname = "ubuntu-quantal"
  end

  config.vm.define "ubuntu-precise" do |m|
    m.vm.box = "ubuntu/precise64"
    m.vm.hostname = "ubuntu-precise"
  end

  config.vm.define "centos-7" do |m|
    m.vm.box = "chef/centos-7"
    m.vm.hostname = "centos-7"
  end

  config.vm.define "centos-6" do |m|
    m.vm.box = "chef/centos-6.5"
    m.vm.hostname = "centos-6"
    m.vm.provision "ansible" do |ansible|
      ansible.playbook = "deploy.yml"
      ansible.limit = 'all'
    end
  end

end
