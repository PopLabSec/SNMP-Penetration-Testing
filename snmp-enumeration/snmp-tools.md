---
description: >-
  xplore our comprehensive article that delves into SNMP hacking tools, offering
  detailed insights into their usage, tactics, and preventive strategies against
  potential threats.
---

# SNMP Tools

### MsfConsole

```
auxiliary/scanner/misc/oki_scanner                                    
 auxiliary/scanner/snmp/aix_version                                   
 auxiliary/scanner/snmp/arris_dg950                                   
 auxiliary/scanner/snmp/brocade_enumhash                               
 auxiliary/scanner/snmp/cisco_config_tftp                               
 auxiliary/scanner/snmp/cisco_upload_file                              
 auxiliary/scanner/snmp/cnpilot_r_snmp_loot                             
 auxiliary/scanner/snmp/epmp1000_snmp_loot                             
 auxiliary/scanner/snmp/netopia_enum                                    
 auxiliary/scanner/snmp/sbg6580_enum                                 
 auxiliary/scanner/snmp/snmp_enum                                 
 auxiliary/scanner/snmp/snmp_enum_hp_laserjet                           
 auxiliary/scanner/snmp/snmp_enumshares                                
 auxiliary/scanner/snmp/snmp_enumusers                                 
 auxiliary/scanner/snmp/snmp_login
```

### Impacket

```
python3 samdump.py SNMP 172.21.0.0 
```

### Nmap

{% code overflow="wrap" %}
```
nmap -vv -sV -sU -Pn -p 161,162 --script=snmp-netstat,snmp-processes 10.11.1.111
```
{% endcode %}

{% code overflow="wrap" %}
```
nmap 10.11.1.111 -Pn -sU -p 161 --script=snmp-brute,snmp-hh3c-logins,snmp-info,snmp-interfaces,snmp-ios-config,snmp-netstat,snmp-processes,snmp-sysdescr,snmp-win32-services,snmp-win32-shares,snmp-win32-software,snmp-win32-users
```
{% endcode %}

### SNMP-Walk

```
snmpwalk -c public -v1 ipaddress 1
snmpwalk -c private -v1 ipaddress 1
snmpwalk -c manager -v1 ipaddress 1
```

OneSixtyOne

SNMP Check

Hydra Brute Force
