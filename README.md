\# rpm -qa | grep samba<br>
samba-common-3.6.23-53.el6_10.x86_64<br>
samba4-libs-4.2.10-15.el6.x86_64<br>
samba-winbind-3.6.23-53.el6_10.x86_64<br>
samba-3.6.23-53.el6_10.x86_64<br>
samba-client-3.6.23-53.el6_10.x86_64<br>
samba-winbind-clients-3.6.23-53.el6_10.x86_64<br>
----------------------<br>
\# yum remove samba-*<br>

\# rpm -qa | grep samba<br>
samba4-libs-4.2.10-15.el6.x86_64<br>

\# yum install samba4 samba4-client<br>

\# rpm -qa | grep samba<br>
samba4-common-4.2.10-15.el6.x86_64<br>
samba4-4.2.10-15.el6.x86_64<br>
samba4-libs-4.2.10-15.el6.x86_64<br>
samba4-client-4.2.10-15.el6.x86_64<br>

\# testparm <br>
Load smb config files from /etc/samba/smb.conf<br>
rlimit_max: increasing rlimit_max (1024) to minimum Windows limit (16384)<br>
WARNING: Ignoring invalid value 'share' for parameter 'security'<br>
Error loading services.<br>

\# service smb restart<br>
Shutting down SMB services:                                [  OK  ]<br>
Starting SMB services:                                     [FAILED]<br>

