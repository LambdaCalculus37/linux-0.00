# Linux v0.00 Source Code

*(A Historic Look Into Where it All Began!)

**About This Repo**

Here it is. The conception. The beginning. The start. This repo is an effort to archive, mirror, and help preserve the source code for the very, very true first version of Linux ever: version 0.00!

**What To Expect**

Linux 0.00 only did a tiny handful of things: it went into protected mode, started two tasks, and repeated switched between the printing of the strings "AAAA" and "BBBB" over and over.

![Linux 0.00 running in QEMU](linux-000.png "Linux 0.00 running in QEMU)

**Where Did This Come From?**

There's a copy over on [oldlinux.org](http://oldlinux.org/Linux.old/bochs-images/linux-0.00-041217.zip) which I discovered via the Linux 0.00 page on [Gunkies](https://gunkies.org/wiki/Linux_0.00). In the spirit of preservation, I downloaded it and arranged it into this repo, as you never know if and when a website may go under and take everything it has on it with it.

**Repo Layout**

There are two folders of interest in this repo:

1. disk-image - Contains a bootable floppy disk image that's usable in [QEMU](https://www.qemu.org/) (and I also guess [Bochs](https://bochs.sourceforge.io/), although I haven't tested with it). Instructions to run it are below.
2. source - The source code itself, written in x86 assembly. A Makefile is included as well, but I haven't tried to even see if it would build in modern Linux (and it likely won't!)
3. Other files - The files 'bochsrc-hd.bxrc' and 'bootimage-0.00' are (probably?) Bochs related and a boot disk? I haven't tried either out, so if anyone has an idea, let me know!

**A bootable disk image, you say?**

Yes indeed, I do say! This disk image came from the [Gunkies Computer History Wiki page](https://gunkies.org/wiki/Linux_0.00) for Linux 0.00, and I added it to the repo so anyone can quickly and easily run it in an emulator like QEMU or Bochs.

In order to run this in QEMU, simply invoke the following command from the `disk-image` directory:

`qemu-system-i386 -fda Linux-0.00.vfd`

QEMU should start right up and you should see endless strings of "AAAAAAAAAA" and "BBBBBBBBBBB" printing repeatedly.

**License**

As far as I can tell, there is no license attached at all to Linux 0.00. But it's not my call to just attach one. So no license applies here, either.