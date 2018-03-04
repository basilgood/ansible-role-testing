# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.hostname = "testing"
  config.vm.box = "plumelo/xenial64"

  config.vm.provider :lxc do |lxc|
    lxc.container_name = "testing"
  end

  config.vm.provision "shell",
    :path => "specs.sh",
    :upload_path => "/home/vagrant/specs",
    # change role name below
    :args => "--install ansible-role-testing"
end
