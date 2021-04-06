
\# /etc/rc.d/init.d/network restart<br>
Shutting down interface eth0:                              [  OK  ]<br>
Shutting down loopback interface:                          [  OK  ]<br>
Bringing up loopback interface:                            [  OK  ]<br>
Bringing up interface eth0:  Determining if ip address 192.168.24.240 is already in use for device eth0...<br>
                                                           [  OK  ]<br>
\# ip route show cache | grep 192.168.40.10<br>
\# traceroute -I 192.168.40.10<br>
traceroute to 192.168.40.10 (192.168.40.10), 30 hops max, 60 byte packets<br>
 1  192.168.24.1 (192.168.24.1)  0.308 ms  0.453 ms  0.577 ms<br>
 2  192.168.24.239 (192.168.24.239)  0.650 ms  0.651 ms  0.652 ms<br>
 3  192.168.40.10 (192.168.40.10)  1.474 ms  1.476 ms  1.729 ms<br>
\# ip route show cache | grep 192.168.40.10<br>
192.168.40.10 via 192.168.24.239 dev eth0  src 192.168.24.240 <br>
local 192.168.24.240 from 192.168.40.10 dev lo  src 192.168.24.240 <br>
192.168.40.10 from 192.168.24.240 via 192.168.24.239 dev eth0 <br>
\# traceroute -I 192.168.40.10<br>
traceroute to 192.168.40.10 (192.168.40.10), 30 hops max, 60 byte packets<br>
 1  192.168.24.239 (192.168.24.239)  0.327 ms  0.322 ms  0.290 ms<br>
 2  192.168.40.10 (192.168.40.10)  1.212 ms  1.214 ms  1.212 ms<br>
\# ip route flush cache<br>
\# ip route show cache | grep 192.168.40.10<br>
\# traceroute -I 192.168.40.10<br>
traceroute to 192.168.40.10 (192.168.40.10), 30 hops max, 60 byte packets<br>
 1  192.168.24.1 (192.168.24.1)  0.337 ms  0.475 ms  0.598 ms<br>
 2  192.168.24.239 (192.168.24.239)  0.649 ms  0.650 ms  0.649 ms<br>
 3  192.168.40.10 (192.168.40.10)  1.540 ms  1.543 ms  1.542 ms<br>
