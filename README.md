Vagrant LAMP
============

This repository has the configuration and all the cookbooks needed to setup a
simple LAMP server using [Vagrant](http://vagrantup.com).

If you use this repository, you will end up with a Linux server that has the
following packages:

* Apache
* MySQL
* PHP
* Git (client)
* Phing
* PHP-Unit

Usage
-----

```
$ git clone https://github.com/elachys/vagrant-lamp.git project
$ cd project
$ vagrant box add precise64 http://files.vagrantup.com/precise64.box
$ vagrant up
```

You can skip the 3rd step if you already have done it. If you didn't name your
Linux image as `lucid32` you will have to modify the corresponding line in
`Vagrantfile`, for example:

```
config.vm.box = "my-custom-name"
```

Credits
-------

This is forked from: https://github.com/egrajeda/vagrant-lamp

All the Chef recipes are taken from [Opscode public cookbooks repository](http://github.com/opscode/cookbooks),
I just put them in one place, modified some neccesary bits and packaged them
in a single repository.

