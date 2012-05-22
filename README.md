Collection of bash scripts created while migrating 
[Axway](http://www.axway.fr/) [Gateway](http://www.axway.fr/produits-solutions/mft/gateways/gateway) 6.11 
to Gateway 6.13 (or 6.14) + [SecureRelay](http://www.axway.fr/produits-solutions/mft/gateways/dmz-security)

## expimp_objects: Export / import of Gateway objects

``` bash
# Export all objects (pel, sec & vfd)
$ expimp_objects
# Export only pel objects
$ expimp_objects pel
# Export security & VFD objects (vfd exports are made by creating the vfdadm create commands for the directories, NOT by vfdbase)
$ expimp_objects sec vfd
```

## install_auto: Install automatically the gateway

### Pre requisites

Make an install (or use an existing one) to get the following configuration files:
- dconf.save
- pelsetup.def
- pelsetup.ini
- silentFiles/Synchrony.*

Update the environments variables (site alias name, IP addresses, ports, etc)

``` bash
# Install the gateway, install the patch(s), setup configuration (protocols, etc)
$ ./install_auto
```

## migration_exports: Export all objects into a tar file

``` bash
$ ./migration_exports
```

## migration_import: Import all object from a tar file

``` bash
$ ./migration_import
```

## switch_gateway: Switch from the old gateway to the new one

``` bash
$ ./switch_gateway
```

Stop the gateways
Move the folders as required
Update the ports
Start the gateways