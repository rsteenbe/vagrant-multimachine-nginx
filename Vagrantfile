Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Provision 2 ubuntu/xenial64 boxes with Nginx"

  config.vm.define "server1" do |server1|
    server1.vm.box = "ubuntu/xenial64"
	server1.vm.network 'forwarded_port', guest: 80, host: 80
	server1.vm.network "private_network", ip: "192.168.50.10"
	server1.vm.provider "virtualbox" do |v|
		v.memory = 2048
		v.cpus = 2
	end
	server1.vm.provision "shell", inline: <<-SHELL
		 apt-get update -y
		 apt-get install nginx -y
	SHELL
  end

  config.vm.define "server2" do |server2|
    server2.vm.box = "ubuntu/xenial64"
	server2.vm.network 'forwarded_port', guest: 80, host: 81
	server2.vm.network "private_network", ip: "192.168.50.11"
	server2.vm.provider "virtualbox" do |v|
		v.memory = 2048
		v.cpus = 2
	end
	server2.vm.provision "shell", inline: <<-SHELL
		 apt-get update -y
		 apt-get install nginx -y
	SHELL
  end
end
