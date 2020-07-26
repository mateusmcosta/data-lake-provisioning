Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-7.5"
  config.vm.define "hdp-master" do |m|
    m.vm.hostname = "hdp-master"
    m.vm.network "private_network", ip: "10.220.0.11"
    m.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", "2048"]
        vb.customize ["modifyvm", :id, "--cpus", "2"]
    end
  end

  config.vm.define "hdp-node01" do |m|
    m.vm.hostname = "hdp-node01"
    m.vm.network "private_network", ip: "10.220.0.12"
    m.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", "1024"]
        vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
  end

  config.vm.define "hdp-node02" do |m|
    m.vm.hostname = "hdp-node02"
    m.vm.network "private_network", ip: "10.220.0.13"
    m.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "1024"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
  end

  config.vm.define "custumer-db" do |m|
    m.vm.hostname = "custumer-db"
    m.vm.network "private_network", ip: "10.220.0.21"
    m.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "1024"]
      vb.customize ["modifyvm", :id, "--cpus", "2"]
    end
  end
end
