# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # ansible
  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "generic/ubuntu2004"
    ansible.vm.hostname = "ansible"
    ansible.vm.network "private_network", ip: "192.168.1.100"
    ansible.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
  end

  # ubuntu01
  config.vm.define "ubuntu01" do |ubuntu01|
    ubuntu01.vm.box = "ubuntu/trusty64"
    ubuntu01.vm.hostname = "ubuntu01"
    ubuntu01.vm.network "private_network", ip: "192.168.100.10"
    ubuntu01.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
  end
  
  # ubuntu02
  config.vm.define "ubuntu02" do |ubuntu02|
    ubuntu02.vm.box = "ubuntu/trusty64"
    ubuntu02.vm.hostname = "ubuntu02"
    ubuntu02.vm.network "private_network", ip: "192.168.100.20"
    ubuntu02.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
  end

  # centos01
  config.vm.define "centos01" do |centos01|
    centos01.vm.box = "centos/7"
    centos01.vm.hostname = "centos01"
    centos01.vm.network "private_network", ip: "192.168.200.10"
    centos01.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
  end
  
  # centos02
  config.vm.define "centos02" do |centos02|
    centos02.vm.box = "centos/7"
    centos02.vm.hostname = "centos01"
    centos02.vm.network "private_network", ip: "192.168.200.10"
    centos02.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
  end

  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
