# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end
  config.vm.box = 'centos/7'

  config.vm.define :myplaybook do |t|
  end

  config.vm.network 'forwarded_port', guest: 9229, host: 9229

  config.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'playbook.yml'
      ansible.host_key_checking = false
      ansible.inventory_path = 'inventory/vagrant/'
      ansible.raw_arguments = ['--vault-password-file=~/.vault']
      ansible.limit = 'all'
    end
  end
