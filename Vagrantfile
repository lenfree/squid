# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'centos6.6'
  config.vm.box_url = 'https://github.com/tommy-muehle/puppet-vagrant-boxes/releases/download/1.0.0/centos-6.6-x86_64.box'

  config.vm.network 'private_network', ip: '192.168.2.5',
    virtualbox__intnet: true
  config.vm.network 'public_network'
  config.ssh.forward_agent = true
  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'proxy.yml'
    ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
    ansible.verbose = 'vvvv'
  end
end
