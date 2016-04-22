Vagrant.configure(2) do |config|
  # base box 
  config.vm.box = "ubuntu/precise64"
  # port forwarding
  config.vm.network "forwarded_port", guest: 80, host: 8080, auto_correct: true
  # private network/ip
  config.vm.network "private_network", ip: "192.168.33.11"
  # provisioning
  config.vm.provision :shell, :path => ".provision/bootstrap.sh"
end
