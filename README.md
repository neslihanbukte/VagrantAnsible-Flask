<h1>Flask Uygulaması - Vagrant ve Ansible ile Deploy</h1>

Bu proje, Flask uygulamasını Vagrant ve Ansible kullanarak bir sanal makine üzerinde çalıştırmayı amaçlar. Amaç, otomatikleştirilmiş bir geliştirme ortamı sunmaktır.

## Özellikler
- **Vagrant**: Sanal makine oluşturma ve yönetme.
- **Ansible**: Sanal makineye yazılım yükleme ve yapılandırma.
- **Flask**: Web uygulamasının temel altyapısı.
- **Nginx**: Ters proxy (reverse proxy) sunucusu.

---

## Kullanım Adımları

1. **Depoyu Klonlayın**
   - İlk olarak, bu projeyi yerel bilgisayarınıza klonlayın:
     ```bash
     git clone <repository-url>
     cd <repository-folder>
     ```

2. **Gerekli Araçların Kurulumu**
   - Aşağıdaki araçların sisteminizde kurulu olduğundan emin olun:
     - [Vagrant](https://www.vagrantup.com/downloads)
     - [VirtualBox](https://www.virtualbox.org/)
     - [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

3. **Proje Dosyalarının Yapısı**
   - Proje dosyaları şu şekilde olmalıdır:
     ```
     project-folder/
     ├── Vagrantfile
     └── ansible/
         ├── app.py
         ├── nginx.conf
         ├── inventory
         └── main.yml
     ```

4. **Sanal Makine Başlatılması**
   - Proje klasöründe terminal açın ve şu komutu çalıştırın:
     ```bash
     vagrant up
     ```
   - Bu komut, sanal makineyi oluşturur ve Ansible ile tüm yapılandırmaları uygular.

5. **Uygulama Test Edilmesi**
   - Tarayıcıdan şu adresi ziyaret edin:
     ```
     http://localhost:8081
     ```
   - Eğer her şey doğru çalışıyorsa, “Hello, World! Vagrant ve Ansible ile deploy edildi.” mesajını görmelisiniz.

---

## Projede Kullanılan Teknolojiler

- **Vagrant**: Sanal makineler için geliştirme ortamı aracı.
- **VirtualBox**: Sanal makine sağlayıcısı.
- **Ansible**: Sunucu konfigürasyonu ve yönetimi için otomasyon aracı.
- **Flask**: Python tabanlı mikro web çerçevesi.
- **Nginx**: Web sunucusu ve ters proxy.

---

## Proje Adımları

1. **Vagrantfile ve Ansible Yapılandırmalarının Hazırlanması**
   - Vagrantfile, sanal makinenin yapılandırmasını yönetir. Bu dosyada, sanal makinenin kurulum ve yapılandırma ayarlarını tanımladık.
   - Ansible, uygulamanın sanal makine üzerinde doğru şekilde yapılandırılmasını sağlamak için `main.yml` dosyasını kullanır. Ayrıca, `inventory` dosyası hedef makineleri tanımlar.

2. **Flask Uygulamasının Yazılması**
   - `app.py` dosyası Flask uygulamasının temel altyapısını içerir. Burada web uygulamasının temel işlevselliği tanımlanır.

3. **Nginx Konfigürasyonunun Yapılması**
   - `nginx.conf` dosyası, Nginx'in Flask uygulamasına gelen istekleri doğru şekilde yönlendirmesini sağlamak için yapılandırılır. Bu adım, Nginx'in ters proxy olarak çalışmasını sağlar.

4. **Sanal Makinenin ve Uygulamanın Başlatılması**
   - Vagrant ile sanal makineyi oluşturun ve Ansible ile yapılandırma işlemlerini otomatikleştirin. Bu sayede Flask uygulamanız doğru ortamda çalıştırılabilir.

---

