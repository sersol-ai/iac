- Disk format

```
/disk format usb1 file-system=ext4 mbr-partition-table=no
```

- Create necessary directories on your RouterOS device

```
/file add name=usb1/configs type=directory
/file add name=usb1/traefik type=directory
/file add name=usb1/docker/traefik type=directory  
/file add name=usb1/docker/mpm type=directory
```

- Download Traefik Configuration

```
/tool fetch url="https://raw.githubusercontent.com/akmalovaa/mikrotik-proxy-manager/refs/heads/main/traefik/traefik.yml" mode=https dst-path="usb1/traefik/traefik.yml"
```
