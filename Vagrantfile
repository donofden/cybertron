Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.box_version = "20190119.0.0"
  config.vm.hostname = "cybertron"
  config.vm.network :private_network, ip: "192.168.56.202"
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.ssh.forward_agent = true

  config.vm.provider "virtualbox" do |vb|
     # To enable GUI mode
     # vb.gui = true
     vb.customize ["modifyvm", :id, "--name", "cybertron"]
  end

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"
  ##
  # NFS Shared Folders
  ##
  config.vm.synced_folder("../../private-git", "/mnt/nfs/web", :nfs=>true, :nfs_export=>true, :linux__nfs_options => ['rw','no_subtree_check','all_squash','async'])
  config.vm.synced_folder("/tmp", "/hosttmp", :nfs=>true, :nfs_export=>true, :linux__nfs_options => ['rw','no_subtree_check','all_squash','async'])

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant/ansible/all.yml"
    ansible.extra_vars = {
      ansible_python_interpreter: "/usr/bin/python3",
    }
  end
end
