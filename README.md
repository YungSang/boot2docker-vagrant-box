# boot2docker Vagrant Box

This repository contains the scripts necessary to create a Vagrant-compatible
[boot2docker](https://github.com/boot2docker/boot2docker) box. If you work solely
with Docker, this box lets you keep your Vagrant workflow and work in the
most minimal Docker environment possible.

## Usage

If you just want to use the box, then download the latest box from
the [releases page](https://github.com/YungSang/boot2docker-vagrant-box/releases)
and `vagrant up` as usual! Or, if you don't want to leave your terminal:

    $ vagrant init yungsang/boot2docker
    $ vagrant up
    $ export DOCKER_HOST=tcp://localhost:2375
    $ vagrant ssh
    $ docker version

![Vagrant Up Boot2Docker](https://raw.github.com/YungSang/boot2docker-vagrant-box/master/readme_image.gif)

## Building the Box

If you want to recreate the box, rather than using the binary, then
you can use the Packer template and sources within this repository to
do it in seconds.

To build the box, first install the following prerequisites:

  * [Packer](http://www.packer.io) (at least version 0.5.2, 0.6.1 for Parallels)
  * [VirtualBox](http://www.virtualbox.org)

Then, just run `make`. The resulting box will be named `boot2docker-virtualbox.box` and `boot2docker-parallels.box`.
The entire process to make the box takes about 20 seconds.

## License

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)  
To the extent possible under law, the person who associated CC0 with this work has waived all copyright and related or neighboring rights to this work.

- [boot2docker](http://boot2docker.io/) is under the [Apache 2.0 license](http://www.apache.org/licenses/LICENSE-2.0).
- [Vagrant](http://www.vagrantup.com/): Copyright (c) 2010-2014 Mitchell Hashimoto, under the [MIT License](https://github.com/mitchellh/vagrant/blob/master/LICENSE)
