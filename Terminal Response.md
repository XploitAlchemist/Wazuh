(kali㉿kali)-[~]
└─$ curl -sO https://packages.wazuh.com/4.5/wazuh-certs-tool.sh
                                                                                                                                       
┌──(kali㉿kali)-[~]
└─$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos  wazuh-certs-tool.sh
                                                                                                                                       
┌──(kali㉿kali)-[~]
└─$ curl -sO https://packages.wazuh.com/4.5/config.yml
                                                                                                                                       
┌──(kali㉿kali)-[~]
└─$ ls
config.yml  Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos  wazuh-certs-tool.sh
                                                                                                                                        
┌──(kali㉿kali)-[~]
└─$ sudo nano config.yml                                
[sudo] password for kali: 
                                                                                                                                        
┌──(kali㉿kali)-[~]
└─$ bash ./wazuh-certs-tool.sh -A
03/09/2023 16:28:37 INFO: Admin certificates created.
03/09/2023 16:28:38 INFO: Wazuh indexer certificates created.
03/09/2023 16:28:39 INFO: Wazuh server certificates created.
03/09/2023 16:28:40 INFO: Wazuh dashboard certificates created.
                                                                                                                                        
┌──(kali㉿kali)-[~]
└─$ ls
config.yml  Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos  wazuh-certificates  wazuh-certs-tool.sh
                                                                                                                                        
┌──(kali㉿kali)-[~]
└─$ ls
config.yml  Downloads  Public     wazuh-certificates
Desktop     Music      Templates  wazuh-certs-tool.sh
Documents   Pictures   Videos
                                                                    
┌──(kali㉿kali)-[~]
└─$ cd wazuh-certificates                             
                                                                    
┌──(kali㉿kali)-[~/wazuh-certificates]
└─$ ls
admin-key.pem      dashboard.pem   root-ca.key      wazuh-1.pem
admin.pem          node-1-key.pem  root-ca.pem
dashboard-key.pem  node-1.pem      wazuh-1-key.pem
                                                                    
┌──(kali㉿kali)-[~/wazuh-certificates]
└─$ cd ..                
                                                                    
┌──(kali㉿kali)-[~]
└─$ ls
config.yml  Downloads  Public     wazuh-certificates
Desktop     Music      Templates  wazuh-certs-tool.sh
Documents   Pictures   Videos
                                                                    
┌──(kali㉿kali)-[~]
└─$ tar -cvf ./wazuh-certificates.tar -C ./wazuh-certificates/ .
./
./root-ca.key
./wazuh-1.pem
./dashboard.pem
./admin.pem
./wazuh-1-key.pem
./dashboard-key.pem
./node-1.pem
./node-1-key.pem
./root-ca.pem
./admin-key.pem
                                                                    
┌──(kali㉿kali)-[~]
└─$ rm -rf ./wazuh-certificates 
                                                                    
┌──(kali㉿kali)-[~]
└─$ ls
config.yml  Downloads  Public     wazuh-certificates.tar
Desktop     Music      Templates  wazuh-certs-tool.sh
Documents   Pictures   Videos
                                                                    
┌──(kali㉿kali)-[~]
└─$ apt-get install debconf adduser procps
E: Could not open lock file /var/lib/dpkg/lock-frontend - open (13: Permission denied)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), are you root?
                                                                    
┌──(kali㉿kali)-[~]
└─$ sudo apt-get install debconf adduser procps
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
debconf is already the newest version (1.5.82).
adduser is already the newest version (3.137).
procps is already the newest version (2:4.0.3-1).
The following packages were automatically installed and are no longer required:
  debugedit gir1.2-gtksource-3.0 gir1.2-javascriptcoregtk-4.0
  gir1.2-soup-2.4 gir1.2-webkit2-4.0 gobject-introspection
  king-phisher libavfilter8 libavformat59 libblockdev-crypto2
  libblockdev-fs2 libblockdev-loop2 libblockdev-part-err2
  libblockdev-part2 libblockdev-swap2 libblockdev-utils2
  libblockdev2 libcodec2-1.0 libfsverity0 libgdal32 libgeos3.11.1
  libgnuradio-analog3.10.5 libgnuradio-audio3.10.5
  libgnuradio-blocks3.10.5 libgnuradio-channels3.10.5
  libgnuradio-digital3.10.5 libgnuradio-dtv3.10.5
  libgnuradio-fec3.10.5 libgnuradio-fft3.10.5
  libgnuradio-filter3.10.5 libgnuradio-iio3.10.5
  libgnuradio-network3.10.5 libgnuradio-pdu3.10.5
  libgnuradio-pmt3.10.5 libgnuradio-qtgui3.10.5
  libgnuradio-runtime3.10.5 libgnuradio-soapy3.10.5
  libgnuradio-trellis3.10.5 libgnuradio-uhd3.10.5
  libgnuradio-video-sdl3.10.5 libgnuradio-vocoder3.10.5
  libgnuradio-wavelet3.10.5 libgnuradio-zeromq3.10.5
  libgupnp-igd-1.0-4 libhttp-cookiejar-perl liblc3-0
  libmongocrypt0 libmozilla-publicsuffix-perl libmujs2 libncurses5
  libnfs13 libobjc-12-dev libplacebo208 libpostproc56 librpm9
  librpmbuild9 librpmio9 librpmsign9 libsoup-gnome2.4-1
  libspatialite7 libsuperlu5 libswscale6 libtinfo5 libuhd4.3.0
  libvolk2.5 libwebsockets17 libyara9
  linux-image-6.1.0-kali9-amd64 pipewire-alsa pwgen
  python3-advancedhttpserver python3-boltons python3-cairo-dev
  python3-cryptography37 python3-flask-security python3-geoip2
  python3-geojson python3-graphene python3-graphene-sqlalchemy
  python3-graphql-core python3-graphql-relay python3-icalendar
  python3-jaraco.classes python3-maxminddb python3-promise
  python3-pytz-deprecation-shim python3-requests-file
  python3-rule-engine python3-rx python3-smoke-zephyr
  python3-texttable tftp
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
                                                                    
┌──(kali㉿kali)-[~]
└─$ sudo su                                    
┌──(root㉿kali)-[/home/kali]
└─# ls
config.yml  Downloads  Public     wazuh-certificates.tar
Desktop     Music      Templates  wazuh-certs-tool.sh
Documents   Pictures   Videos
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# apt-get install gnupg apt-transport-https
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
gnupg is already the newest version (2.2.40-1.1).
gnupg set to manually installed.
The following packages were automatically installed and are no longer required:
  debugedit gir1.2-gtksource-3.0 gir1.2-javascriptcoregtk-4.0
  gir1.2-soup-2.4 gir1.2-webkit2-4.0 gobject-introspection
  king-phisher libavfilter8 libavformat59 libblockdev-crypto2
  libblockdev-fs2 libblockdev-loop2 libblockdev-part-err2
  libblockdev-part2 libblockdev-swap2 libblockdev-utils2
  libblockdev2 libcodec2-1.0 libfsverity0 libgdal32 libgeos3.11.1
  libgnuradio-analog3.10.5 libgnuradio-audio3.10.5
  libgnuradio-blocks3.10.5 libgnuradio-channels3.10.5
  libgnuradio-digital3.10.5 libgnuradio-dtv3.10.5
  libgnuradio-fec3.10.5 libgnuradio-fft3.10.5
  libgnuradio-filter3.10.5 libgnuradio-iio3.10.5
  libgnuradio-network3.10.5 libgnuradio-pdu3.10.5
  libgnuradio-pmt3.10.5 libgnuradio-qtgui3.10.5
  libgnuradio-runtime3.10.5 libgnuradio-soapy3.10.5
  libgnuradio-trellis3.10.5 libgnuradio-uhd3.10.5
  libgnuradio-video-sdl3.10.5 libgnuradio-vocoder3.10.5
  libgnuradio-wavelet3.10.5 libgnuradio-zeromq3.10.5
  libgupnp-igd-1.0-4 libhttp-cookiejar-perl liblc3-0
  libmongocrypt0 libmozilla-publicsuffix-perl libmujs2 libncurses5
  libnfs13 libobjc-12-dev libplacebo208 libpostproc56 librpm9
  librpmbuild9 librpmio9 librpmsign9 libsoup-gnome2.4-1
  libspatialite7 libsuperlu5 libswscale6 libtinfo5 libuhd4.3.0
  libvolk2.5 libwebsockets17 libyara9
  linux-image-6.1.0-kali9-amd64 pipewire-alsa pwgen
  python3-advancedhttpserver python3-boltons python3-cairo-dev
  python3-cryptography37 python3-flask-security python3-geoip2
  python3-geojson python3-graphene python3-graphene-sqlalchemy
  python3-graphql-core python3-graphql-relay python3-icalendar
  python3-jaraco.classes python3-maxminddb python3-promise
  python3-pytz-deprecation-shim python3-requests-file
  python3-rule-engine python3-rx python3-smoke-zephyr
  python3-texttable tftp
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  apt-transport-https
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 25.7 kB of archives.
After this operation, 36.9 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 apt-transport-https all 2.7.3 [25.7 kB]
Fetched 25.7 kB in 3s (9,989 B/s)        
Selecting previously unselected package apt-transport-https.
(Reading database ... 464279 files and directories currently installed.)
Preparing to unpack .../apt-transport-https_2.7.3_all.deb ...
Unpacking apt-transport-https (2.7.3) ...
Setting up apt-transport-https (2.7.3) ...
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# curl -s https://packages.wazuh.com/key/GPG-KEY-WAZUH | gpg --no-default-keyring --keyring gnupg-ring:/usr/share/keyrings/wazuh.gpg --import && chmod 644 /usr/share/keyrings/wazuh.gpg
gpg: keyring '/usr/share/keyrings/wazuh.gpg' created
gpg: directory '/root/.gnupg' created
gpg: /root/.gnupg/trustdb.gpg: trustdb created
gpg: key 96B3EE5F29111145: public key "Wazuh.com (Wazuh Signing Key) <support@wazuh.com>" imported
gpg: Total number processed: 1
gpg:               imported: 1
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# echo "deb [signed-by=/usr/share/keyrings/wazuh.gpg] https://packages.wazuh.com/4.x/apt/ stable main" | tee -a /etc/apt/sources.list.d/wazuh.list
deb [signed-by=/usr/share/keyrings/wazuh.gpg] https://packages.wazuh.com/4.x/apt/ stable main
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# apt-get update
Get:1 https://packages.wazuh.com/4.x/apt stable InRelease [17.3 kB]
Hit:2 http://kali.cs.nycu.edu.tw/kali kali-rolling InRelease
Get:3 https://packages.wazuh.com/4.x/apt stable/main amd64 Packages [31.5 kB]
Get:4 https://packages.wazuh.com/4.x/apt stable/main amd64 Contents (deb) [1,715 kB]
Fetched 1,764 kB in 3s (639 kB/s)         
Reading package lists... Done
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# apt-get -y install wazuh-indexer
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  debugedit gir1.2-gtksource-3.0 gir1.2-javascriptcoregtk-4.0
  gir1.2-soup-2.4 gir1.2-webkit2-4.0 gobject-introspection
  king-phisher libavfilter8 libavformat59 libblockdev-crypto2
  libblockdev-fs2 libblockdev-loop2 libblockdev-part-err2
  libblockdev-part2 libblockdev-swap2 libblockdev-utils2
  libblockdev2 libcodec2-1.0 libfsverity0 libgdal32 libgeos3.11.1
  libgnuradio-analog3.10.5 libgnuradio-audio3.10.5
  libgnuradio-blocks3.10.5 libgnuradio-channels3.10.5
  libgnuradio-digital3.10.5 libgnuradio-dtv3.10.5
  libgnuradio-fec3.10.5 libgnuradio-fft3.10.5
  libgnuradio-filter3.10.5 libgnuradio-iio3.10.5
  libgnuradio-network3.10.5 libgnuradio-pdu3.10.5
  libgnuradio-pmt3.10.5 libgnuradio-qtgui3.10.5
  libgnuradio-runtime3.10.5 libgnuradio-soapy3.10.5
  libgnuradio-trellis3.10.5 libgnuradio-uhd3.10.5
  libgnuradio-video-sdl3.10.5 libgnuradio-vocoder3.10.5
  libgnuradio-wavelet3.10.5 libgnuradio-zeromq3.10.5
  libgupnp-igd-1.0-4 libhttp-cookiejar-perl liblc3-0
  libmongocrypt0 libmozilla-publicsuffix-perl libmujs2 libncurses5
  libnfs13 libobjc-12-dev libplacebo208 libpostproc56 librpm9
  librpmbuild9 librpmio9 librpmsign9 libsoup-gnome2.4-1
  libspatialite7 libsuperlu5 libswscale6 libtinfo5 libuhd4.3.0
  libvolk2.5 libwebsockets17 libyara9
  linux-image-6.1.0-kali9-amd64 pipewire-alsa pwgen
  python3-advancedhttpserver python3-boltons python3-cairo-dev
  python3-cryptography37 python3-flask-security python3-geoip2
  python3-geojson python3-graphene python3-graphene-sqlalchemy
  python3-graphql-core python3-graphql-relay python3-icalendar
  python3-jaraco.classes python3-maxminddb python3-promise
  python3-pytz-deprecation-shim python3-requests-file
  python3-rule-engine python3-rx python3-smoke-zephyr
  python3-texttable tftp
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  wazuh-indexer
0 upgraded, 1 newly installed, 0 to remove and 1 not upgraded.
Need to get 688 MB of archives.
After this operation, 971 MB of additional disk space will be used.
Get:1 https://packages.wazuh.com/4.x/apt stable/main amd64 wazuh-indexer amd64 4.5.1-1 [688 MB]
Fetched 688 MB in 2min 4s (5,540 kB/s)                             
Selecting previously unselected package wazuh-indexer.              
(Reading database ... 464283 files and directories currently installed.)                                                                
Preparing to unpack .../wazuh-indexer_4.5.1-1_amd64.deb ...         
Creating wazuh-indexer group... OK                                  
Creating wazuh-indexer user... OK                                   
Unpacking wazuh-indexer (4.5.1-1) ...                               
Setting up wazuh-indexer (4.5.1-1) ...                              
Created opensearch keystore in /etc/wazuh-indexer/opensearch.keystore
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# nano /etc/wazuh-indexer/opensearch.yml
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# NODE_NAME=node-1             
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# mkdir /etc/wazuh-indexer/certs
tar -xf ./wazuh-certificates.tar -C /etc/wazuh-indexer/certs/ ./$NODE_NAME.pem ./$NODE_NAME-key.pem ./admin.pem ./admin-key.pem ./root-ca.pem
mv -n /etc/wazuh-indexer/certs/$NODE_NAME.pem /etc/wazuh-indexer/certs/indexer.pem
mv -n /etc/wazuh-indexer/certs/$NODE_NAME-key.pem /etc/wazuh-indexer/certs/indexer-key.pem
chmod 500 /etc/wazuh-indexer/certs
chmod 400 /etc/wazuh-indexer/certs/*
chown -R wazuh-indexer:wazuh-indexer /etc/wazuh-indexer/certs
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# cd /etc/wazuh-indexer 
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer]
└─# ls
certs                     opensearch-notifications-core
jvm.options               opensearch-observability
jvm.options.d             opensearch-performance-analyzer
log4j2.properties         opensearch-reports-scheduler
opensearch.keystore       opensearch-security
opensearch-notifications  opensearch.yml
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer]
└─# cd certs             
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# ls
admin-key.pem  admin.pem  indexer-key.pem  indexer.pem  root-ca.pem
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# systemctl daemon-reload
systemctl enable wazuh-indexer
systemctl start wazuh-indexer
Synchronizing state of wazuh-indexer.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable wazuh-indexer
Created symlink /etc/systemd/system/multi-user.target.wants/wazuh-indexer.service → /lib/systemd/system/wazuh-indexer.service.
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# systemctl status wazuh-indexer
● wazuh-indexer.service - Wazuh-indexer
     Loaded: loaded (/lib/systemd/system/wazuh-indexer.service; ena>
     Active: active (running) since Sun 2023-09-03 16:59:03 EDT; 43>
       Docs: https://documentation.wazuh.com
   Main PID: 27206 (java)
      Tasks: 63 (limit: 2265)
     Memory: 1.2G
        CPU: 1min 37.095s
     CGroup: /system.slice/wazuh-indexer.service
             └─27206 /usr/share/wazuh-indexer/jdk/bin/java -Xshare:>

Sep 03 16:58:09 kali systemd[1]: Starting wazuh-indexer.service - W>
Sep 03 16:58:16 kali systemd-entrypoint[27206]: WARNING: A terminal>
Sep 03 16:58:16 kali systemd-entrypoint[27206]: WARNING: System::se>
Sep 03 16:58:16 kali systemd-entrypoint[27206]: WARNING: Please con>
Sep 03 16:58:16 kali systemd-entrypoint[27206]: WARNING: System::se>
Sep 03 16:58:22 kali systemd-entrypoint[27206]: WARNING: A terminal>
Sep 03 16:58:22 kali systemd-entrypoint[27206]: WARNING: System::se>
Sep 03 16:58:22 kali systemd-entrypoint[27206]: WARNING: Please con>
Sep 03 16:58:22 kali systemd-entrypoint[27206]: WARNING: System::se>
Sep 03 16:59:03 kali systemd[1]: Started wazuh-indexer.service - Wa>
lines 1-21/21 (END)
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# /usr/share/wazuh-indexer/bin/indexer-security-init.sh
**************************************************************************
** This tool will be deprecated in the next major release of OpenSearch **
** https://github.com/opensearch-project/security/issues/1755           **
**************************************************************************
Security Admin v7
Will connect to 192.168.2.136:9200 ... done
Connected as "CN=admin,OU=Wazuh,O=Wazuh,L=California,C=US"
OpenSearch Version: 2.6.0
Contacting opensearch cluster 'opensearch' and wait for YELLOW clusterstate ...
Clustername: wazuh-cluster
Clusterstate: GREEN
Number of nodes: 1
Number of data nodes: 1
.opendistro_security index does not exists, attempt to create it ... done (0-all replicas)
Populate config from /etc/wazuh-indexer/opensearch-security/
Will update '/config' with /etc/wazuh-indexer/opensearch-security/config.yml 
   SUCC: Configuration for 'config' created or updated
Will update '/roles' with /etc/wazuh-indexer/opensearch-security/roles.yml 
   SUCC: Configuration for 'roles' created or updated
Will update '/rolesmapping' with /etc/wazuh-indexer/opensearch-security/roles_mapping.yml 
   SUCC: Configuration for 'rolesmapping' created or updated
Will update '/internalusers' with /etc/wazuh-indexer/opensearch-security/internal_users.yml 
   SUCC: Configuration for 'internalusers' created or updated
Will update '/actiongroups' with /etc/wazuh-indexer/opensearch-security/action_groups.yml 
   SUCC: Configuration for 'actiongroups' created or updated
Will update '/tenants' with /etc/wazuh-indexer/opensearch-security/tenants.yml 
   SUCC: Configuration for 'tenants' created or updated
Will update '/nodesdn' with /etc/wazuh-indexer/opensearch-security/nodes_dn.yml 
   SUCC: Configuration for 'nodesdn' created or updated
Will update '/whitelist' with /etc/wazuh-indexer/opensearch-security/whitelist.yml 
   SUCC: Configuration for 'whitelist' created or updated
Will update '/audit' with /etc/wazuh-indexer/opensearch-security/audit.yml 
   SUCC: Configuration for 'audit' created or updated
Will update '/allowlist' with /etc/wazuh-indexer/opensearch-security/allowlist.yml 
   SUCC: Configuration for 'allowlist' created or updated
SUCC: Expected 10 config types for node {"updated_config_types":["allowlist","tenants","rolesmapping","nodesdn","audit","roles","whitelist","internalusers","actiongroups","config"],"updated_config_size":10,"message":null} is 10 (["allowlist","tenants","rolesmapping","nodesdn","audit","roles","whitelist","internalusers","actiongroups","config"]) due to: null
Done with success
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# apt-get -y install wazuh-manager
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  debugedit gir1.2-gtksource-3.0 gir1.2-javascriptcoregtk-4.0
  gir1.2-soup-2.4 gir1.2-webkit2-4.0 gobject-introspection
  king-phisher libavfilter8 libavformat59 libblockdev-crypto2
  libblockdev-fs2 libblockdev-loop2 libblockdev-part-err2
  libblockdev-part2 libblockdev-swap2 libblockdev-utils2
  libblockdev2 libcodec2-1.0 libfsverity0 libgdal32 libgeos3.11.1
  libgnuradio-analog3.10.5 libgnuradio-audio3.10.5
  libgnuradio-blocks3.10.5 libgnuradio-channels3.10.5
  libgnuradio-digital3.10.5 libgnuradio-dtv3.10.5
  libgnuradio-fec3.10.5 libgnuradio-fft3.10.5
  libgnuradio-filter3.10.5 libgnuradio-iio3.10.5
  libgnuradio-network3.10.5 libgnuradio-pdu3.10.5
  libgnuradio-pmt3.10.5 libgnuradio-qtgui3.10.5
  libgnuradio-runtime3.10.5 libgnuradio-soapy3.10.5
  libgnuradio-trellis3.10.5 libgnuradio-uhd3.10.5
  libgnuradio-video-sdl3.10.5 libgnuradio-vocoder3.10.5
  libgnuradio-wavelet3.10.5 libgnuradio-zeromq3.10.5
  libgupnp-igd-1.0-4 libhttp-cookiejar-perl liblc3-0
  libmongocrypt0 libmozilla-publicsuffix-perl libmujs2 libncurses5
  libnfs13 libobjc-12-dev libplacebo208 libpostproc56 librpm9
  librpmbuild9 librpmio9 librpmsign9 libsoup-gnome2.4-1
  libspatialite7 libsuperlu5 libswscale6 libtinfo5 libuhd4.3.0
  libvolk2.5 libwebsockets17 libyara9
  linux-image-6.1.0-kali9-amd64 pipewire-alsa pwgen
  python3-advancedhttpserver python3-boltons python3-cairo-dev
  python3-cryptography37 python3-flask-security python3-geoip2
  python3-geojson python3-graphene python3-graphene-sqlalchemy
  python3-graphql-core python3-graphql-relay python3-icalendar
  python3-jaraco.classes python3-maxminddb python3-promise
  python3-pytz-deprecation-shim python3-requests-file
  python3-rule-engine python3-rx python3-smoke-zephyr
  python3-texttable tftp
Use 'sudo apt autoremove' to remove them.
The following packages will be REMOVED:
  wazuh-agent
The following NEW packages will be installed:
  wazuh-manager
0 upgraded, 1 newly installed, 1 to remove and 0 not upgraded.
Need to get 171 MB of archives.
After this operation, 597 MB of additional disk space will be used.
Get:1 https://packages.wazuh.com/4.x/apt stable/main amd64 wazuh-manager amd64 4.5.1-1 [171 MB]
Fetched 171 MB in 29s (5,842 kB/s)                                 
(Reading database ... 465405 files and directories currently installed.)
Removing wazuh-agent (4.4.5-1) ...
Selecting previously unselected package wazuh-manager.
(Reading database ... 465052 files and directories currently installed.)
Preparing to unpack .../wazuh-manager_4.5.1-1_amd64.deb ...
Unpacking wazuh-manager (4.5.1-1) ...
Setting up wazuh-manager (4.5.1-1) ...
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# systemctl daemon-reload
systemctl enable wazuh-manager
systemctl start wazuh-manager
Synchronizing state of wazuh-manager.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable wazuh-manager
Created symlink /etc/systemd/system/multi-user.target.wants/wazuh-manager.service → /lib/systemd/system/wazuh-manager.service.
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# systemctl status wazuh-manager
● wazuh-manager.service - Wazuh manager
     Loaded: loaded (/lib/systemd/system/wazuh-manager.service; ena>
     Active: active (running) since Sun 2023-09-03 17:09:34 EDT; 42>
    Process: 76017 ExecStart=/usr/bin/env /var/ossec/bin/wazuh-cont>
      Tasks: 111 (limit: 2265)
     Memory: 310.0M
        CPU: 1min 8.999s
     CGroup: /system.slice/wazuh-manager.service
             ├─76335 /var/ossec/framework/python/bin/python3 /var/o>
             ├─76384 /var/ossec/bin/wazuh-authd
             ├─76408 /var/ossec/bin/wazuh-db
             ├─76439 /var/ossec/bin/wazuh-execd
             ├─76469 /var/ossec/bin/wazuh-analysisd
             ├─76489 /var/ossec/bin/wazuh-syscheckd
             ├─76513 /var/ossec/bin/wazuh-remoted
             ├─76584 /var/ossec/bin/wazuh-logcollector
             ├─76600 /var/ossec/framework/python/bin/python3 /var/o>
             ├─76603 /var/ossec/framework/python/bin/python3 /var/o>
             ├─76616 /var/ossec/bin/wazuh-monitord
             └─76647 /var/ossec/bin/wazuh-modulesd

Sep 03 17:09:24 kali env[76017]: Started wazuh-db...
Sep 03 17:09:25 kali env[76017]: Started wazuh-execd...
Sep 03 17:09:26 kali env[76017]: Started wazuh-analysisd...
Sep 03 17:09:27 kali env[76017]: Started wazuh-syscheckd...
Sep 03 17:09:28 kali env[76017]: Started wazuh-remoted...
Sep 03 17:09:29 kali env[76017]: Started wazuh-logcollector...
Sep 03 17:09:30 kali env[76017]: Started wazuh-monitord...
Sep 03 17:09:32 kali env[76017]: Started wazuh-modulesd...
Sep 03 17:09:34 kali env[76017]: Completed.
Sep 03 17:09:34 kali systemd[1]: Started wazuh-manager.service - Wa>
lines 1-31/31 (END)
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# apt-get -y install filebeat
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  debugedit gir1.2-gtksource-3.0 gir1.2-javascriptcoregtk-4.0
  gir1.2-soup-2.4 gir1.2-webkit2-4.0 gobject-introspection
  king-phisher libavfilter8 libavformat59 libblockdev-crypto2
  libblockdev-fs2 libblockdev-loop2 libblockdev-part-err2
  libblockdev-part2 libblockdev-swap2 libblockdev-utils2
  libblockdev2 libcodec2-1.0 libfsverity0 libgdal32 libgeos3.11.1
  libgnuradio-analog3.10.5 libgnuradio-audio3.10.5
  libgnuradio-blocks3.10.5 libgnuradio-channels3.10.5
  libgnuradio-digital3.10.5 libgnuradio-dtv3.10.5
  libgnuradio-fec3.10.5 libgnuradio-fft3.10.5
  libgnuradio-filter3.10.5 libgnuradio-iio3.10.5
  libgnuradio-network3.10.5 libgnuradio-pdu3.10.5
  libgnuradio-pmt3.10.5 libgnuradio-qtgui3.10.5
  libgnuradio-runtime3.10.5 libgnuradio-soapy3.10.5
  libgnuradio-trellis3.10.5 libgnuradio-uhd3.10.5
  libgnuradio-video-sdl3.10.5 libgnuradio-vocoder3.10.5
  libgnuradio-wavelet3.10.5 libgnuradio-zeromq3.10.5
  libgupnp-igd-1.0-4 libhttp-cookiejar-perl liblc3-0
  libmongocrypt0 libmozilla-publicsuffix-perl libmujs2 libncurses5
  libnfs13 libobjc-12-dev libplacebo208 libpostproc56 librpm9
  librpmbuild9 librpmio9 librpmsign9 libsoup-gnome2.4-1
  libspatialite7 libsuperlu5 libswscale6 libtinfo5 libuhd4.3.0
  libvolk2.5 libwebsockets17 libyara9
  linux-image-6.1.0-kali9-amd64 pipewire-alsa pwgen
  python3-advancedhttpserver python3-boltons python3-cairo-dev
  python3-cryptography37 python3-flask-security python3-geoip2
  python3-geojson python3-graphene python3-graphene-sqlalchemy
  python3-graphql-core python3-graphql-relay python3-icalendar
  python3-jaraco.classes python3-maxminddb python3-promise
  python3-pytz-deprecation-shim python3-requests-file
  python3-rule-engine python3-rx python3-smoke-zephyr
  python3-texttable tftp
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  filebeat
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 22.1 MB of archives.
After this operation, 73.6 MB of additional disk space will be used.
Get:1 https://packages.wazuh.com/4.x/apt stable/main amd64 filebeat amd64 7.10.2 [22.1 MB]
Fetched 22.1 MB in 5s (4,896 kB/s)   
Selecting previously unselected package filebeat.
(Reading database ... 486310 files and directories currently installed.)
Preparing to unpack .../filebeat_7.10.2_amd64.deb ...
Unpacking filebeat (7.10.2) ...
Setting up filebeat (7.10.2) ...
Processing triggers for kali-menu (2023.4.5) ...
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# curl -so /etc/filebeat/filebeat.yml https://packages.wazuh.com/4.5/tpl/wazuh/filebeat/filebeat.yml
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# nano /etc/filebeat/filebeat.yml       
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# filebeat keystore create
Created filebeat keystore
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# echo admin | filebeat keystore add username --stdin --force
echo admin | filebeat keystore add password --stdin --force
Successfully updated the keystore
Successfully updated the keystore
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# curl -so /etc/filebeat/wazuh-template.json https://raw.githubusercontent.com/wazuh/wazuh/4.5/extensions/elasticsearch/7.x/wazuh-template.json
chmod go+r /etc/filebeat/wazuh-template.json
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# curl -s https://packages.wazuh.com/4.x/filebeat/wazuh-filebeat-0.2.tar.gz | tar -xvz -C /usr/share/filebeat/module
wazuh/alerts/
wazuh/alerts/config/
wazuh/alerts/config/alerts.yml
wazuh/alerts/manifest.yml
wazuh/alerts/ingest/
wazuh/alerts/ingest/pipeline.json
wazuh/archives/
wazuh/archives/config/
wazuh/archives/config/archives.yml
wazuh/archives/manifest.yml
wazuh/archives/ingest/
wazuh/archives/ingest/pipeline.json
wazuh/module.yml
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer/certs]
└─# /                                                    
                                                                    
┌──(root㉿kali)-[/]
└─# ls
bin   initrd.img      libx32      proc  swapfile  vmlinuz
boot  initrd.img.old  lost+found  root  sys       vmlinuz.old
dev   lib             media       run   tmp
etc   lib32           mnt         sbin  usr
home  lib64           opt         srv   var
                                                                    
┌──(root㉿kali)-[/]
└─# ~
                                                                    
┌──(root㉿kali)-[~]
└─# ls
bettercap.history
                                                                    
┌──(root㉿kali)-[~]
└─# cd ..   
                                                                    
┌──(root㉿kali)-[/]
└─# ls
bin   initrd.img      libx32      proc  swapfile  vmlinuz
boot  initrd.img.old  lost+found  root  sys       vmlinuz.old
dev   lib             media       run   tmp
etc   lib32           mnt         sbin  usr
home  lib64           opt         srv   var
                                                                    
┌──(root㉿kali)-[/]
└─# cd /kali             
cd: no such file or directory: /kali
                                                                    
┌──(root㉿kali)-[/]
└─# ~       
                                                                    
┌──(root㉿kali)-[~]
└─# cd /kali
cd: no such file or directory: /kali
                                                                    
┌──(root㉿kali)-[~]
└─# ls
bettercap.history
                                                                    
┌──(root㉿kali)-[~]
└─# cd ..   
                                                                    
┌──(root㉿kali)-[/]
└─# ls
bin   initrd.img      libx32      proc  swapfile  vmlinuz
boot  initrd.img.old  lost+found  root  sys       vmlinuz.old
dev   lib             media       run   tmp
etc   lib32           mnt         sbin  usr
home  lib64           opt         srv   var
                                                                    
┌──(root㉿kali)-[/]
└─# cd /home/kali 
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# ls
config.yml  Downloads  Public     wazuh-certificates.tar
Desktop     Music      Templates  wazuh-certs-tool.sh
Documents   Pictures   Videos
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# NODE_NAME=wazuh-1
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# mkdir /etc/filebeat/certs
tar -xf ./wazuh-certificates.tar -C /etc/filebeat/certs/ ./$NODE_NAME.pem ./$NODE_NAME-key.pem ./root-ca.pem
mv -n /etc/filebeat/certs/$NODE_NAME.pem /etc/filebeat/certs/filebeat.pem
mv -n /etc/filebeat/certs/$NODE_NAME-key.pem /etc/filebeat/certs/filebeat-key.pem
chmod 500 /etc/filebeat/certs
chmod 400 /etc/filebeat/certs/*
chown -R root:root /etc/filebeat/certs
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# systemctl daemon-reload
systemctl enable filebeat
systemctl start filebeat
Synchronizing state of filebeat.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable filebeat
Created symlink /etc/systemd/system/multi-user.target.wants/filebeat.service → /lib/systemd/system/filebeat.service.
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# systemctl status filebeat.service 
● filebeat.service - Filebeat sends log files to Logstash or direct>
     Loaded: loaded (/lib/systemd/system/filebeat.service; enabled;>
     Active: active (running) since Sun 2023-09-03 17:26:52 EDT; 51>
       Docs: https://www.elastic.co/products/beats/filebeat
   Main PID: 85627 (filebeat)
      Tasks: 7 (limit: 2265)
     Memory: 13.7M
        CPU: 145ms
     CGroup: /system.slice/filebeat.service
             └─85627 /usr/share/filebeat/bin/filebeat --environment>

Sep 03 17:26:52 kali systemd[1]: Started filebeat.service - Filebea>

                                                                    
┌──(root㉿kali)-[/home/kali]
└─# filebeat test output
elasticsearch: https://192.168.2.136:9200...
  parse url... OK
  connection...                                                     
    parse host... OK
    dns lookup... OK                                                
    addresses: 192.168.2.136                                        
    dial up... OK
  TLS...                                                            
    security: server's certificate chain verification is enabled
    handshake... OK
    TLS version: TLSv1.3                                            
    dial up... OK
  talk to server... OK                                              
  version: 7.10.2                                                   
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# apt-get install debhelper tar curl libcap2-bin #debhelper version 9 or later
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
tar is already the newest version (1.34+dfsg-1.2).
curl is already the newest version (8.2.1-1).
curl set to manually installed.
libcap2-bin is already the newest version (1:2.66-4).
The following packages were automatically installed and are no longer required:
  debugedit gir1.2-gtksource-3.0 gir1.2-javascriptcoregtk-4.0
  gir1.2-soup-2.4 gir1.2-webkit2-4.0 gobject-introspection
  king-phisher libavfilter8 libavformat59 libblockdev-crypto2
  libblockdev-fs2 libblockdev-loop2 libblockdev-part-err2
  libblockdev-part2 libblockdev-swap2 libblockdev-utils2
  libblockdev2 libcodec2-1.0 libfsverity0 libgdal32 libgeos3.11.1
  libgnuradio-analog3.10.5 libgnuradio-audio3.10.5
  libgnuradio-blocks3.10.5 libgnuradio-channels3.10.5
  libgnuradio-digital3.10.5 libgnuradio-dtv3.10.5
  libgnuradio-fec3.10.5 libgnuradio-fft3.10.5
  libgnuradio-filter3.10.5 libgnuradio-iio3.10.5
  libgnuradio-network3.10.5 libgnuradio-pdu3.10.5
  libgnuradio-pmt3.10.5 libgnuradio-qtgui3.10.5
  libgnuradio-runtime3.10.5 libgnuradio-soapy3.10.5
  libgnuradio-trellis3.10.5 libgnuradio-uhd3.10.5
  libgnuradio-video-sdl3.10.5 libgnuradio-vocoder3.10.5
  libgnuradio-wavelet3.10.5 libgnuradio-zeromq3.10.5
  libgupnp-igd-1.0-4 libhttp-cookiejar-perl liblc3-0
  libmongocrypt0 libmozilla-publicsuffix-perl libmujs2 libncurses5
  libnfs13 libobjc-12-dev libplacebo208 libpostproc56 librpm9
  librpmbuild9 librpmio9 librpmsign9 libsoup-gnome2.4-1
  libspatialite7 libsuperlu5 libswscale6 libtinfo5 libuhd4.3.0
  libvolk2.5 libwebsockets17 libyara9
  linux-image-6.1.0-kali9-amd64 pipewire-alsa pwgen
  python3-advancedhttpserver python3-boltons python3-cairo-dev
  python3-cryptography37 python3-flask-security python3-geoip2
  python3-geojson python3-graphene python3-graphene-sqlalchemy
  python3-graphql-core python3-graphql-relay python3-icalendar
  python3-jaraco.classes python3-maxminddb python3-promise
  python3-pytz-deprecation-shim python3-requests-file
  python3-rule-engine python3-rx python3-smoke-zephyr
  python3-texttable tftp
Use 'sudo apt autoremove' to remove them.
The following additional packages will be installed:
  autopoint dh-autoreconf dh-strip-nondeterminism dwz gettext
  intltool-debian libarchive-cpio-perl libdebhelper-perl
  libfile-stripnondeterminism-perl libmail-sendmail-perl
  libsub-override-perl libsys-hostname-long-perl po-debconf
Suggested packages:
  dh-make gettext-doc libasprintf-dev libgettextpo-dev
  libmail-box-perl
The following NEW packages will be installed:
  autopoint debhelper dh-autoreconf dh-strip-nondeterminism dwz
  gettext intltool-debian libarchive-cpio-perl libdebhelper-perl
  libfile-stripnondeterminism-perl libmail-sendmail-perl
  libsub-override-perl libsys-hostname-long-perl po-debconf
0 upgraded, 14 newly installed, 0 to remove and 0 not upgraded.
Need to get 3,311 kB of archives.
After this operation, 9,384 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 autopoint all 0.21-13 [496 kB]
Get:2 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 libdebhelper-perl all 13.11.6 [81.9 kB]
Get:3 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 dh-autoreconf all 20 [17.1 kB]
Get:4 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 libsub-override-perl all 0.09-4 [9,304 B]
Get:5 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 libfile-stripnondeterminism-perl all 1.13.1-1 [19.4 kB]
Get:6 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 dh-strip-nondeterminism all 1.13.1-1 [8,620 B]
Get:7 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 dwz amd64 0.15-1 [109 kB]
Get:8 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 gettext amd64 0.21-13 [1,300 kB]
Get:9 http://http.kali.org/kali kali-rolling/main amd64 intltool-debian all 0.35.0+20060710.6 [22.9 kB]
Get:10 http://http.kali.org/kali kali-rolling/main amd64 po-debconf all 1.0.21+nmu1 [248 kB]
Get:11 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 debhelper all 13.11.6 [952 kB]
Get:12 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 libarchive-cpio-perl all 0.10-3 [10.8 kB]
Get:13 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 libsys-hostname-long-perl all 1.5-3 [11.6 kB]
Get:14 http://kali.cs.nycu.edu.tw/kali kali-rolling/main amd64 libmail-sendmail-perl all 0.80-3 [24.3 kB]
Fetched 3,311 kB in 36s (90.9 kB/s)                                
Selecting previously unselected package autopoint.
(Reading database ... 486629 files and directories currently installed.)
Preparing to unpack .../00-autopoint_0.21-13_all.deb ...
Unpacking autopoint (0.21-13) ...
Selecting previously unselected package libdebhelper-perl.
Preparing to unpack .../01-libdebhelper-perl_13.11.6_all.deb ...
Unpacking libdebhelper-perl (13.11.6) ...
Selecting previously unselected package dh-autoreconf.
Preparing to unpack .../02-dh-autoreconf_20_all.deb ...
Unpacking dh-autoreconf (20) ...
Selecting previously unselected package libsub-override-perl.
Preparing to unpack .../03-libsub-override-perl_0.09-4_all.deb ...
Unpacking libsub-override-perl (0.09-4) ...
Selecting previously unselected package libfile-stripnondeterminism-perl.
Preparing to unpack .../04-libfile-stripnondeterminism-perl_1.13.1-1_all.deb ...
Unpacking libfile-stripnondeterminism-perl (1.13.1-1) ...
Selecting previously unselected package dh-strip-nondeterminism.
Preparing to unpack .../05-dh-strip-nondeterminism_1.13.1-1_all.deb ...
Unpacking dh-strip-nondeterminism (1.13.1-1) ...
Selecting previously unselected package dwz.
Preparing to unpack .../06-dwz_0.15-1_amd64.deb ...
Unpacking dwz (0.15-1) ...
Selecting previously unselected package gettext.
Preparing to unpack .../07-gettext_0.21-13_amd64.deb ...
Unpacking gettext (0.21-13) ...
Selecting previously unselected package intltool-debian.
Preparing to unpack .../08-intltool-debian_0.35.0+20060710.6_all.deb ...
Unpacking intltool-debian (0.35.0+20060710.6) ...
Selecting previously unselected package po-debconf.
Preparing to unpack .../09-po-debconf_1.0.21+nmu1_all.deb ...
Unpacking po-debconf (1.0.21+nmu1) ...
Selecting previously unselected package debhelper.
Preparing to unpack .../10-debhelper_13.11.6_all.deb ...
Unpacking debhelper (13.11.6) ...
Selecting previously unselected package libarchive-cpio-perl.
Preparing to unpack .../11-libarchive-cpio-perl_0.10-3_all.deb ...
Unpacking libarchive-cpio-perl (0.10-3) ...
Selecting previously unselected package libsys-hostname-long-perl.
Preparing to unpack .../12-libsys-hostname-long-perl_1.5-3_all.deb ...
Unpacking libsys-hostname-long-perl (1.5-3) ...
Selecting previously unselected package libmail-sendmail-perl.
Preparing to unpack .../13-libmail-sendmail-perl_0.80-3_all.deb ...
Unpacking libmail-sendmail-perl (0.80-3) ...
Setting up gettext (0.21-13) ...
Setting up libdebhelper-perl (13.11.6) ...
Setting up intltool-debian (0.35.0+20060710.6) ...
Setting up autopoint (0.21-13) ...
Setting up dwz (0.15-1) ...
Setting up libarchive-cpio-perl (0.10-3) ...
Setting up libsub-override-perl (0.09-4) ...
Setting up libsys-hostname-long-perl (1.5-3) ...
Setting up libfile-stripnondeterminism-perl (1.13.1-1) ...
Setting up po-debconf (1.0.21+nmu1) ...
Setting up dh-autoreconf (20) ...
Setting up libmail-sendmail-perl (0.80-3) ...
Setting up dh-strip-nondeterminism (1.13.1-1) ...
Setting up debhelper (13.11.6) ...
Processing triggers for kali-menu (2023.4.5) ...
Processing triggers for doc-base (0.11.1) ...
Processing 1 added doc-base file...
Processing triggers for libc-bin (2.37-7) ...
Processing triggers for man-db (2.11.2-3) ...
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# apt-get install gnupg apt-transport-https
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
gnupg is already the newest version (2.2.40-1.1).
apt-transport-https is already the newest version (2.7.3).
The following packages were automatically installed and are no longer required:
  debugedit gir1.2-gtksource-3.0 gir1.2-javascriptcoregtk-4.0
  gir1.2-soup-2.4 gir1.2-webkit2-4.0 gobject-introspection
  king-phisher libavfilter8 libavformat59 libblockdev-crypto2
  libblockdev-fs2 libblockdev-loop2 libblockdev-part-err2
  libblockdev-part2 libblockdev-swap2 libblockdev-utils2
  libblockdev2 libcodec2-1.0 libfsverity0 libgdal32 libgeos3.11.1
  libgnuradio-analog3.10.5 libgnuradio-audio3.10.5
  libgnuradio-blocks3.10.5 libgnuradio-channels3.10.5
  libgnuradio-digital3.10.5 libgnuradio-dtv3.10.5
  libgnuradio-fec3.10.5 libgnuradio-fft3.10.5
  libgnuradio-filter3.10.5 libgnuradio-iio3.10.5
  libgnuradio-network3.10.5 libgnuradio-pdu3.10.5
  libgnuradio-pmt3.10.5 libgnuradio-qtgui3.10.5
  libgnuradio-runtime3.10.5 libgnuradio-soapy3.10.5
  libgnuradio-trellis3.10.5 libgnuradio-uhd3.10.5
  libgnuradio-video-sdl3.10.5 libgnuradio-vocoder3.10.5
  libgnuradio-wavelet3.10.5 libgnuradio-zeromq3.10.5
  libgupnp-igd-1.0-4 libhttp-cookiejar-perl liblc3-0
  libmongocrypt0 libmozilla-publicsuffix-perl libmujs2 libncurses5
  libnfs13 libobjc-12-dev libplacebo208 libpostproc56 librpm9
  librpmbuild9 librpmio9 librpmsign9 libsoup-gnome2.4-1
  libspatialite7 libsuperlu5 libswscale6 libtinfo5 libuhd4.3.0
  libvolk2.5 libwebsockets17 libyara9
  linux-image-6.1.0-kali9-amd64 pipewire-alsa pwgen
  python3-advancedhttpserver python3-boltons python3-cairo-dev
  python3-cryptography37 python3-flask-security python3-geoip2
  python3-geojson python3-graphene python3-graphene-sqlalchemy
  python3-graphql-core python3-graphql-relay python3-icalendar
  python3-jaraco.classes python3-maxminddb python3-promise
  python3-pytz-deprecation-shim python3-requests-file
  python3-rule-engine python3-rx python3-smoke-zephyr
  python3-texttable tftp
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# apt-get update
Hit:1 https://packages.wazuh.com/4.x/apt stable InRelease
Hit:2 http://kali.cs.nycu.edu.tw/kali kali-rolling InRelease
Reading package lists... Done
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# apt-get -y install wazuh-dashboard
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  debugedit gir1.2-gtksource-3.0 gir1.2-javascriptcoregtk-4.0
  gir1.2-soup-2.4 gir1.2-webkit2-4.0 gobject-introspection
  king-phisher libavfilter8 libavformat59 libblockdev-crypto2
  libblockdev-fs2 libblockdev-loop2 libblockdev-part-err2
  libblockdev-part2 libblockdev-swap2 libblockdev-utils2
  libblockdev2 libcodec2-1.0 libfsverity0 libgdal32 libgeos3.11.1
  libgnuradio-analog3.10.5 libgnuradio-audio3.10.5
  libgnuradio-blocks3.10.5 libgnuradio-channels3.10.5
  libgnuradio-digital3.10.5 libgnuradio-dtv3.10.5
  libgnuradio-fec3.10.5 libgnuradio-fft3.10.5
  libgnuradio-filter3.10.5 libgnuradio-iio3.10.5
  libgnuradio-network3.10.5 libgnuradio-pdu3.10.5
  libgnuradio-pmt3.10.5 libgnuradio-qtgui3.10.5
  libgnuradio-runtime3.10.5 libgnuradio-soapy3.10.5
  libgnuradio-trellis3.10.5 libgnuradio-uhd3.10.5
  libgnuradio-video-sdl3.10.5 libgnuradio-vocoder3.10.5
  libgnuradio-wavelet3.10.5 libgnuradio-zeromq3.10.5
  libgupnp-igd-1.0-4 libhttp-cookiejar-perl liblc3-0
  libmongocrypt0 libmozilla-publicsuffix-perl libmujs2 libncurses5
  libnfs13 libobjc-12-dev libplacebo208 libpostproc56 librpm9
  librpmbuild9 librpmio9 librpmsign9 libsoup-gnome2.4-1
  libspatialite7 libsuperlu5 libswscale6 libtinfo5 libuhd4.3.0
  libvolk2.5 libwebsockets17 libyara9
  linux-image-6.1.0-kali9-amd64 pipewire-alsa pwgen
  python3-advancedhttpserver python3-boltons python3-cairo-dev
  python3-cryptography37 python3-flask-security python3-geoip2
  python3-geojson python3-graphene python3-graphene-sqlalchemy
  python3-graphql-core python3-graphql-relay python3-icalendar
  python3-jaraco.classes python3-maxminddb python3-promise
  python3-pytz-deprecation-shim python3-requests-file
  python3-rule-engine python3-rx python3-smoke-zephyr
  python3-texttable tftp
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  wazuh-dashboard
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 128 MB of archives.
After this operation, 813 MB of additional disk space will be used.
Get:1 https://packages.wazuh.com/4.x/apt stable/main amd64 wazuh-dashboard amd64 4.5.1-1 [128 MB]
Fetched 128 MB in 22s (5,831 kB/s)                                 
Selecting previously unselected package wazuh-dashboard.
(Reading database ... 487426 files and directories currently installed.)
Preparing to unpack .../wazuh-dashboard_4.5.1-1_amd64.deb ...
Creating wazuh-dashboard group... OK
Creating wazuh-dashboard user... OK
Unpacking wazuh-dashboard (4.5.1-1) ...
Setting up wazuh-dashboard (4.5.1-1) ...
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# nano /etc/wazuh-dashboard/opensearch_dashboards.yml
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# NODE_NAME=dashboard   
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# mkdir /etc/wazuh-dashboard/certs
tar -xf ./wazuh-certificates.tar -C /etc/wazuh-dashboard/certs/ ./$NODE_NAME.pem ./$NODE_NAME-key.pem ./root-ca.pem
mv -n /etc/wazuh-dashboard/certs/$NODE_NAME.pem /etc/wazuh-dashboard/certs/dashboard.pem
mv -n /etc/wazuh-dashboard/certs/$NODE_NAME-key.pem /etc/wazuh-dashboard/certs/dashboard-key.pem
chmod 500 /etc/wazuh-dashboard/certs
chmod 400 /etc/wazuh-dashboard/certs/*
chown -R wazuh-dashboard:wazuh-dashboard /etc/wazuh-dashboard/certs
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# systemctl daemon-reload
systemctl enable wazuh-dashboard
systemctl start wazuh-dashboard
Created symlink /etc/systemd/system/multi-user.target.wants/wazuh-dashboard.service → /etc/systemd/system/wazuh-dashboard.service.
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# systemctl status wazuh-dashboard.service 
● wazuh-dashboard.service - wazuh-dashboard
     Loaded: loaded (/etc/systemd/system/wazuh-dashboard.service; e>
     Active: active (running) since Sun 2023-09-03 17:41:19 EDT; 1m>
   Main PID: 93352 (node)
      Tasks: 11 (limit: 2265)
     Memory: 182.5M
        CPU: 25.344s
     CGroup: /system.slice/wazuh-dashboard.service
             └─93352 /usr/share/wazuh-dashboard/bin/../node/bin/nod>

Sep 03 17:41:41 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:42 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:42 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:43 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:43 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:43 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:45 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:46 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:46 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:46 kali opensearch-dashboards[93352]: {"type":"log","@>
lines 1-20/20 (END)
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# nano /usr/share/wazuh-dashboard/data/wazuh/config/wazuh.yml
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# systemctl status wazuh-dashboard.service                   
● wazuh-dashboard.service - wazuh-dashboard
     Loaded: loaded (/etc/systemd/system/wazuh-dashboard.service; e>
     Active: active (running) since Sun 2023-09-03 17:41:19 EDT; 3m>
   Main PID: 93352 (node)
      Tasks: 11 (limit: 2265)
     Memory: 145.3M
        CPU: 27.770s
     CGroup: /system.slice/wazuh-dashboard.service
             └─93352 /usr/share/wazuh-dashboard/bin/../node/bin/nod>

Sep 03 17:41:41 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:42 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:42 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:43 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:43 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:43 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:45 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:46 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:46 kali opensearch-dashboards[93352]: {"type":"log","@>
Sep 03 17:41:46 kali opensearch-dashboards[93352]: {"type":"log","@>
lines 1-20/20 (END)
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# systemctl status wazuh-manager.service                     
● wazuh-manager.service - Wazuh manager
     Loaded: loaded (/lib/systemd/system/wazuh-manager.service; ena>
     Active: active (running) since Sun 2023-09-03 17:09:34 EDT; 42>
      Tasks: 112 (limit: 2265)
     Memory: 247.2M
        CPU: 2min 21.691s
     CGroup: /system.slice/wazuh-manager.service
             ├─76335 /var/ossec/framework/python/bin/python3 /var/o>
             ├─76384 /var/ossec/bin/wazuh-authd
             ├─76408 /var/ossec/bin/wazuh-db
             ├─76439 /var/ossec/bin/wazuh-execd
             ├─76469 /var/ossec/bin/wazuh-analysisd
             ├─76489 /var/ossec/bin/wazuh-syscheckd
             ├─76513 /var/ossec/bin/wazuh-remoted
             ├─76584 /var/ossec/bin/wazuh-logcollector
             ├─76600 /var/ossec/framework/python/bin/python3 /var/o>
             ├─76603 /var/ossec/framework/python/bin/python3 /var/o>
             ├─76616 /var/ossec/bin/wazuh-monitord
             └─76647 /var/ossec/bin/wazuh-modulesd

Sep 03 17:09:24 kali env[76017]: Started wazuh-db...
Sep 03 17:09:25 kali env[76017]: Started wazuh-execd...
Sep 03 17:09:26 kali env[76017]: Started wazuh-analysisd...
Sep 03 17:09:27 kali env[76017]: Started wazuh-syscheckd...
Sep 03 17:09:28 kali env[76017]: Started wazuh-remoted...
Sep 03 17:09:29 kali env[76017]: Started wazuh-logcollector...
Sep 03 17:09:30 kali env[76017]: Started wazuh-monitord...
Sep 03 17:09:32 kali env[76017]: Started wazuh-modulesd...
Sep 03 17:09:34 kali env[76017]: Completed.
Sep 03 17:09:34 kali systemd[1]: Started wazuh-manager.service - Wa>

                                                                    
┌──(root㉿kali)-[/home/kali]
└─# systemctl status filebeat.service     
● filebeat.service - Filebeat sends log files to Logstash or direct>
     Loaded: loaded (/lib/systemd/system/filebeat.service; enabled;>
     Active: active (running) since Sun 2023-09-03 17:26:52 EDT; 25>
       Docs: https://www.elastic.co/products/beats/filebeat
   Main PID: 85627 (filebeat)
      Tasks: 8 (limit: 2265)
     Memory: 11.8M
        CPU: 974ms
     CGroup: /system.slice/filebeat.service
             └─85627 /usr/share/filebeat/bin/filebeat --environment>

Sep 03 17:26:52 kali systemd[1]: Started filebeat.service - Filebea>

                                                                    
┌──(root㉿kali)-[/home/kali]
└─# systemctl status wazuh-indexer        
● wazuh-indexer.service - Wazuh-indexer
     Loaded: loaded (/lib/systemd/system/wazuh-indexer.service; ena>
     Active: active (running) since Sun 2023-09-03 16:59:03 EDT; 53>
       Docs: https://documentation.wazuh.com
   Main PID: 27206 (java)
      Tasks: 71 (limit: 2265)
     Memory: 923.5M
        CPU: 4min 21.678s
     CGroup: /system.slice/wazuh-indexer.service
             └─27206 /usr/share/wazuh-indexer/jdk/bin/java -Xshare:>

Sep 03 16:58:09 kali systemd[1]: Starting wazuh-indexer.service - W>
Sep 03 16:58:16 kali systemd-entrypoint[27206]: WARNING: A terminal>
Sep 03 16:58:16 kali systemd-entrypoint[27206]: WARNING: System::se>
Sep 03 16:58:16 kali systemd-entrypoint[27206]: WARNING: Please con>
Sep 03 16:58:16 kali systemd-entrypoint[27206]: WARNING: System::se>
Sep 03 16:58:22 kali systemd-entrypoint[27206]: WARNING: A terminal>
Sep 03 16:58:22 kali systemd-entrypoint[27206]: WARNING: System::se>
Sep 03 16:58:22 kali systemd-entrypoint[27206]: WARNING: Please con>
Sep 03 16:58:22 kali systemd-entrypoint[27206]: WARNING: System::se>
Sep 03 16:59:03 kali systemd[1]: Started wazuh-indexer.service - Wa>
lines 1-21/21 (END)
                                                                    
┌──(root㉿kali)-[/home/kali]
└─# cd /etc/wazuh-indexer
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer]
└─# ls
certs                     opensearch-notifications-core
jvm.options               opensearch-observability
jvm.options.d             opensearch-performance-analyzer
log4j2.properties         opensearch-reports-scheduler
opensearch.keystore       opensearch-security
opensearch-notifications  opensearch.yml
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer]
└─# nano opensearch.yml                                        
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer]
└─# curl -so /etc/filebeat/wazuh-template.json https://raw.githubusercontent.com/wazuh/wazuh/4.5/extensions/elasticsearch/7.x/wazuh-template.json
chmod go+r /etc/filebeat/wazuh-template.json
                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer]
└─# systemctl status filebeat.service
● filebeat.service - Filebeat sends log files to Logstash or direct>
     Loaded: loaded (/lib/systemd/system/filebeat.service; enabled;>
     Active: active (running) since Sun 2023-09-03 17:26:52 EDT; 31>
       Docs: https://www.elastic.co/products/beats/filebeat
   Main PID: 85627 (filebeat)
      Tasks: 8 (limit: 2265)
     Memory: 11.9M
        CPU: 1.211s
     CGroup: /system.slice/filebeat.service
             └─85627 /usr/share/filebeat/bin/filebeat --environment>

Sep 03 17:26:52 kali systemd[1]: Started filebeat.service - Filebea>

                                                                    
┌──(root㉿kali)-[/etc/wazuh-indexer]
└─# filebeat test output
elasticsearch: https://192.168.2.136:9200...
  parse url... OK
  connection...
    parse host... OK
    dns lookup... OK                                                
    addresses: 192.168.2.136                                        
    dial up... OK
  TLS...                                                            
    security: server's certificate chain verification is enabled
    handshake... OK
    TLS version: TLSv1.3                                            
    dial up... OK
  talk to server... OK                                              
  version: 7.10.2                                                   
                  
