# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "puphpet/ubuntu1604-x64"

  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.synced_folder ".", "/home/vagrant",
  	group: "www-data", mount_options: ["dmode=775,fmode=664"]

  config.vm.provider "virtualbox" do |vb|
    vb.name = "chronos"
    vb.memory = "1024"
  end

  # Do provisioning
  config.vm.provision :shell, path: "_provision/vagrant.sh"
end
