## mptcp-netlink-api-example
* This is an example of the MPTCP Netlink API tested.
* Example to toggle the priorities of two Subflows.
* An action video at the bottom.

<br>

## Environments
#### Server
<pre>
HW
	- Desktop PC (x86)
	- One Ethernet NIC
OS
	- Ubuntu 18.04.x
	- Kernel 4.19.x
	- Mptcp 0.95 (mptcp of multipath-tcp.org)
Package
	- libnl3
</pre>
#### Client
<pre>
HW
	- Raspberry Pi 3 B+ (Arm)
	- Two Ethernet NIC
OS
	- Raspberry Pi OS 2020-05-xx
	- Kernel 4.19.x
	- Mptcp 0.95 (mptcp of multipath-tcp.org)
Package
	- libnl3
	- ifstat (for testing)
</pre>  

<br>

## Caution
* Must be an MPTCP for multipath-tcp.org.
* The mptcp version must be 0.95 or higher
* The client must have at least two NICs.
* The client must complete Routing setup. (See this link : https://multipath-tcp.org/pmwiki.php/Users/ConfigureRouting)
* Servers and clients must not use loopback addresses.

<br>

## Installation Package
<pre>
libnl3 (Must)

$ sudo apt-get install libnl-3-dev libnl-genl-3-dev
</pre>
<pre>
ifstat

$ sudo apt-get install ifstat
</pre>

<br>

## How to installations?
<pre>
$ cd src
$ make
</pre>

<br>

## How to run?
##### in server
<pre>
$ cd src
$ sudo ./mptcp_nl_server [ip_address] [port_number]
</pre>
##### in client
<pre>
$ cd src
$ sudo ./mptcp_nl_client [file_path]
</pre>

<br>

## Video
* Preparing...
