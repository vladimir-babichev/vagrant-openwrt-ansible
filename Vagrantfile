Vagrant.configure("2") do |config|
  config.vm.box = "openwrt-19.07.3"
  config.vm.define "router"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--nic2", "nat"]
    v.customize ["modifyvm", :id, "--nic3", "bridged", "--bridgeadapter3", "en0"]
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "site.yaml"
    ansible.groups = {
        "openwrt" => ["router"]
    }
  end
end
