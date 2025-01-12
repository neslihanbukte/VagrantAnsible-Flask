Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64" 
  config.vm.boot_timeout = 600
  
  # Nginx için 80 -> 8081 yönlendirmesi
  config.vm.network "forwarded_port", guest: 80, host: 8081
  
  # Flask için 5000 -> 5000 yönlendirmesi
  config.vm.network "forwarded_port", guest: 5000, host: 5000
  
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "ansible/main.yml"
    ansible.inventory_path = "ansible/inventory"
  end
end

