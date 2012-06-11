# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "lucid32"

  config.vm.forward_port 80, 8080
  config.vm.forward_port 3306, 8081

  config.vm.provision :chef_solo do |chef|
    chef.json = {
      "mysql" => { "server_root_password" => "" }
    }
    chef.add_recipe "apt"
#    chef.add_recipe "build-essential"
    chef.add_recipe "git"
    chef.add_recipe "apache2"
    chef.add_recipe "apache2::mod_php5"
    chef.add_recipe "mysql"
    chef.add_recipe "mysql::server"
    chef.add_recipe "php"
    chef.add_recipe "php::module_mysql"
    chef.add_recipe "phing"
  end
end
