Vagrant.configure("2") do |config|

  ## Choose your base box
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", 3072]
  end

  # SSH Agent forwarding
  config.ssh.forward_agent = true
end
