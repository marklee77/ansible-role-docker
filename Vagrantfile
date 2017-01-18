# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "ubuntu-trusty64" do |m|
    m.vm.box = "ubuntu/trusty64"
    m.vm.provision "ansible" do |ansible|
      ansible.playbook = "site.yml"
      ansible.limit = 'all'
    end
    m.vm.provision "ansible" do |ansible|
      ansible.playbook = "test.yml"
      ansible.limit = 'all'
    end
  end
end
