# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    # Hostname
    config.vm.hostname = "mysql"
    config.disksize.size = "25GB"

    # Box OS
    config.vm.box = "ubuntu/xenial64"

    # Enable ports
    config.vm.network :forwarded_port, guest: 3306, host: 3306, host_ip: "127.0.0.1"

    # Configure VirtualBox
    config.vm.provider "virtualbox" do |machine|
        machine.name = "mysql"
        # machine.memory = 4096
    end

    config.vm.provision :shell, :path => "bootstrap.sh"
end
