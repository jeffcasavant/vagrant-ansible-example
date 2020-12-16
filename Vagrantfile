Vagrant.configure("2") do |config|
  # base image
  config.vm.box = "peru/ubuntu-20.04-desktop-amd64"
  config.vm.box_version = "20201203.01"
  # default user is "vagrant" with password "vagrant"

  config.vm.provider "virtualbox" do |vbox|
    vbox.gui = true
    vbox.name = "Build"

    # vm hardware settings
    vbox.memory = 2048
    vbox.cpus = 4
  end

  config.vm.provision "ansible" do |ansible|
    # and then once vagrant has stood up the VM, run ansible
    ansible.playbook = "playbook.yml"
  end
end
