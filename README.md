Collection of bash scripts created while migrating 
[Axway](http://www.axway.fr/) [Gateway](http://www.axway.fr/produits-solutions/mft/gateways/gateway) 6.11 
to Gateway 6.14 + [SecureRelay](http://www.axway.fr/produits-solutions/mft/gateways/dmz-security)

## Export / import of Gateway objects

``` bash
# Export all objects (pel, sec & vfd)
$ expimp_objects
# Export only pel objects
$ expimp_objects pel
# Export security & VFD objects (vfd exports are made by creating the vfdadm create commands for the directories, NOT by vfdbase)
$ expimp_objects sec vfd
```

## Install automatically the gateway

### Pre requisites

Make an install (or use an existing one) to get the following configuration files:
- dconf.save
- pelsetup.def
- pelsetup.ini
- silentFiles/Synchrony.*

Update the environments variables (site alias name, IP addresses, ports, etc)

``` bash
$ ./install_auto
```