# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  #config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = true

  config.vm.network "private_network", ip: "192.168.66.10"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end