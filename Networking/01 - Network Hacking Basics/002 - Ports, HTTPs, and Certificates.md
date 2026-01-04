# Ports
For a hacker to gain access to another device, they need to get through a port. It is not enough to just know the IP Address.

>Analogy: robbers can know someone's address but for access they need to get through a door. 

- There are 65,535 possible port numbers, with certain ports pre-dedicated for certain functions
### Ephemeral Port
If you are connecting to some service online like Google, you also expect information to be received back. This does not happen through the same port, but rather through Ephemeral ports.

1. The computer picks a random high number port to use as the ephemeral port.
2. Receives information through that port.
3. Instantly closes the connection of that port once data has been received.
The entire process takes split seconds to finish.

```
netstat                  # Shows listening and established connections
```

<img src="https://upload.wikimedia.org/wikipedia/commons/9/9f/Netstat_screenshot.png">

- Listening - the port is waiting for connection to be made and data to be received
- Established - a connection has been made for data to be received

#  Certificates
When users connect to the internet and are [[Requesting a URL]], the DNS system looks up the IP address for the user. However this may not always be good and safe.
- `/etc/hosts` contains cached data of IP addresses which the computer might use instead of going to a DNS system because it is quicker. However, someone can maliciously enters a field for a popular website to the IP address of a website they made.
- DNS Spoofing -> similar to the above, the hack may be directly on the DNS system to replace the IP address

Browsers check whether a website is actually the real website by checking the certificates (this is like checking someone's ID).

# Resources
https://www.speedguide.net/ports.php
https://www.exploit-db.com/