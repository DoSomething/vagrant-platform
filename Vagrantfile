Vagrant.configure("2") do |config|

  ## Choose your base box
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", 3072]
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  end

  # SSH Agent forwarding
  config.ssh.forward_agent = true

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = :v
    ansible.playbook = "ansible/vagrant.yml"
    # ansible.ask_vault_pass = true
    ansible.vault_password_file = ".vault.txt"
  end

  # Solr.
  config.vm.network :forwarded_port, guest: 8983, host: 8983

end
