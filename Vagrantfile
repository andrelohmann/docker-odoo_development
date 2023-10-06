#Vagrant.configure("2") do |config|
#  config.vm.provider "docker" do |d|
#    d.image = "nginx:latest"
#    d.ports = ["8080:80"]
#    d.name = "nginx-container"
#  end
#end

#Vagrant.configure("2") do |config|
#  config.vm.define "app" do
#    config.vm.provider "docker" do |d|
#      d.image = "nginx"
#    end
#  end
#
#  config.vm.define "consul" do
#    config.vm.provider "docker" do |d|
#      d.image = "consul"
#    end
#  end
#end

Vagrant.configure("2") do |config|
  config.vm.define "docker"  do |docker|
    docker.vm.network :private_network, type: "dhcp", docker_network__internal: true
    docker.vm.network :private_network, ip: "192.168.50.4", netmask: "24"
    docker.vm.provider "docker" do |d|
      d.image = "nginx:latest"
      d.ports = ["8080:80"]
      d.name = "nginx-container"
    end
  end
end
