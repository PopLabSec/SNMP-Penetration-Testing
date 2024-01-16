---
description: >-
  Discover the intricacies of SNMP enumeration in our latest article. Uncover
  how this key technique aids in network management & potentially exposes
  vulnerabilities.
cover: ../.gitbook/assets/SNMP  Penetration Testing.jpg
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Enumeration

Simple Network Management Protocol (SNMP) enumeration is a process used in penetration testing that involves collecting important data about network devices.&#x20;

This technique is used to find hosts’ information such as device type, system name, services running, etc.

### **Discovering SNMP-Enabled Devices:**

* **Enumeration:** The process begins with enumerating potential target IP addresses or network ranges.
* **Network Scanning:** Conducting network scans to identify hosts that respond to SNMP requests.

### **SNMP Version Detection:**

* **SNMPv1, SNMPv2c, SNMPv3:** Identifying the SNMP versions supported by the target devices. Different versions have varying levels of security features.

### **Community String Enumeration:**

* **Default and Common Strings:** Attempting to identify SNMP community strings associated with the target devices. Default or common community strings may provide unauthorized access.

### **Gathering Information:**

* **System Information:** Querying devices for system information, such as device names, descriptions, and contact details.
* **Interfaces:** Enumerating network interfaces and their statuses.
* **Configuration Data:** Extracting configuration details, including SNMP settings and other relevant parameters.

### **Mapping the Network:**

* **Device Relationships:** Understanding the relationships between SNMP-enabled devices on the network.
* **Topology Discovery:** Building a map of the network based on SNMP information.

\


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
