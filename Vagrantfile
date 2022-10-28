Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"

 #config.vm.network "private_network"
  config.vm.network "public_network", ip: "X.X.X.X"
  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.provider "virtualbox" do |vb|
     vb.name = "jenkins"
     vb.cpus = 1
     vb.memory = 6000
  end
  
  config.vm.provision "shell", inline: <<-SHELL
     sudo yum update
     sudo yum install gedit
  SHELL
end
