Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal164"
  #network
  
  #config.vm.network "forwarded_port", guest: 80, host: 8080
  
  #config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

   config.vm.network "private_network", ip: "192.168.33.111"

  # config.vm.network "public_network"
#folders
  
  #config.vm.synced_folder "../data", "/vagrant_data"

  # provider

   config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
    vb.cpus = "4"
   end
  # provisnor
   
   config.vm.provision "shell", inline: <<-SHELL
   apt-get update
     apt-get install -y apache2
   SHELL
end
