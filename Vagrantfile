# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  #Enter the name of the vagrant box here 
  config.vm.box = "zeab/ub-16.04-64x-base"
  
  #UNCOMMENT to mount another folder besides the defualt vagrant folder
	#Windows To Linux
  #config.vm.synced_folder "C:/Some/Host/Folder", "/Some/Location/In/VM", type: "nfs"
	#Linux To Linux
  #config.vm.synced_folder "/Some/Host/Folder", "/Some/Location/In/VM"
  
  #UNCOMMENT to explose internal services out through portfowarding
  #config.vm.network :forwarded_port, guest: 8080, host: 8080, id: "ServiceName"
  
  #Virtualbox config
  config.vm.provider "virtualbox" do |vb|
	
	#Start vm with GUI
	vb.gui = false
	
	#SYSTEM SETTINGS
		#Modify Memory
	vb.customize ["modifyvm", :id, "--memory", 2048]
		#Modify CPU's
	vb.customize ["modifyvm", :id, "--cpus", 2]

	#VIRTUALBOX SPECIFIC NETWORK SETTINGS
	
	#UNCOMMENT to turn on 2nd bridged network adapter
		#LARGELY UNESSESSARY IF PORT FORWARDING IS SET UP ABOVE
		#Configures the 2nd network card as bridged
	#vb.customize ["modifyvm", :id, "--nic2", "bridged"]
	#vb.customize ["modifyvm", :id, "--nictype2", "virtio"]
		#Replace the network card named here with your own local network card
	#vb.customize ["modifyvm", :id, "--bridgeadapter2", "Intel(R) Dual Band Wireless-AC 8260"] #Dell Latitude E7470
	#vb.customize ["modifyvm", :id, "--bridgeadapter2", "Intel(R) PRO/1000 GT Desktop Adapter"] #Home Server
	#vb.customize ["modifyvm", :id, "--bridgeadapter2", "eno1"] #Linx Server
	end
end