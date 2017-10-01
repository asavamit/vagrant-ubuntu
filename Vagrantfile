Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 80, host: 1080
  config.vm.network "forwarded_port", guest: 9292, host: 92
  config.vm.network "forwarded_port", guest: 8080, host: 18080
  config.vm.network "forwarded_port", guest: 8081, host: 18081
  ##config.vm.network "private_network", ip: "192.168.10.9", auto_config: false
  config.vm.provision :shell, path: "bootstrap.sh"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
  end
end
