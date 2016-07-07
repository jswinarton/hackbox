# -*- mode: ruby -*-
# vi: ft=ruby:

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "10.0.20.20"

  config.vm.synced_folder "./shared", "/vagrant"

  config.ssh.forward_agent = true

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 1
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/site.yml"
  end
end
