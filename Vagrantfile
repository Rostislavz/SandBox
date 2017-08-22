
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"

#config resources for machines
  config.vm.provider :virtualbox do |vb|

    vb.customize ["modifyvm", :id, "--cpus", "1", "--memory", "512"]

  end

  config.vm.provider "vmware_fusion" do |v, override|

      override.vm.box = "ubuntu/xenial64"

      v.vmx["memsize"] = "512"

      v.vmx["numvcpus"] = "1"

  end

   config.vm.define :host1 do |host1|

    host1.vm.network "private_network", ip: "192.168.2.21",
    
      virtualbox__intnet: "vlan2"

    host1.vm.hostname = "host1.local"

   end

   config.vm.define :host2 do |host2|

    host2.vm.network "private_network", ip: "192.168.2.22",
  
      virtualbox__intnet: "vlan2"


    host2.vm.hostname = "host2.local"

   end

   config.vm.define :host3 do |host3|

    host3.vm.network "private_network", ip: "192.168.3.33",
   
      virtualbox__intnet: "vlan3"


    host3.vm.hostname = "host3.local"

   end

   config.vm.define :host4 do |host4|

    host4.vm.network "private_network", ip: "192.168.3.34",
    
      virtualbox__intnet: "vlan3"



    host4.vm.hostname = "host4.local"

   end
  

  config.vm.define :host5 do |host5|

  	host5.vm.box = "centos/6"
  	host5.vm.box_url = "centos/6"
  	
    host5.vm.network "private_network", ip: "192.168.2.25",
    
      virtualbox__intnet: "vlan2"
    
    host5.vm.network "private_network", ip: "192.168.3.35",
    
      virtualbox__intnet: "vlan3"


    host5.vm.hostname = "host5.local"

   end


end
