---
description: >-
  Discover the intricacies of SNMP enumeration in our latest article. Uncover
  how this key technique aids in network management & potentially exposing
  vulnerabilities.
---

# Enumeration

### onesixtyone <a href="#onesixtyone" id="onesixtyone"></a>

* ​[https://github.com/trailofbits/onesixtyone](https://github.com/trailofbits/onesixtyone)​

Brute force community strings:$ onesixtyone -c /usr/share/seclists/Discovery/SNMP/snmp.txt 10.10.13.37

### snmp-check <a href="#snmp-check" id="snmp-check"></a>

{% code overflow="wrap" %}
```
snmp-check -v 2c -c public 10.10.13.37$ for i in `seq 1 254`; do snmp-check -v 2c -c public -t1 10.10.13.$i | grep -aA2 'System information'; done
```
{% endcode %}

### snmpwn <a href="#snmpwn" id="snmpwn"></a>

* ​[https://github.com/hatlord/snmpwn](https://github.com/hatlord/snmpwn)​

$ ./snmpwn.rb --hosts hosts.txt --users users.txt --passlist passwords.txt --enclist passwords.txt

```
snmp -v 2c -c public 192.241.218.3 .1.3.6.1.2.1.2 | grep STRING
```

{% embed url="https://attack.mitre.org/techniques/T1016/" %}

{% embed url="https://nmap.org/nsedoc/scripts/snmp-interfaces.html" %}

{% embed url="https://linux.die.net/man/1/snmpwalk" %}
