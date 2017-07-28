Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 22, host: 1222
  config.vm.network "forwarded_port", guest: 80, host: 1080
  config.vm.network "forwarded_port", guest: 443, host: 1443

  config.vm.network "private_network", ip: "192.168.47.110"

   config.vm.provider "virtualbox" do |vb|
     vb.memory = "3500"
   end

end