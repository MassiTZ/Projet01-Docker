# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/jammy64"
  config.vm.hostname = "hostmassi" 
  config.vm.network "private_network", ip: "192.168.56.2"
  config.vm.provision "file", source: "docker-compose.yml", destination: "$HOME/"
  config.vm.provision "file", source: "db_password.txt", destination: "$HOME/"
  config.vm.provision "file", source: "db_root_password.txt", destination: "$HOME/"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
    vb.cpus = 2
    vb.name = "Projet01-Docker"
  end
  config.vm.provision "shell", path: "install-docker.sh"
end 