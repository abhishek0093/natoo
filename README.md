# NATOO
Network analysis tool

# Build instructions
```sh
make -j4
```

# Usage
NATOO supports the following features:
* Host discovery
* Port scanning
* OS detection
* Packet sniffing
* ARP poisoning

### Host discovery
In order to scan for host in a subnet, run the following command,

```sh
$ ./natoo -H <subnet>
# example
# ./natoo -H 192.168.1.0/24
```

### Port scanning
Scan ports of an IP address using the following command,

```sh
$ ./natoo -P <ip-addr>
# example
# ./natoo -P 192.168.1.123
```

### OS detection
OS of an IP address can also be detected using the following command

```sh
$ ./natoo -Dp <port> <ip-addr>
# example
# ./natoo -Dp 80 192.168.1.123
```

### Packet sniffing
Inspect incoming packets on a network interface using the following command,

```sh
$ ./natoo -Sn <num-packets> -i <interface>
# example
# ./natoo -Sn 100 -i wlan0
```

### ARP poisoning
ARP poisoning attack can be launched using the following command,

```sh
$ ./natoo -A <gateway-ip> -i <interface> -m <mac-addr>
# example
# ./natoo -A 192.168.1.1 -i wlan0 -m aa:bb:cc:dd:ee:ff
```
