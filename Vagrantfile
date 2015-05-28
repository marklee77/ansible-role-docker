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

  config.vm.define "ubuntu-precise" do |m|
    m.vm.box = "ubuntu/precise64"
    m.vm.hostname = "ubuntu-precise"
  end

  config.vm.define "debian-jessie" do |m|
    m.vm.box = "debian/jessie64"
    m.vm.hostname = "debian-jessie"
  end

  config.vm.define "centos-7" do |m|
    m.vm.box = "chef/centos-7.0"
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
