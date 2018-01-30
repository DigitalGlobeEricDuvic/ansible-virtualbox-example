Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.network "private_network", ip: "192.168.33.5"

  config.vm.provision "ansible_local" do |ansible|
    ansible.verbose = "y"
    ansible.playbook = "site.yml"
    ansible.install_mode = "pip"
    ansible.galaxy_role_file = "requirements.yml"
  end
end
