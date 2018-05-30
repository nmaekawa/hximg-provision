# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # vagrant dns; requires `vagrant plugin install landrush`
  config.landrush.enabled = true
  config.landrush.tld = "vm"

  # loris image server node
  config.vm.define "loris" do |loris|
    loris.vm.box = "bento/ubuntu-16.04"
    loris.vm.hostname = "loris.vm"
    loris.vm.network "private_network", ip: "10.8.0.10"

    loris.ssh.forward_agent = true
    loris.ssh.insert_key = false

    loris.vm.provider "virtualbox" do |v|
        v.memory = "4096"
    end
  end

  # ids image server node
  config.vm.define "ids" do |ids|
    ids.vm.box = "bento/ubuntu-16.04"
    ids.vm.hostname = "ids.vm"
    ids.vm.network "private_network", ip: "10.8.0.9"

    ids.ssh.forward_agent = true
    ids.ssh.insert_key = false

    ids.vm.provider "virtualbox" do |v|
        v.memory = "4096"
    end
  end

  # manifest node
  config.vm.define "manifest" do |manifest|
    manifest.vm.box = "bento/ubuntu-16.04"
    manifest.vm.hostname = "manifest.vm"
    manifest.vm.network "private_network", ip: "10.8.0.11"

    manifest.ssh.forward_agent = true
    manifest.ssh.insert_key = false

    manifest.vm.provider "virtualbox" do |v|
        v.memory = "1096"
    end
  end
end
