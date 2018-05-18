# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.synced_folder ".", "/vagrant",
      owner: "root", group: "root"
    
  # 建立虛擬機之後，在虛擬機中執行的程式

  config.vm.provision "shell", path: "installdocker.sh"
  config.ssh.insert_key = true

  config.vm.provider :virtualbox do |vb|
    vb.memory = 4096
  end


  config.vm.define :docker01 do |docker01|
    docker01.vm.provision "shell", inline: "locale-gen zh_TW.UTF-8"
  end

  config.vm.define :docker02 do |docker02|
    docker02.vm.provision "shell", inline: "locale-gen zh_TW.UTF-8"
  end

  config.vm.define :docker03 do |docker03|
    docker03.vm.provision "shell", inline: "locale-gen zh_TW.UTF-8"
  end
end
