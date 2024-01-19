---
title: Projects
x-toc-enable: true
...

Endless Projects
================
These projects don't have some end-goal, so I will continue to add ontop of them for as-long as I find it either useful or enjoyable

[Basil Overlay](https://codeberg.org/BasilBasil/basil-overlay)
-------------
I have a Gentoo overlay I'm working on, the main purpose of it is to package my own software, software that either isn't packaged anywhere else, and software that is packaged poorly/missing features in other overlays.

[Etools](https://codeberg.org/BasilBasil/etools)
------
Etools is another Gentoo-centric project I've been working on, It's a bash script that contains a bunch of small applets (kind of like how busybox works) meant to speed up a lot of tasks on Gentoo.

It can help with things such as enabling repositories, listing which package a specific use flag is enabled on, precalculating dependencies for solving update conflicts, providing the time since your last emerge sync in a customizable format, and finding out what cpu flags are enabled by gcc when using `-march=native` so that you can migrate to a distcc setup while keeping all your CPU optimizations enabled.

[util-basil](https://codeberg.org/BasilBasil/util-basil)
----------
util-basil started off as a few standalone utilities that I was writing with the intention of speeding up very small tasks like getting the difference between two dates, counting down, and moving a file to ~/.local/bin/ and marking it as executable.

Nothing in util-basil is anything remarkable, ~~honestly some of the code in there is pretty embarassing~~ but it's just a bunch of stuff I designed to be good enough to get the job done.

Some of the tools in util-basil are required for some of my other programs to work to avoid rewriting the same code multiple times.

[nyaofetch](https://codeberg.org/BasilBasil/nyaofetch)
---------
Nyaofetch is a project I created for fun, it utilizes one of my already-complete projects called boltauthd, the goal of nyaofetch is to have a more featureful UI with the ability to distinguish dGPUs and eGPUs and allow listing a specific GPU using a index in an array.

Most importantly I wanted to implement it such that none of these features made it slower than neofetch so I try to cache information where possible and use more performant ways of fetching information.

Active Projects
===============
Here's a list of my ongoing projects!

[Charon](https://codeberg.org/BasilBasil/Charon)
------
Charon is a project I started a while back, originally with the goal to create a small tool for switching between graphics cards for Vulkan and and OpenGL programs, it quickly expanded because I had to test that it was working and realized that checking the current GPU for multiple APIs at once was annoying.

So I set out to create a neat user interface for viewing the GPU that is in use for every major graphics API.

Now the toolset is comprised on 3 parts: one for listing connected GPUs and GPU kernel modules (asphodel), one for setting the GPU (elysium), and one for displaying what GPU is in use (tartarus).

[sudoas](https://codeberg.org/BasilBasil/sudoas)
------
Sudoas is a project I'm working on on-and-off, it serves as a wrapper for doas to mimick the existence of sudo, with the end-goal of being 1:1 compatible with sudo command line flags (and perhaps even others in the future).

idlebox
-------
Idlebox is one of the larger projects I'm currently working on, the goal is to recreate all of the GNU Coreutils using pure POSIX shell with no external dependencies. (Yes, this includes recreating a bash environment)

I haven't yet gotten the project to a state that I'm happy with, but I plan to share it once it gets to that point!

container manager (name TBD)
----------------------------
This project is currently undergoing a full rewrite, the goal of the program is to make it easy to quickly deploy a container install of any distro with your own customizations, simmilar to how docker works but compatible with multiple tools such as chroot, proot, unshare, newuidmap, newgidmap, and possibly others to make it hopefully as portable as possible.

My hopes are to get it running out of the box on most linux distros both with and without root access.

When the rewrite of the project is done and I'm happy with the level of modularity is has then I'll be sharing this one on codeberg aswell! ^-^

Finished Projects
=================
These are projects that already reached feature-completion.

[boltauthd](https://codeberg.org/BasilBasil/boltauthd)
---------
Boltauthd is a project that I originally created for use with Nyaofetch, with the purpose of tracking when PCIe devices are plugged in to compare them to a list that was cached when the system booted up so that it can correlate a ThunderBolt/USB4 device ID to the PCI ID.

The purpose of distinguishing them was to be able to figure out which PCI display adapters are external and which ones are internal so that I could store external GPUs in a separate array index from internal GPUs to improve the customization of Nyaofetch's output.

I'm really happy with how it turned out in the end, it was certainly a bit janky in the methodology but the results are very consistent even when rapidly hotplugging devices.
