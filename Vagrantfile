# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
    v.memory = 2048
    v.linked_clone = true
  end

# server 1.
  config.vm.define "app1" do |app|
    app.vm.hostname = "app"
    app.vm.network :private_network, ip: "192.168.60.20"
  end 
end
