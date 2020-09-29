Vagrant.configure("2") do |config|
  config.vm.define "k8s-master" do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "k8s-master"
    config.vm.network "private_network", ip: "192.168.36.10"
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "setup.yml"
    end
  end
  config.vm.define "k8s-worker-1" do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "k8s-worker-1"
    config.vm.network "private_network", ip: "192.168.36.11"
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "setup.yml"
    end
  end
  config.vm.define "k8s-worker-2" do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "k8s-worker-2"
    config.vm.network "private_network", ip: "192.168.36.12"
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "setup.yml"
    end
  end
end
