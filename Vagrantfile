# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  #Enter the name of the vagrant box here 
  config.vm.box = "zeab/ub-16.04-64x-base"
  #Uncomment to mount another folder besides the defualt vagrant folder
  #config.vm.synced_folder "C:/Some/Host/Folder", "/Some/Location/In/VM"
  config.vm.provider "virtualbox" do |vb|
	vb.gui = false
	vb.customize ["modifyvm", :id, "--memory", 2048]
	vb.customize ["modifyvm", :id, "--cpus", 2]
	#Configures the 2nd network card as bridged
	vb.customize ["modifyvm", :id, "--nic2", "bridged"]
	vb.customize ["modifyvm", :id, "--nictype2", "virtio"]
	#Replace the network card named here with your own local network card
	vb.customize ["modifyvm", :id, "--bridgeadapter2", "Intel(R) Dual Band Wireless-AC 8260"] #Dell Latitude E7470
	#vb.customize ["modifyvm", :id, "--bridgeadapter2", "Intel(R) PRO/1000 GT Desktop Adapter"] #Home Server
	#vb.customize ["modifyvm", :id, "--bridgeadapter2", "eno1"] #Linx Server
	end
end