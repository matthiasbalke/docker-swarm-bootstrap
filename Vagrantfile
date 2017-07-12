# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "centos/7"

  config.vm.provider 'virtualbox' do |v|
    # use linked clones if possible
    v.linked_clone = true if Gem::Version.new(Vagrant::VERSION) >= Gem::Version.new('1.8.0')
  end

  config.vm.define "swarm-manager-1" do |manager1|
    manager1.vm.network "private_network", ip: "192.168.50.10"
    manager1.vm.hostname = "swarm-manager-1"
  end

  config.vm.define "swarm-worker-1" do |worker1|
    worker1.vm.network "private_network", ip: "192.168.50.20"
    worker1.vm.hostname = "swarm-worker-1"
  end

  config.vm.define "swarm-worker-2" do |worker2|
    worker2.vm.network "private_network", ip: "192.168.50.30"
    worker2.vm.hostname = "swarm-worker-2"
  end

end
