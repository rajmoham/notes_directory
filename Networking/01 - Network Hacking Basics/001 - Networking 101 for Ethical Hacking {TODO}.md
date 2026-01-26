When sending requests (for example [[Requesting a URL]]), certain information is required to know where to fetch the data, and who to give it to.
To identify the person who gave the initial request, we need the MAC address and the IP address.

MAC address tells you the device within a network which requested the information.
IP address tells you the network from which the the device is contained within and where the request came from.

MAC address does not change and is hard-coded. However, the public IP address you have constantly changes. The private IP address is linked to the device giving the request and can change also as devices connect and disconnect within the network.

DHCP server automatically assigns an private IP address to devices within a local network. You can make certain devices have a static IP so this does not change.


NAT
Subnets
IPv6 -> does not need NAT, SLAAC