# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|

  config.vm.box      = 'precise64'
  config.vm.box_url  = 'http://files.vagrantup.com/precise64.box'
  config.vm.hostname = 'mysql.dev.example.net'

  config.vm.network :private_network, ip: '192.168.33.10'

  config.vm.provision :ansible do |ansible|
    ansible.inventory_file = './hosts.ini'
    ansible.hosts = 'mysql-service'
    ansible.sudo = true
    ansible.playbook = './ansible/playbook.yml'
  end

end
