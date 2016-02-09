# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

VAGRANT_COMMAND = ARGV[0]

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
    v.cpus = 2
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  end

  # Original starting point of the base box, and deploy script
  config.vm.box = "bento/centos-6.7"
  config.vm.hostname = "dsra-client"

  #config.vm.provision "ansible" do |ansible|
#      ansible.playbook = "playbook.yml"
#  end

  # To use the same network as the Host OS is
  #config.vm.network "public_network"
end
