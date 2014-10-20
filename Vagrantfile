VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Vagrant box
  config.vm.box = "debian73"
  config.vm.box_url = "http://puppet-vagrant-boxes.puppetlabs.com/debian-73-x64-virtualbox-puppet.box"
  config.vm.host_name = "test"

  # Network configs
  config.vm.network :private_network, ip: "192.168.10.10"

  # Virtualbox configs
  config.vm.provider "virtualbox" do |v|
    v.name = "test"
  end


  # Puppet provision
  config.vm.provision "puppet" do |puppet|
    puppet.manifests_path = "puppet/manifests"
    puppet.manifest_file  = "site.pp"
    puppet.module_path = ['puppet/modules']
  end

end