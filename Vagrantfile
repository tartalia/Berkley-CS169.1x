# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "shell", privileged: true, inline: <<-SHELL
     apt-get update
     command curl -sSL https://rvm.io/mpapis.asc | gpg --import -
     curl -sSL https://get.rvm.io | bash -s stable --ruby=2.2.2
     source /home/vagrant/.rvm/scripts/rvm
     curl -fsSL c9setup.saasbook.info | bash --login
  SHELL
end
