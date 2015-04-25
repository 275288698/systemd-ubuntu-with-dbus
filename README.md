# systemd for ubuntu with dbus enabled

This repo is intented to provide a compilable source for [miraclecast](https://github.com/albfan/miraclecast) systemd dependency on ubuntu

It is based on official git repo on debian

# usage

- clone this repo

- compile

    $ sudo debuild -uc -ux -i -rfakeroot

`sudo` is needed since introspection is needed to compile an it's generated on system paths

 - install all .deb generated

You need to clean this files prior to install

        $ rm /usr/share/doc/libsystemd0/changelog.Debian.gz
        $ rm /usr/share/doc/libudev1/changelog.Debian.gz

        $ sudo dpkg -i *.deb

# Easy install

Install the package compiled with

    $ sudo add-apt-repository ppa:thopiekar/miraclecast
    $ sudo apt-get update
    $ sudo apt-get upgrade
    $ sudo apt-get install miraclecast .

# Original repos

- freedesktop:

  - web: http://www.freedesktop.org/software/systemd/
  - vcs: git://anongit.freedesktop.org/systemd/systemd

- debian

  - web: https://anonscm.debian.org/cgit/pkg-systemd/systemd.git
  - vcs: git://anonscm.debian.org/pkg-systemd/systemd.git

- ubuntu
  - web: https://launchpad.net/ubuntu/+source/systemd/&lt;version&gt;
  - vcs: lp:ubuntu/systemd
