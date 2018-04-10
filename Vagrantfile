Vagrant.configure("2") do |config|

    config.vm.synced_folder "./provisioning", "/vagrant_data"
    
    config.ssh.insert_key = false
  
    config.vm.define "vagrantlamp" do |vagrantlamp|
        vagrantlamp.vm.box = "ubuntu/xenial64"
        vagrantlamp.vm.network :private_network, ip: "192.168.55.56"
        vagrantlamp.vm.network "forwarded_port", guest: 80, host: 8080
        vagrantlamp.vm.network "forwarded_port", guest: 443, host: 8443
    end

end