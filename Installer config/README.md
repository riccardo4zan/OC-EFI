# Installer

Grab the EFI folder and substitute the file on EFI/OC with the one in this folder.
This plist file has debug mode enabled, making easy to solve problems if stuck at boot.

## Making the installer in Linux
Guide: https://dortania.github.io/OpenCore-Install-Guide/installer-guide/linux-install.html#method-1

In order to make the installer you have to use the tool GibMacOS(https://github.com/corpnewt/gibMacOS), and then preparing the USB as the guide states.

```shell
lsblk
```
To list all storage devices

```shell
sudo gdisk /dev/<USB device> (not partition)
```
Then send: 
* p (to print all usb device blocks)
* o (to clear partition table and make a new GPT one) -> y (to confirm)
* n (leave partition number, first sector, last sector blank, and set Hex code or GUID : 0700 for Microsoft basic data partition type)
* w (to write modifications) -> y (to confirm)

Ad this point gdisk should quit on its own.

### Unmount USB partitions from the File System and then:

```shell
lsblk
```
To list all storage devices

```shell
sudo mkfs.vfat -F 32 -n "OPENCORE" /dev/<USB partition block>
```

Then follow the guide
________________________________________________________________________________________________________________________________________________________

## Post Install
Link to the documentation: https://dortania.github.io/OpenCore-Post-Install/#how-to-follow-this-guide

### Boot without USB installer
In order to be able to boot Catalina whitout the installation media you have to copy the EFI folder in the EFI partition of the installation drive.

Select ONE of the EFI folders, download it and rename it to 'EFI'.

#### Link to the guide (Uses a tool)
Guide: https://dortania.github.io/OpenCore-Post-Install/universal/oc2hdd.html#grabbing-opencore-off-the-usb

#### DIY
When you are in OS X use

```shell
diskutil list 
```

This command will list all storage devices attached to the system.

```shell
sudo diskutil mount disk?s?
```

This command will be used to mount the EFI partition of the boot drive.
The '?' must be substituted with numbers associated to the boot drive, recognizable in the output of the first command.

At this point you can copy the EFI folder inside the partition you mount. The name of the folder must be EFI (so if you downloaded 'EFI-Stable' rename it to 'EFI')

And then you can unmount

```shell
diskutil unmount disk?s?
```
