# vagrant-demo
Vagrant, yazılım geliştiriciler ve sistem yöneticileri için sanal makineler oluşturmayı, dağıtmayı ve yönetmeyi kolaylaştıran bir araçtır. Vagrant, farklı sanal makine sağlayıcılarıyla (VirtualBox, VMware, Docker, vb.) çalışarak geliştirici ortamlarının tutarlı ve taşınabilir olmasını sağlar.



### Genel Komutlar
<br>

1. **autocomplete**:<br>
   - **Açıklama**: Komut satırı otomatik tamamlama işlevselliğini yönetir.<br>
   - **Alt Komutlar**:<br>
     - `vagrant autocomplete install`: Otomatik tamamlama işlevini kurar.<br>
     - `vagrant autocomplete uninstall`: Otomatik tamamlama işlevini kaldırır.<br>
   - **Örnek Kullanım**:<br>
     ```bash
     vagrant autocomplete install
     ```

2. **box**:<br>
   - **Açıklama**: Box'ları (önceden yapılandırılmış sanal makine görüntüleri) yönetir.<br>
   - **Alt Komutlar**:<br>
     - `vagrant box add <name>`: Yeni bir box ekler.<br>
     - `vagrant box remove <name>`: Bir box'ı kaldırır.<br>
     - `vagrant box list`: Yüklü box'ları listeler.<br>
   - **Örnek Kullanım**:<br>
     ```bash
     vagrant box add ubuntu/bionic64
     vagrant box list
     vagrant box remove ubuntu/bionic64
     ```

3. **cloud**:<br>
   - **Açıklama**: Vagrant Cloud ile ilgili işlemleri yönetir.<br>
   - **Alt Komutlar**:<br>
     - `vagrant cloud publish`: Bir box'ı Vagrant Cloud'a yayınlar.<br>
     - `vagrant cloud delete`: Vagrant Cloud'dan bir box'ı siler.<br>
     - `vagrant cloud search <query>`: Vagrant Cloud'da box arar.<br>
   - **Örnek Kullanım**:<br>
     ```bash
     vagrant cloud publish username/box-name version provider
     vagrant cloud search ubuntu
     ```

4. **destroy**:<br>
   - **Açıklama**: Vagrant makinesini durdurur ve tüm izlerini siler.<br>
   - **Örnek Kullanım**:<br>
     ```bash
     vagrant destroy
     ```

5. **global-status**:<br>
   - **Açıklama**: Bu kullanıcı için mevcut tüm Vagrant ortamlarının durumunu gösterir.<br>
   - **Örnek Kullanım**:<br>
     ```bash
     vagrant global-status
     ```

6. **halt**:<br>
   - **Açıklama**: Vagrant makinesini durdurur.<br>
   - **Örnek Kullanım**:<br>
     ```bash
     vagrant halt
     ```

7. **help**:<br>
   - **Açıklama**: Belirli bir alt komut için yardımı gösterir.<br>
   - **Örnek Kullanım**:<br>
     ```bash
     vagrant help up
     ```

8. **init**:<br>
   - **Açıklama**: Bir Vagrant ortamını başlatarak bir Vagrantfile oluşturur.<br>
   - **Örnek Kullanım**:<br>
     ```bash
     vagrant init ubuntu/bionic64
     ```

9. **login**:<br>
   - **Açıklama**: Vagrant Cloud'a giriş yapar.<br>
   - **Örnek Kullanım**:<br>
     ```bash
     vagrant login
     ```

10. **package**:<br>
    - **Açıklama**: Çalışan bir Vagrant ortamını bir box dosyasına paketler.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant package --output my_box_name.box
      ```

11. **plugin**:<br>
    - **Açıklama**: Vagrant eklentilerini yönetir.<br>
    - **Alt Komutlar**:<br>
      - `vagrant plugin install <name>`: Bir eklenti yükler.<br>
      - `vagrant plugin uninstall <name>`: Bir eklentiyi kaldırır.<br>
      - `vagrant plugin update <name>`: Bir eklentiyi günceller.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant plugin install vagrant-vbguest
      vagrant plugin list
      vagrant plugin uninstall vagrant-vbguest
      ```

12. **port**:<br>
    - **Açıklama**: Konuk makinelerin port yönlendirme bilgilerini gösterir.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant port
      ```

13. **powershell**:<br>
    - **Açıklama**: PowerShell uzaktan erişimi ile makineye bağlanır.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant powershell
      ```

14. **provision**:<br>
    - **Açıklama**: Vagrant makinesini provisioning işlemini gerçekleştirir.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant provision
      ```

15. **push**:<br>
    - **Açıklama**: Bu ortam içindeki kodu yapılandırılmış bir hedefe dağıtır.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant push
      ```

16. **rdp**:<br>
    - **Açıklama**: Vagrant makinesine RDP (Uzak Masaüstü Protokolü) ile bağlanır.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant rdp
      ```

17. **reload**:<br>
    - **Açıklama**: Vagrant makinesini yeniden başlatır ve yeni Vagrantfile yapılandırmasını yükler.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant reload
      ```

18. **resume**:<br>
    - **Açıklama**: Askıya alınmış bir Vagrant makinesini devam ettirir.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant resume
      ```

19. **serve**:<br>
    - **Açıklama**: Vagrant sunucusunu başlatır.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant serve
      ```

20. **snapshot**:<br>
    - **Açıklama**: Anlık görüntüleri yönetir.<br>
    - **Alt Komutlar**:<br>
      - `vagrant snapshot save <name>`: Anlık görüntü kaydeder.<br>
      - `vagrant snapshot restore <name>`: Anlık görüntüyü geri yükler.<br>
      - `vagrant snapshot list`: Anlık görüntüleri listeler.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant snapshot save my_snapshot
      vagrant snapshot list
      vagrant snapshot restore my_snapshot
      ```

21. **ssh**:<br>
    - **Açıklama**: Vagrant makinesine SSH ile bağlanır.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant ssh
      ```

22. **ssh-config**:<br>
    - **Açıklama**: OpenSSH yapılandırmasını çıktılar.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant ssh-config
      ```

23. **status**:<br>
    - **Açıklama**: Vagrant makinesinin durumunu gösterir.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant status
      ```

24. **suspend**:<br>
    - **Açıklama**: Vagrant makinesini askıya alır.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant suspend
      ```

25. **up**:<br>
    - **Açıklama**: Vagrant ortamını başlatır ve sağlama işlemini gerçekleştirir.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant up
      ```

26. **upload**:<br>
    - **Açıklama**: Dosyaları iletişim kurarak makineye yükler.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant upload my_local_file /vagrant
      ```

27. **validate**:<br>
    - **Açıklama**: Vagrantfile'ı doğrular.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant validate
      ```

28. **version**:<br>
    - **Açıklama**: Mevcut ve en son Vagrant sürümünü gösterir.<br>
    - **Örnek Kullanım**:<br>
      ```bash
      vagrant version
      ```

