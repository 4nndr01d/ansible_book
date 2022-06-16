VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.ssh.insert_key = false

  config.vm.define "vagrant1" do |vagrant1|
    vagrant1.vm.box = "ubuntu/trysty64"
#     Путь до локального образа vm
    vagrant1.vm.box_url = "/home/user/trusty-server-cloudimg-amd64-vagrant-disk1.box"
    vagrant1.vm.network  "forwarded_port", guest: 80, host: 8080
    vagrant1.vm.network  "forwarded_port", guest: 443, host: 8443
  end
  config.vm.define "vagrant2" do |vagrant2|
    vagrant2.vm.box = "ubuntu/trysty64"
    vagrant2.vm.box_url = "/home/user/trusty-server-cloudimg-amd64-vagrant-disk1.box"
    vagrant2.vm.network "forwarded_port", guest: 80, host: 8081
    vagrant2.vm.network "forwarded_port", guest: 443, host: 8444
  end
  config.vm.define "vagrant3" do |vagrant3|
    vagrant3.vm.box = "ubuntu/trysty64"
    vagrant3.vm.box_url = "/home/user/trusty-server-cloudimg-amd64-vagrant-disk1.box"
    vagrant3.vm.network "forwarded_port", guest: 80, host: 8082
    vagrant3.vm.network "forwarded_port", guest: 443, host: 8445
  end
end
