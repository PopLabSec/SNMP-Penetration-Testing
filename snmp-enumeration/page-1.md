# Page 1

Discover devices with default community strings:msf > use auxiliary/scanner/snmp/snmp\_loginmsf > set PASSWORD publicmsf > set RHOSTS file:snmp.txtmsf > set THREADS 25msf > set VERBOSE falsemsf > set VERSION 2cmsf > run

### onesixtyone <a href="#onesixtyone" id="onesixtyone"></a>

* ​[https://github.com/trailofbits/onesixtyone](https://github.com/trailofbits/onesixtyone)​

Brute force community strings:$ onesixtyone -c /usr/share/seclists/Discovery/SNMP/snmp.txt 10.10.13.37

### snmp-check <a href="#snmp-check" id="snmp-check"></a>

Collect data:$ snmp-check -v 2c -c public 10.10.13.37$ for i in \`seq 1 254\`; do snmp-check -v 2c -c public -t1 10.10.13.$i | grep -aA2 'System information'; done

### snmpwn <a href="#snmpwn" id="snmpwn"></a>

* ​[https://github.com/hatlord/snmpwn](https://github.com/hatlord/snmpwn)​

$ ./snmpwn.rb --hosts hosts.txt --users users.txt --passlist passwords.txt --enclist passwords.txt
