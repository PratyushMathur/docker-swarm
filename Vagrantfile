BOX_IMAGE="centos/7"

Vagrant.configure("2") do |config|
	config.vm.box=BOX_IMAGE

	config.vm.define "manager" do |node|
		node.vm.hostname='manager'
		node.vm.provision :docker
		node.vm.network :private_network, ip: "192.168.100.10"	
		node.vm.network :forwarded_port, guest: 8080, host: 8080
	end

	config.vm.define "worker1" do |node|
		node.vm.hostname='worker1'
		node.vm.provision :docker
		node.vm.network :private_network, ip: "192.168.100.11"
	end

	config.vm.define "worker2" do |node|
		node.vm.hostname='worker2'
		node.vm.provision :docker
		node.vm.network :private_network, ip: "192.168.100.12"
	end
end
