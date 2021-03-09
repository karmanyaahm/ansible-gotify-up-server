# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.box = "debian/buster64"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "test.yml"
  end
  config.vm.network "forwarded_port", guest: 80, host: 5080
  config.vm.network "forwarded_port", guest: 443, host: 5443

end

