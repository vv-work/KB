# Net settings

-[oficial documenation](https://ubuntu.com/server/docs/network-configuration)

## Static ip

`/etc/netplan/99_config.yaml`

```bash
network:
  version: 2
  renderer: networkd
  ethernets:
    enp3s0:
      dhcp4: false
      addresses: [192.168.1.100/24]
      nameservers:
        addresses: [192.168.1.1,8.8.8.8]
      routes:
        - to: default
          via: 192.168.1.1
```
`sudo netplan apply`

`cat file.txt` - see incide file
`echo "some command" >>file.txt` - Write To file
`wget`
`w3m`
`Feh`
`Fim`

- [Article on installing desktop slim way](https://phoenixnap.com/kb/how-to-install-a-gui-on-ubuntu)


## Awesome 

- I3M tilling for ubuntu

`startx`
`i3`
`xinit`
