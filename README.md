\# nmcli c m enp2s0 +ipv4.routes "192.168.40.0/24 192.168.24.239"<br>
\# nmcli c m enp2s0 +ipv4.routes "192.168.50.0/24 192.168.24.230"<br>
\# netstat -ner<br>
Kernel IP routing table<br>
Destination     Gateway         Genmask         Flags Metric Ref    Use Iface<br>
0.0.0.0         192.168.24.1    0.0.0.0         UG    100    0        0 enp2s0<br>
192.168.24.0    0.0.0.0         255.255.255.0   U     100    0        0 enp2s0<br>

\# cat /etc/sysconfig/network-scripts/route-enp2s0 <br>
ADDRESS0=192.168.40.0<br>
NETMASK0=255.255.255.0<br>
GATEWAY0=192.168.24.239<br>
ADDRESS1=192.168.50.0<br>
NETMASK1=255.255.255.0<br>
GATEWAY1=192.168.24.230<br>

\# systemctl restart network<br>
\# netstat -nr<br>
Kernel IP routing table<br>
Destination     Gateway         Genmask         Flags   MSS Window  irtt Iface<br>
0.0.0.0         192.168.24.1    0.0.0.0         UG        0 0          0 enp2s0<br>
192.168.24.0    0.0.0.0         255.255.255.0   U         0 0          0 enp2s0<br>
192.168.40.0    192.168.24.239  255.255.255.0   UG        0 0          0 enp2s0<br>
192.168.50.0    192.168.24.230  255.255.255.0   UG        0 0          0 enp2s0<br>

\# nmcli c m enp2s0 -ipv4.routes "192.168.40.0/24 192.168.24.239"<br>

\# cat /etc/sysconfig/network-scripts/route-enp2s0 <br>
ADDRESS0=192.168.50.0<br>
NETMASK0=255.255.255.0<br>
GATEWAY0=192.168.24.230<br>

\# systemctl restart network<br>
\# netstat -nr<br>
Kernel IP routing table<br>
Destination     Gateway         Genmask         Flags   MSS Window  irtt Iface<br>
0.0.0.0         192.168.24.1    0.0.0.0         UG        0 0          0 enp2s0<br>
192.168.24.0    0.0.0.0         255.255.255.0   U         0 0          0 enp2s0<br>
192.168.50.0    192.168.24.230  255.255.255.0   UG        0 0          0 enp2s0<br>


\# nmcli c m enp2s0 +ipv4.routes "192.168.40.0/24 192.168.24.239"<br>

\# nmcli -f ipv4.routes c s enp2s0<br>
ipv4.routes:                            { ip = 192.168.50.0/24, nh = 192.168.24.230 }; { ip = 192.168.40.0/24, nh = 19<br>
