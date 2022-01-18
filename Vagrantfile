# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = 'ubuntu/focal64'

  config.vm.network 'forwarded_port', guest: 80, host: 8888

  config.vm.provision :server, type: :ansible do |ansible|
    ansible.playbook = 'server.yml'
    ansible.compatibility_mode = '2.0'
  end
end
