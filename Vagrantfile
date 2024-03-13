Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu-22.04"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "VagrantTest"
    vb.gui = false
    vb.memory = "2048"
    vb.cpus = 1
  end
  config.vm.hostname = "VagrantTest"
  config.vm.synced_folder ".", "/home/vagtest/note",
    owner: "www-data", group: "www-data"
  config.vm.network "forwarded_port", guest: 80, host: 8000
  config.vm.network "forwarded_port", guest: 3306, host: 33060
  config.vm.network "private_network", ip: "192.168.56.110"
end
