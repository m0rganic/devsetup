# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu1310-docker-ansible"

  config.vm.network :private_network, ip: "192.168.127.4"
  config.vm.network :forwarded_port, guest: 5000, host: 5000
  config.vm.network :forwarded_port, guest: 22, host: 2258

  # Forward X11
  config.ssh.forward_x11 = true

 config.vm.synced_folder ".", "/vagrant"

end