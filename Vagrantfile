Vagrant.configure("2") do |config|

  ## Choose your base box
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", 3072]
  end

  # SSH Agent forwarding
  config.ssh.forward_agent = true

  ## For masterless, mount your salt file root
  # config.vm.synced_folder "salt/roots/", "/srv/"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = :vv
    ansible.playbook = "server-playbooks/vagrant.yml"
    # ansible.ask_vault_pass = true
    ansible.vault_password_file = ".vault.txt"
  end

end
