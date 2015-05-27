# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.ssh.insert_key = false

  config.vm.define "ubuntu" do |m|
    m.vm.box = "ubuntu/trusty64"
    m.vm.hostname = "ubuntu"
  end

  config.vm.define "centos" do |m|
    m.vm.box = "chef/centos-6.5"
    m.vm.hostname = "centos"
    m.vm.provision "ansible" do |ansible|
      ansible.playbook = "deploy.yml"
      ansible.limit = 'all'
    end
  end

end
