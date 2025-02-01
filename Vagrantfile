Vagrant.configure("2") do |config|
  config.hostmanager.enabled = true 
  config.hostmanager.manage_host = true
  
### DB vm  ####
  config.vm.define "Jenkins" do |db01|
    db01.vm.box = "ubuntu/jammy64"
    db01.vm.hostname = "Jenkins"
    db01.vm.network "private_network", ip: "192.168.56.15"
    db01.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
   end

  end
  
### Memcache vm  #### 
  config.vm.define "Sonarqube" do |mc01|
    mc01.vm.box = "ubuntu/jammy64"
    mc01.vm.hostname = "Sonarqube"
    mc01.vm.network "private_network", ip: "192.168.56.14"
    mc01.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
   end
  end
  
### RabbitMQ vm  ####
  config.vm.define "Nexus" do |rmq01|
    rmq01.vm.box = "ubuntu/jammy64"
  rmq01.vm.hostname = "Nexus"
    rmq01.vm.network "private_network", ip: "192.168.56.13"
    rmq01.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
   end
  end
  
end
