# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "movor/torch"
  config.vm.box_version = "0.0.1"
  config.vm.network "private_network", ip: "192.168.11.11"
  config.vm.hostname = "torch"
  config.vm.synced_folder "~/Development/web", "/var/www", :mount_options => ["dmode=777", "fmode=777"]
  config.ssh.insert_key = false
  config.vm.box_check_update = false
  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--cpuexecutioncap", "100"]
    v.memory = 512
    v.cpus = 1
  end
end
