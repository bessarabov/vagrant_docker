Vagrant::Config.run do |config|

    config.vm.box = "ubuntu/trusty64"
    config.vm.host_name = "machine"

    config.vm.forward_port 8080, 80
    config.vm.forward_port 8443, 443

    config.vm.provision "ansible" do |ansible|
        ansible.verbose = "v"
        ansible.playbook = "playbooks/create_server.yml"
    end

end
