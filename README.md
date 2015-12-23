# PowerDNS-Authoritative-cacti-templates
URL:http://forums.cacti.net/viewtopic.php?t=37716<br>
<br>
====
<br>
## Requirement<br>
OS:CentOS6<br>
Package:cacti-0.8.8b-7.el6.noarch<br>
pdns-3.3.3-1.el6.x86_64<br>
net-snmp-5.5-54.el6_7.1.x86_64<br>
net-snmp-libs-5.5-54.el6_7.1.x86_64<br>
net-snmp-utils-5.5-54.el6_7.1.x86_64<br>
<br>
## Install<br>
-- edit snmpd.conf<br>
$ cat snmpd.conf.add >> /etc/snmp/snmpd.conf<br>
<br>
-- check example<br>
$ cat /etc/snmp/snmpd.conf|grep pdns-auth<br>
extend .1.3.6.1.4.1.18689.0.7 pdns-auth /usr/local/bin/pdnsauth-stats<br>
<br>
-- copy pdnsauth-stats<br>
$ cp pdnsauth-stats /usr/local/bin/<br>
$ chmod 755 /usr/local/bin/pdnsauth-stats<br>
<br>
-- check example<br>
$ /usr/local/bin/pdnsauth-stats<br>
0<br>
0<br>
0<br>
0<br>
751<br>
80<br>
0<br>
0<br>
124<br>
208<br>
0<br>
0<br>
0<br>
0<br>
0<br>
0<br>
0<br>
1372<br>
1372<br>
1372<br>
1372<br>
0<br>
0<br>
<br>
<br>
## Notes



