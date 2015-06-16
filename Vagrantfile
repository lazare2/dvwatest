Vagrant.configure("2") do |config|

  config.vm.box = "debian-wheezy72-x64-vbox43"
  config.vm.box_url = "http://box.puphpet.com/debian-wheezy72-x64-vbox43.box"

  config.vm.network :forwarded_port, guest: 80, host: 8090

  config.vm.provider :virtualbox do |vb|
    vb.gui = false
  end

  config.vm.provision :shell, :path => "bootstrap.sh"
end
