# MMGenLive 

MMGenLive is a fully functional Linux system on a USB stick with the [MMGen
online/offline Bitcoin wallet][6], Bitcoin Core and related programs preinstalled.

MMGenLive gives you, out of the box:

* A completely installed, upgradeable and configurable Ubuntu Linux system
* The MMGen wallet system and documentation, also upgradeable
* The latest Bitcoin Core
* Automated scripts that make setting up and running your node easy
* Full disk encryption (entire filesystem is read/write)
* Full Tor support for both running the node and upgrading the system

MMGenLive can be used as both an **offline signing wallet** and an **online
tracking/transacting wallet** with a full or pruned blockchain.

***MMGenLive is also an easy way to set up and run a full node, whether you
choose to use the MMGen wallet or not.***

### There are two ways to install and run MMGenLive:

* download a prebuilt bootable image (the preferred method); or
* build the bootable image yourself using the automated shell script (Linux only).

## To run MMGenLive from a prebuilt bootable image:
* Download the latest zipped boot image file for your architecture from the
  [bootimages download directory][3].
* Insert a blank USB stick into your computer.

> ### If you’re running Linux:

> * Determine your USB stick’s device name.  This can be done with the command
> `dmesg` or `lsblk`.  Copy the image to the USB stick using the command
> `zcat *.img.tgz >/dev/sdX`, replacing `sdX` with your USB stick’s device name.

> ### If you’re running Windows:

> * Unzip the boot image file using an archiving program such as WinRAR.
>   Download the disk image-copying program [Win32DiskImager][7] from its
>   project page on SourceForge.  Make a note of your USB stick’s drive letter.
>   Open the Win32DiskImager archive in your archiving program and launch it
>   straight from the archive; it doesn't require installation.  Drag and drop
>   the *unzipped* boot image into Win32DiskImager's “Image File” box, select
>   the drive letter of your USB stick in the “Device” box and click “Write”.

* When the copying operation has completed, shut down your computer and reboot
  from the USB stick.  You may have to enter your BIOS boot menu to do this.
  During the boot process, you’ll be prompted to unlock the disk.  Enter the
  password `mmgen`.  After the graphical interface appears, follow the
  instructions on the terminal screen.

## To build the MMGenLive USB image using the automated shell script (Linux only):

* Clone the mmgen and MMGenLive repositories:

			git clone https://github.com/mmgen/mmgen.git
			cd mmgen && git checkout -b mm stable_linux
			cd ..
			git clone https://github.com/mmgen/MMGenLive.git
			cd MMGenLive && git checkout -b mm stable

* Download the [latest extras files][2] and place them in the MMGenLive
  repository root.

* Build and install the MMGenLive system:

			sudo ./build_system.sh

### Upgrading your installation:

To avoid the need to download new boot images as improvements are made and
features added to MMGenLive, a **revision and upgrade system** was introduced
with version 0.0.7.  To bring your system up-to-date with the latest revisions,
type 'mmlive-upgrade' from within your running MMGenLive installation.  A list
of the latest revisions may be found in the **[ChangeLog][9].**

For more detailed information, see the **[MMGenLive internal documentation][8].**

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

[**Forum**][4] |
[Reddit][0] |
[PGP Public Key][5] |
Donate: 15TLdmi5NYLdqmtCqczUs5pBPkJDXRs83w

[0]: https://www.reddit.com/user/mmgen-py
[1]: https://www.raspberrypi.org/documentation/installation/installing-images/windows.md
[2]: https://github.com/mmgen/MMGenLive/releases/tag/extras-v0.0.7
[3]: https://github.com/mmgen/MMGenLive/releases/tag/bootimage-v0.0.7
[4]: https://bitcointalk.org/index.php?topic=567069.0
[5]: https://github.com/mmgen/mmgen/wiki/MMGen-Signing-Key
[6]: https://github.com/mmgen/mmgen/
[7]: https://sourceforge.net/projects/win32diskimager/
[8]: https://github.com/mmgen/MMGenLive/wiki/MMGenLive-internal-documentation
[9]: https://github.com/mmgen/MMGenLive/blob/master/ChangeLog.md
