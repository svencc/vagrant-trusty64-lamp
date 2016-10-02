Vagrant.configure("2") do |config|
  
  #BOX & VIRTUAL-MACHINE
  config.vm.box = "ubuntu/trusty64"
  config.vm.memory = 1024
  config.vm.cpus = 1

  #APACHE2
  config.vm.provision :shell, path: "bootstrap/apache.sh"

  #SYNCED FOLDERS  HOST->GUEST
  #config.vm.synced_folder "www/", "/var/www"



  #NETWORKING
  ##PORT-FORWARING
  #config.vm.network :forwarded_port, guest: 80, host: 2222
  config.vm.network :private_network, ip: "192.168.68.101"

  #SHARE

  #SSH CONNECT
  config.ssh.insert_key = false
  config.ssh.keys_only  = false
  config.ssh.username   = "vagrant"
  config.ssh.password   = "vagrant"
end