# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/ubuntu-16.04"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = 'v'
    ansible.playbook = "provisioning/site.yml"
    ansible.raw_arguments = ENV['ANSIBLE_ARGS']
  end

  config.vm.network "forwarded_port", guest: 1880, host: 1880

end
