## Kullanım/Örnekler

Vagrant, sanal makineleri tanımlamak için Vagrantfile adında bir yapılandırma dosyası kullanır. Proje klasörünüzde bir Vagrantfile oluşturabilirsiniz.
```powershell
mkdir my-vagrant-project
cd my-vagrant-project
vagrant init 
```

Vagrantfile içinde sanal makine yapılandırmalarını belirtirsiniz. Örneğin, Ubuntu 20.04 kullanmak istiyorsanız, Vagrantfile şu şekilde olabilir:
```powershell
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
end
```

Sanal makineyi başlatmak için vagrant up komutunu kullanın.
```powershell
vagrant up
```

Sanal makineye SSH ile bağlanmak için vagrant ssh komutunu kullanın.
```powershell
vagrant ssh
```

Sanal makineyi durdurmak için vagrant halt, tamamen silmek için vagrant destroy komutlarını kullanabilirsiniz.
```powershell
vagrant halt
vagrant destroy
```

Diyelim ki bir web geliştirme ortamı kurmak istiyorsunuz. Vagrantfile'ınız şu şekilde olabilir:
```bash
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.network "private_network", type: "dhcp"
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y apache2
  SHELL
end
```
