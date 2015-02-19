Vagrant::Config.run do |config|

    config.vm.box = "ubuntu/trusty64"
    config.vm.host_name = "machine"

    config.vm.forward_port 80, 8080
    config.vm.forward_port 443, 8443

    config.vm.provision "ansible" do |ansible|
        ansible.verbose = "v"
        ansible.playbook = "playbooks/create_server.yml"
    end

end
