## Mount disk proxmox

To mount a disk in any linux distribution including proxmox you need to execute the following command:
``` bash
fdisk -l

Disque /dev/sdb : 32 GiB, 34359738368 octets, 67108864 secteurs
Modèle de disque : QEMU HARDDISK   
Unités : secteur de 1 × 512 = 512 octets
Taille de secteur (logique / physique) : 512 octets / 512 octets
taille d'E/S (minimale / optimale) : 512 octets / 512 octets
```
Then you need to create a directory where you will mount the disk:
``` bash
mkdir /mnt/disk
```
Then you need to mount the disk:
``` bash
mount /dev/sdb /mnt/disk
```
If



<div style="width: 100%;"><div style="position: relative; padding-bottom: 70.31%; padding-top: 0; height: 0;"><iframe title="Serveurs" frameborder="0" width="1199" height="843" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://view.genial.ly/63b2b37ad309ae0012bf1832" type="text/html" allowscriptaccess="always" allowfullscreen="true" scrolling="yes" allownetworking="all"></iframe> </div> </div>
