require 'time'

Vagrant.configure("2") do |config|

  config.vm.hostname = "fsa"
  config.vm.box = "ubuntu_1404"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  config.vm.network :private_network, ip: "33.33.33.10"
  
  config.vm.synced_folder "~/development", "/home/vagrant/development"
  config.vm.define "fsa-dev"

  config.vm.provider "virtualbox" do |v|
    v.name = "fsa-dev"
    v.memory = 3072
    v.cpus = 2
  end

  config.berkshelf.enabled = true

  config.vm.provision "chef_solo" do |chef|
    chef.roles_path = "roles"
    chef.add_recipe("omnibus_updater")
    chef.add_role("base")
  end
 
  #Set the VM timezone to the host timezone
  offset = ((Time.zone_offset(Time.now.zone)/60)/60)
  zonesuffix = offset >= 0 ? "+#{offset.to_s}" : "#{offset.to_s}"
  timezone = 'Etc/GMT' + zonesuffix
  config.vm.provision :shell, :inline => "echo \"#{timezone}\" | sudo tee /etc/timezone && dpkg-reconfigure --frontend noninteractive tzdata"

end
