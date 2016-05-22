# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "debian/jessie64"

  config.vm.network "private_network", ip: "10.10.10.10"

  config.vm.synced_folder ".", "/vagrant", type: :nfs

  config.vm.provision :ansible do |ansible|
    ansible.playbook       = "ansible/provision.yml"
    ansible.limit          = "all"
  end
end
