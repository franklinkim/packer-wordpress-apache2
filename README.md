# Packer WordPress

> A base box builder for local WordPress development powered by Packer.

## Installation

The built box is hosted on [Atlas](https://atlas.hashicorp.com/franklinkim/boxes/wordpress)

```
$ vagrant box add franklinkim/wordpress-apache2
```

## Usage

Use it with your `Vagrantfile`:

```
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = 'franklinkim/wordpress-apache2'
end
```

## Building

```
$ git clone https://github.com/franklinkim/packer-wordpress.git
$ cd packer-wordpress
$ rake build
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your [changes](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#-git-commit-guidelines) (`git commit -am 'feat: add new feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
Copyright (c) franklin under the MIT license.
