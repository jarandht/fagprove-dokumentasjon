# Proxmox Backup server

## Opprette lagringsområde

**Disk**

Administration > Storage / Disks > ZFS > Create: ZFS
- Standard settings single disk (Grunan VM) 
- Navn store01

**Backup lokasjon**

Datastore > Add Datastore

## Gi tilgong til PVE for å lagre backupar

**Opprett brukar**

Configuration > Acess controll > User management > Add

- User name: su.pve-cl01
- Realm: Proxmox backup authentication

**Gi tilgongar**

Datastore > store01 > Permussions > Add > User permissions

- Path: /Datastore/store01/pve-cl01
- User: su.pve-cl01@pbs
- Role: DatastoreBackup

**Finne cert fingerprint**

Configuration > Certificates

- Velg proxy.pem
- View certificate
- Kopier fingerprint

**Legge til i PVE**

I pve interface > Datacenter (pve-cl01) > Storage > Add > Proxmox Backup Server

- ID: srv-pbs01
- Server: 10.100.0.15
- Username: su.pve-cl01@pbs
- Datastore: store01
- Namepace: pve-cl01
- Fingerprint: XXX

**Aktivere backup task i PVE**

I pve interface > Datacenter (pve-cl01) > Backup > Add > 