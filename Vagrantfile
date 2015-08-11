Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
#  config.vm.box = "centos-6.6-x86_64.box"
#  config.vm.box_url = "../packer/packer-vagrant-linux/build/centos-6.6-x86_64.box"

	config.vm.define "ansitest" do |ansitest|
		ansitest.vm.hostname = "ansitest"
  		config.vm.network "forwarded_port", guest: 80, host: 8888
  		config.vm.provision :ansible do |ansible|
        	ansible.playbook = "./playbook.yml"
	  end
  end
end
