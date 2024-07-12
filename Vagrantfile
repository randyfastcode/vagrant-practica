Vagrant.configure("2") do |config|
    config.vm.define "web1" do |web1|
      web1.vm.box = "ubuntu/jammy64"
      web1.vm.hostname = "web1"
      web1.vm.network "private_network", ip: "192.168.56.101"
      web1.vm.synced_folder "./html/web1", "/var/www/html"
  
      web1.vm.provision "shell", inline: <<-SHELL
        sudo apt-get update
        sudo apt-get install -y apache2
      SHELL
    end
  
    config.vm.define "web2" do |web2|
      web2.vm.box = "ubuntu/jammy64"
      web2.vm.hostname = "web2"
      web2.vm.network "private_network", ip: "192.168.56.102"
      web2.vm.synced_folder "./html/web2", "/var/www/html"
  
      web2.vm.provision "shell", inline: <<-SHELL
        sudo apt-get update
        sudo apt-get install -y apache2
      SHELL
    end
  end
  