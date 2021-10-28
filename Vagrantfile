# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "generic/rocky8"
  config.vm.box_version = "3.4.4"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
    v.memory = 1000
    v.linked_clone = true
  end

  #This will be the node to SSH into for ansible
  config.vm.define "controlnode" do |control|
    control.vm.hostname = "controlnode"
    control.vm.network :private_network, ip: "192.168.60.3"
  end

  #Nodes to run Ansible against

  (1..3).each do |i|
    config.vm.define "node#{i}" do |n|
      n.vm.hostname = "node#{i}"
      n.vm.network :private_network, ip: "192.168.60.#{i + 3}"
    end  
  end
end
