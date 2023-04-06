# tcptools

## Using Ping
## What were the min/avg/max/stddev stats for each?
### Amazon
* Ping 1: round-trip min/avg/max/stddev = 21.168/27.473/36.245/4.070 ms over 9 packets
* Ping 2: round-trip min/avg/max/stddev = 21.570/25.877/28.713/2.926 ms over 6 packets
* Ping 3: round-trip min/avg/max/stddev = 21.252/26.370/27.949/2.112 ms over 7 packets

### Google 
* Ping 1: round-trip min/avg/max/stddev = 4.308/9.120/15.620/3.872 ms over 5 packets
* Ping 2: round-trip min/avg/max/stddev = 3.383/8.187/9.281/2.154 ms over 6 packets 
* Ping 3: round-trip min/avg/max/stddev = 4.464/8.104/11.738/2.939 ms over 6 packets

### Microsoft
* Ping 1: round-trip min/avg/max/stddev = 21.317/25.781/32.454/3.854 ms over 6 packets
* Ping 2: round-trip min/avg/max/stddev = 20.560/25.153/29.219/3.176 ms over 6 packets
* Ping 3: round-trip min/avg/max/stddev = 20.749/26.752/28.815/2.551 ms over 7 packets

## Was there any packet loss over the pings?
There was 0 total packets lost - I must have a pretty reliable connection to all three of their servers.

## Did the IP address of a site change between Pings?
There was no change observed to the IP address between each ping for all three websites.

## Using traceroute
## What was the target server's IP address?
### Amazon
18.164.158.208

### Google 
142.251.211.228
### Microsoft 
23.33.17.164
## How many hops were needed to reach the target?
### Amazon
This was a strange case where 44 hops took place and then there was a very long pause. I'm not sure why this is the case, as I'm pretty sure this is an unusually large ammount of hops, especially compared to the other traceroutes done.
### Google
12 hops total
### Microsoft 
16 hops total
## Can you identify your ISP from intermediate server DNS names?
Yes, from all of these traceroutes it is clear that I am using comcast as my ISP, as their domains are most of the intermediate hops.
## Identify the "Class" of IP address from each major step in the trip 
### Amazon
Destination: 18.164.158.208 is class A
Origin: 192.168.1.1 is class C
First hop to comcast domain: 69.139.164.134 is also class A. All these comcast jumps are unsurprsingly class A.
### Google
Destination: 142.251.211.228 is class B - somewhat surprising that Amazon has class A but not Google.
Origin: 192.168.1.1 is class C
Last hop before destination: 216.239.43.231 which is a class C.
### Microsoft 
Destination: 23.33.17.164 is a class A
Origin: 192.168.1.1 is class C
Last hop before destination: 23.33.17.164 which is eploy.static.akamaitechnologies.com. A class A that I have not heard of.

## Extra credit: Using packet-capture tools (2 pts)
From this exercise I found a DHCP lease time for 90 days on a Mac device (I believe my laptop as I switched onto the network).
