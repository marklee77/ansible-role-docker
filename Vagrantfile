# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "centos6" do |machine|
    machine.vm.box = "centos64-6.4"
    machine.vm.box_url = "http://stillwell.me/files/centos64-6.4.box"
    machine.vm.hostname = "centos6"
    machine.vm.provision "ansible" do |ansible|
      ansible.playbook = "provisioning/deploy.yml"
    end
  end

  config.vm.define "centos7" do |machine|
    machine.vm.box = "box-cutter/centos70"
    machine.vm.hostname = "centos7"
    machine.vm.provision "ansible" do |ansible|
      ansible.playbook = "provisioning/deploy.yml"
    end
  end

  config.vm.define "ubuntu-precise" do |machine|
    machine.vm.box = "ubuntu/precise64"
    machine.vm.hostname = "ubuntu-precise"
    machine.vm.provision "ansible" do |ansible|
      ansible.playbook = "provisioning/deploy.yml"
    end
  end

  config.vm.define "ubuntu-trusty" do |machine|
    machine.vm.box = "ubuntu/trusty64"
    machine.vm.hostname = "ubuntu-trusty"
    machine.vm.provision "ansible" do |ansible|
      ansible.playbook = "provisioning/deploy.yml"
    end
  end
end
