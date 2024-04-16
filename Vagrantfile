Vagrant.configure("2") do |config|

  # Define the base box for the first three VMs
  config.vm.define "vm1" do |vm1|
    vm1.vm.box = "hashicorp/bionic64"
    vm1.vm.network "private_network", ip: "192.168.56.4"
  end

  config.vm.define "vm2" do |vm2|
    vm2.vm.box = "hashicorp/bionic64"
    vm2.vm.network "private_network", ip: "192.168.56.5"
  end

  config.vm.define "vm3" do |vm3|
    vm3.vm.box = "hashicorp/bionic64"
    vm3.vm.network "private_network", ip: "192.168.56.6"
  end

  config.vm.define "vm4" do |vm4|
    vm4.vm.box = "hashicorp/bionic64"
    vm4.vm.network "private_network", ip: "192.168.56.7"
  end

  # Define the base box for the fourth VM
  # config.vm.define "vm4" do |vm4|
  #   vm4.vm.box = "centos/7"
  #   vm4.vm.network "private_network", ip: "192.168.56.7"
  # end

end
