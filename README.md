piimg
=====

A utility for working with disk images, which are designed to be flashed onto a Raspberry Pi.

`piimg` is currently untested beyond my own needs, and so I suggest great caution when using it.

Commands
--------

There are 2 useful subcommands; `list` and `mount`. `list` can be run on an image file by running

    piimg list <img-file>

It performs a functionality similar to `fdisk -l` and will list the partitions on the disk.

`mount` is much more cool. It will mount an image files root partition at a given mount point, then mount in the boot partition too. Furthermore, it also bind mounts `/dev` and `/sys`, whilst creating a `/proc`. (How cool is that!?!) It can be run by

    sudo piimg mount <img-file> <mount-point>

At this stage, you must `umount` manually.

Aim
---

The aim is to create a library and command-line utility for manipulating, mounting
and generally working with Raspberry Pi images.

Credits
-------

This project started as a [question on Raspberry Pi.SE](http://raspberrypi.stackexchange.com/q/855/86).
I've also drawn inspiration from the `git` UI.
