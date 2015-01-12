# -*- mode: ruby -*-
# vi: set ft=ruby :

# Definit le provider par défaut
ENV['VAGRANT_DEFAULT_PROVIDER'] = 'vmware_workstation'

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
 
  # Definition de la machine (multiple machine)
  config.vm.define :master do |master|
    master.vm.box = "centos6"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

    # configure le nom de la machine
    master.vm.hostname = "master.des.lan"

    # configure une carte réseau
    master.vm.network "private_network", ip: "192.168.200.41"


  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
    master.vm.provider "virtualbox" do |vb|
      # Active la partie graphique de la vm. Si innactif, la vm
      # fonctionnera en background
      #vb.gui = true
      vb.name = "master"
      vb.memory = "512"
      vb.cpus = "1"
    end

    master.vm.provider "vmware_workstation" do |vw|
      # Active la partie graphique de la vm. Si innactif, la vm
      # fonctionnera en background
      #vb.gui = true
      vw.name = "master"
      vw.memory = "512"
      vw.cpus = "1"
    end
  
  # Enable provisioning with chef solo, specifying a cookbooks path, roles
  # path, and data_bags path (all relative to this Vagrantfile), and adding
  # some recipes and/or roles.
  #

  end

  config.vm.define :client do |client|
    client.vm.box = "centos6"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

    # configure le nom de la machine
    client.vm.hostname = "client.des.lan"

    # configure une carte réseau
    client.vm.network "private_network", ip: "192.168.200.42"
    

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
    client.vm.provider "virtualbox" do |vb|
      # Active la partie graphique de la vm. Si innactif, la vm
      # fonctionnera en background
      #vb.gui = true
      vb.name = "client"
      vb.memory = "512"
      vb.cpus = "1"
    end

    client.vm.provider "vmware_workstation" do |vw|
      # Active la partie graphique de la vm. Si innactif, la vm
      # fonctionnera en background
      #vb.gui = true
      vw.name = "client"
      vw.memory = "512"
      vw.cpus = "1"
    end
  
  # Enable provisioning with chef solo, specifying a cookbooks path, roles
  # path, and data_bags path (all relative to this Vagrantfile), and adding
  # some recipes and/or roles.
  #

  end


end