# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'ubuntu/trusty64'

  config.vm.define 'relay1' do |relay|
    relay.vm.network 'forwarded_port', guest: 9030, host: 9031
  end
  config.vm.define 'relay2' do |relay|
    relay.vm.network 'forwarded_port', guest: 9030, host: 9032
  end

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'provisioning/playbook.yml'
    ansible.groups = {
      'relays' => ['relay1', 'relay2']
    }
  end
end
