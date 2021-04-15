

[global]<br>
	server string = Samba Server<br>
	security = share<br>
	#passdb backend = tdbsam<br>
	log level = 2<br>
	log file = /var/log/samba/%m.log<br>
	max log size = 500<br>
	max protocol = SMB2<br>
	unix extensions = no<br>
	client signing = required<br>
	socket options = TCP_NODELAY SO_RCVBUF=14140000 SO_SNDBUF=14140000<br>
	load printers = no<br>
	printing = bsd<br>
	printcap name = /dev/null<br>
	dns proxy = No<br>
	idmap config * : backend = tdb<br>
	create mask = 0755<br>
	directory mask = 0755<br>
	cups options = raw<br>
	hide special files = Yes<br>
	veto files = /.*<br>
	browseable = No<br>
	wide links = Yes<br>
	vfs objects = shadow_copy<br>
	client NTLMv2 auth = Yes<br>

[share]<br>
	path = /home/share<br>
	username = user<br>
	read only = No<br>
	only user = Yes<br>
