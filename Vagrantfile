# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.provider :libvirt do |vb|
    vb.memory = 4096
    vb.cpus = "4"
  end

  config.vm.define "logstash" do |node|
    config.vm.hostname = "logstash.local"
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.compatibility_mode = "2.0"
  end
end