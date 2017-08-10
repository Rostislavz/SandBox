
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"

#config resources for machines
  config.vm.provider :virtualbox do |vb|

    vb.customize ["modifyvm", :id, "--cpus", "1", "--memory", "512"]

  end



end
