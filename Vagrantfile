# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

script = <<SCRIPT
echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf > /dev/null
apt-get update
SCRIPT

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment require
  #config.vm.box = "hiroshima-arc/martini"
  config.vm.box = "martini"
  config.vm.box_version = "0.0.1"

  config.vm.network :forwarded_port, host: 9009, guest: 9000
  config.vm.synced_folder ".", "/vagrant", mount_options: ['dmode=777','fmode=777']

  config.vm.provider "virtualbox" do |vb|
    vb.gui = false

    # Use VBoxManage to customize the VM. For example to change memory:
    vb.customize ["modifyvm", :id, "--memory", "4096"]
    vb.customize ["modifyvm", :id, "--vram", "128"]
    vb.customize ["modifyvm", :id, "--accelerate3d", "on"]
  end
end
