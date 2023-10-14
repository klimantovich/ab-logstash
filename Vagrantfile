Vagrant.configure("2") do |config|

  config.vm.define "logstash" do |logstash|
    logstash.vm.box = "ubuntu/focal64"
    logstash.vm.hostname = "logstash.vm"
    logstash.vm.network "private_network", ip: "10.0.5.10"

    logstash.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "3072"
    end

    logstash.vm.provision :ansible do |ansible|
      ansible.playbook = "./logstash_setup.yml"
    end

  end

end

