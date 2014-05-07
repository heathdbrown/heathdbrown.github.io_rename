# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "base"
  config.vm.box_url = 'http://files.vagrantup.com/precise64.box'
  config.vm.synced_folder "~/Projects/heathdbrown.github.io/", "/vagrant_data"
  config.vm.network "forwarded_port", guest: 4000, host: 4000
end
