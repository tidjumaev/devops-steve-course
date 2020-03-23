# Firewalld

Firewalld is Linux firewall management tool with support for IPv4, IPv6, Ethernet bridges and IPSet firewall settings. It acts as a front-end to Linux kernel’s netfilter framework. Firewalld is a default firewall management software on RHEL 7 family.

## Zones in Firewalld

Zones -are sets of rules dictating what traffic should be allowed depending on the level of trust.

Install Firewalld on Ubuntu 18.04 / Ubuntu 16.04 by running the commands:

```text
sudo apt-get install firewalld
```

By default, the service should be started, if not running, start and enable it to start on boot:

```text
sudo systemctl enable firewalld
sudo systemctl start firewalld
```

Confirm that the service is running:

```text
$ sudo firewall-cmd --state
running
```

If you have ufw enabled, disable it to make firewalld your default firewall

```text
sudo ufw disable
```

### Using Firewalld on Ubuntu 18.04 / Ubuntu 16.04

Now that the package has been installed and firewalld service started, let’ look at few usage examples

See below examples for the basic usage of firewalld.

#### `1.` List all firewall rules configured

```text
# firewall-cmd --list-all
public
  target: default
  icmp-block-inversion: no
  interfaces: 
  sources: 
  services: ssh dhcpv6-client
  ports: 
  protocols: 
  masquerade: no
  forward-ports: 
  source-ports: 
  icmp-blocks: 
  rich rules:
```

`ssh` and `dhcpv6-client` services are enabled by default when you start firewalld service.

#### `2.` Get a list of all services that can be enabled using a name

```text
sudo firewall-cmd --get-services
```

#### `3.` Enable `http` service

```text
sudo firewall-cmd --add-service=http --permanent
```

The `--permanent` option means persist rules against server reboots.

#### `4.` Enable both http and https on a single line

```text
sudo firewall-cmd --permanent --add-service={http,https} --permanent
```

#### `5.` Enable TCP port 7070

```text
sudo firewall-cmd --add-port=7070/tcp --permanent
```

#### `6.` Enable UDP port 514

```text
sudo firewall-cmd --add-port=514/udp --permanent
```

#### `7.` Create a new zone

```text
sudo firewall-cmd --new-zone=myzone --permanent
```

#### `8.` Enable service on a specific zone

```text
sudo firewall-cmd --zone=myzone --add-port=4567/tcp --permanent
```

#### `9.` Set default zone

```text
sudo firewall-cmd --set-default-zone=public --permanent
```

#### `10.` Add an interface to a zone

```text
sudo firewall-cmd --get-zone-of-interface=eth0 --permanent
sudo firewall-cmd --zone=<zone> --add-interface=eth0 --permanent
```

#### `11.` Allow access to a port from specific subnet/IP

```text
$ sudo firewall-cmd --add-rich-rule 'rule family="ipv4" service name="ssh" \
source address="192.168.0.12/32" accept' --permanent
$ sudo firewall-cmd --add-rich-rule 'rule family="ipv4" service name="ssh" \
source address="10.1.1.0apt /24" accept' --permanent
```

#### `12.` List rich rules

```text
sudo firewall-cmd --list-rich-rules
```

#### `13.` Configure Port forwarding

```text
# Enable masquerading
$ sudo firewall-cmd --add-masquerade --permanent

# Port forward to a different port within same server ( 22 > 2022)
$ sudo firewall-cmd --add-forward-port=port=22:proto=tcp:toport=2022 --permanent

# Port forward to same port on a different server (local:22 > 192.168.2.10:22)
$ sudo firewall-cmd --add-forward-port=port=22:proto=tcp:toaddr=192.168.2.10 --permanent

# Port forward to different port on a different server (local:7071 > 10.50.142.37:9071)
$ sudo firewall-cmd --add-forward-port=port=7071:proto=tcp:toport=9071:toaddr=10.50.142.37 --permanent
```

#### `14.` Removing port/service

Replace `--add` with `–-remove`

[https://youtu.be/7lAdXHMfVjs](https://youtu.be/7lAdXHMfVjs)

