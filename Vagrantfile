Vagrant.configure("2") do |config|
	config.vm.box = "ubuntu/xenial64"
	config.vm.network "public_network"
	config.vm.hostname = "mysql-server"
	config.vm.provider "virtualbox" do |vb|
	 vb.gui = true
	 vb.cpus =  1
	 vb.memory = "1024"
	end
	  config.vm.provision "shell", inline: <<-SHELL
		 apt update && apt upgrade -y 
		 apt install mysql-server -y
	   SHELL
  end