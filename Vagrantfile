# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "envoy-centos" do |c|
    c.vm.box = "bento/centos-7.2"
    c.vm.network :private_network, ip: "192.168.32.31"
    c.vm.provision "shell", inline: "sudo systemctl restart network"
    c.vm.box_check_update = false
    c.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
  end

end
