# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "moozer/deb8-base"

  config.vm.provider :libvirt do |libvirt|
    libvirt.host = ""
    libvirt.nested = true
    libvirt.memory = 1536
  end

  config.vm.synced_folder ".", "/vagrant", type: "9p"
  config.vm.synced_folder "shared", "/shared", type: "9p", accessmode: "mapped", owner: 5000

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "test.yml"
#    ansible.inventory_path = "inventory"
#    ansible.groups = {
#      "routers" => ["ipsrouter"],
#      "servers" => ["ipsclient", "ipsserver"]
#    }
  end
end
