\# rpm -qa | grep samba<br>
samba-winbind-3.6.23-53.el6_10.x86_64<br>
samba-3.6.23-53.el6_10.x86_64<br>
samba4-libs-4.2.10-15.el6.x86_64<br>
samba-winbind-clients-3.6.23-53.el6_10.x86_64<br>
samba-client-3.6.23-53.el6_10.x86_64<br>
samba-common-3.6.23-53.el6_10.x86_64<br>

\# yum downgrade samba-3.5.10-125.el6.x86_64 samba-client-3.5.10-125.el6.x86_64 samba-common-3.5.10-125.el6.x86_64 samba-winbind-3.5.10-125.el6.x86_64 samba-winbind-clients-3.5.10-125.el6.x86_64<br>
Loaded plugins: product-id, search-disabled-repos, security, subscription-manager<br>
Setting up Downgrade Process<br>
Resolving Dependencies<br>
--> Running transaction check<br>
---> Package samba.x86_64 0:3.5.10-125.el6 will be a downgrade<br>
---> Package samba.x86_64 0:3.6.23-53.el6_10 will be erased<br>
---> Package samba-client.x86_64 0:3.5.10-125.el6 will be a downgrade<br>
---> Package samba-client.x86_64 0:3.6.23-53.el6_10 will be erased<br>
---> Package samba-common.x86_64 0:3.5.10-125.el6 will be a downgrade<br>
---> Package samba-common.x86_64 0:3.6.23-53.el6_10 will be erased<br>
---> Package samba-winbind.x86_64 0:3.5.10-125.el6 will be a downgrade<br>
---> Package samba-winbind.x86_64 0:3.6.23-53.el6_10 will be erased<br>
---> Package samba-winbind-clients.x86_64 0:3.5.10-125.el6 will be a downgrade<br>
---> Package samba-winbind-clients.x86_64 0:3.6.23-53.el6_10 will be erased<br>
--> Finished Dependency Resolution<br>

Dependencies Resolved<br>

=============================================================================================================================================<br>
 Package                                Arch                    Version                            Repository                           Size<br>
=============================================================================================================================================<br>
Downgrading:<br>
 samba                                  x86_64                  3.5.10-125.el6                     rhel-6-server-rpms                  5.0 M<br>
 samba-client                           x86_64                  3.5.10-125.el6                     rhel-6-server-rpms                   11 M<br>
 samba-common                           x86_64                  3.5.10-125.el6                     rhel-6-server-rpms                   13 M<br>
 samba-winbind                          x86_64                  3.5.10-125.el6                     rhel-6-server-rpms                  3.5 M<br>
 samba-winbind-clients                  x86_64                  3.5.10-125.el6                     rhel-6-server-rpms                  1.1 M<br>

Transaction Summary<br>
=============================================================================================================================================<br>
Downgrade     5 Package(s)<br>

Total download size: 34 M<br>
Is this ok [y/N]: y<br>
Downloading Packages:<br>
(1/5): samba-3.5.10-125.el6.x86_64.rpm                                                                                | 5.0 MB     00:00<br>     
(2/5): samba-client-3.5.10-125.el6.x86_64.rpm                                                                         |  11 MB     00:01<br>     
(3/5): samba-common-3.5.10-125.el6.x86_64.rpm                                                                         |  13 MB     00:01<br>     
(4/5): samba-winbind-3.5.10-125.el6.x86_64.rpm                                                                        | 3.5 MB     00:00<br>     
(5/5): samba-winbind-clients-3.5.10-125.el6.x86_64.rpm                                                                | 1.1 MB     00:00<br>     
---------------------------------------------------------------------------------------------------------------------------------------------<br>
Total                                                                                                        5.3 MB/s |  34 MB     00:06<br>     
Running rpm_check_debug<br>
Running Transaction Test<br>
Transaction Test Succeeded<br>
Running Transaction<br>
  Installing : samba-winbind-clients-3.5.10-125.el6.x86_64                                                                              1/10 <br>
  Installing : samba-common-3.5.10-125.el6.x86_64                                                                                       2/10 <br>
  Installing : samba-client-3.5.10-125.el6.x86_64                                                                                       3/10 <br>
  Installing : samba-3.5.10-125.el6.x86_64                                                                                              4/10 <br>
  Installing : samba-winbind-3.5.10-125.el6.x86_64                                                                                      5/10 <br>
  Cleanup    : samba-3.6.23-53.el6_10.x86_64                                                                                            6/10 <br>
  Cleanup    : samba-client-3.6.23-53.el6_10.x86_64                                                                                     7/10 <br>
  Cleanup    : samba-common-3.6.23-53.el6_10.x86_64                                                                                     8/10 <br>
  Cleanup    : samba-winbind-3.6.23-53.el6_10.x86_64                                                                                    9/10<br> 
  Cleanup    : samba-winbind-clients-3.6.23-53.el6_10.x86_64                                                                           10/10 <br>
  Verifying  : samba-client-3.5.10-125.el6.x86_64                                                                                       1/10 <br>
  Verifying  : samba-winbind-clients-3.5.10-125.el6.x86_64                                                                              2/10<br> 
  Verifying  : samba-common-3.5.10-125.el6.x86_64                                                                                       3/10 <br>
  Verifying  : samba-3.5.10-125.el6.x86_64                                                                                              4/10<br> 
  Verifying  : samba-winbind-3.5.10-125.el6.x86_64                                                                                      5/10 <br>
  Verifying  : samba-3.6.23-53.el6_10.x86_64                                                                                            6/10 <br>
  Verifying  : samba-common-3.6.23-53.el6_10.x86_64                                                                                     7/10<br> 
  Verifying  : samba-winbind-3.6.23-53.el6_10.x86_64                                                                                    8/10 <br>
  Verifying  : samba-winbind-clients-3.6.23-53.el6_10.x86_64                                                                            9/10<br> 
  Verifying  : samba-client-3.6.23-53.el6_10.x86_64                                                                                    10/10 <br>

Removed:<br>
  samba.x86_64 0:3.6.23-53.el6_10             samba-client.x86_64 0:3.6.23-53.el6_10              samba-common.x86_64 0:3.6.23-53.el6_10<br>  
  samba-winbind.x86_64 0:3.6.23-53.el6_10     samba-winbind-clients.x86_64 0:3.6.23-53.el6_10 <br>   

Installed:<br>
  samba.x86_64 0:3.5.10-125.el6               samba-client.x86_64 0:3.5.10-125.el6                samba-common.x86_64 0:3.5.10-125.el6<br>      
  samba-winbind.x86_64 0:3.5.10-125.el6       samba-winbind-clients.x86_64 0:3.5.10-125.el6 <br>     

Complete!<br>


\# rpm -qa | grep samba<br>
samba-winbind-clients-3.5.10-125.el6.x86_64<br>
samba-client-3.5.10-125.el6.x86_64<br>
samba4-libs-4.2.10-15.el6.x86_64<br>
samba-3.5.10-125.el6.x86_64
samba-winbind-3.5.10-125.el6.x86_64<br>
samba-common-3.5.10-125.el6.x86_64<br>


\# yumdownloader samba-3.5.10-125.el6.x86_64 samba-client-3.5.10-125.el6.x86_64 samba-common-3.5.10-125.el6.x86_64 samba-winbind-3.5.10-125.el6.x86_64 samba-winbind-clients-3.5.10-125.el6.x86_64<br>

\# yum update samba samba-client<br>

\# rpm -qa | grep samba<br>
samba-3.6.23-53.el6_10.x86_64<br>
samba-winbind-clients-3.6.23-53.el6_10.x86_64<br>
samba-common-3.6.23-53.el6_10.x86_64<br>
samba4-libs-4.2.10-15.el6.x86_64<br>
samba-winbind-3.6.23-53.el6_10.x86_64<br>
samba-client-3.6.23-53.el6_10.x86_64<br>

\# rpm -Uvh --oldpackage samba-3.5.10-125.el6.x86_64.rpm samba-client-3.5.10-125.el6.x86_64.rpm samba-common-3.5.10-125.el6.x86_64.rpm samba-winbind-3.5.10-125.el6.x86_64.rpm samba-winbind-clients-3.5.10-125.el6.x86_64.rpm<br>
Preparing...                ########################################### [100%]<br>
   1:samba-winbind-clients  ########################################### [ 20%]<br>
   2:samba-common           ########################################### [ 40%]<br>
   3:samba                  ########################################### [ 60%]<br>
   4:samba-client           ########################################### [ 80%]<br>
   5:samba-winbind          ########################################### [100%]<br>

\d# rpm -qa | grep samba<br>
samba-client-3.5.10-125.el6.x86_64<br>
samba-winbind-clients-3.5.10-125.el6.x86_64<br>
samba-winbind-3.5.10-125.el6.x86_64<br>
samba4-libs-4.2.10-15.el6.x86_64<br>
samba-common-3.5.10-125.el6.x86_64<br>
samba-3.5.10-125.el6.x86_64<br>
