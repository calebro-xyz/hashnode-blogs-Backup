## NMAP overview - A beginner's guide

### Introduction

NMAP? What is Nmap? Nmap is an open-source tool for monitoring, discovering, and troubleshooting network systems. It is a popular and resourceful tool if you are into network security, web security, or system administration.

NMAP comes pre-installed in many security-focused Linux distributions, but if you are on a different operating system or you would like to compile from the source code you can find it here on their [official website.](https://nmap.org)

#### Prerequisites

Before we start, it is vital to note the following:

1. NMAP is case sensitive

2. Always try and find the original IP of the host you want to scan (some host hide behind CDN or honeypots, hence you will not get the desired results)

3. The IP addresses used in this tutorial belong to google.com and are available in the public domain. It's not advisable to pock into networks you are not authorized to do so.

Let us begin.

### Basic scanning techniques

#### Scanning a single host

To scan a single host you provide the IP or the web address of the host you want to scan. **We will use google's public DNS IP for obvious reasons.**

```bash
$nmap 216.58.223.110
```

From the results, we can see that Nmap tries to identify the open ports and the services that run and if they are open, closed, or filtered.

```bash

Starting Nmap 7.80 ( https://nmap.org ) at 2021-06-26 04:14 EAT
Nmap scan report for mba01s08-in-f14.1e100.net (216.58.223.110)
Host is up (0.017s latency).
Not shown: 998 filtered ports
PORT STATE SERVICE
80/tcp open http
443/tcp open https


```

#### scanning several hosts

During reconnaissance, you may have more than one host or a list of hosts you want to scan, scanning one at a time might be very slow or just tedious.

Here are ways you can scan more than one host. Try this on your CLI and see what results you get.

**scanning more than one host**
```bash
$nmap 216.58.223.110 216.58.223.109
```

**scanning a range of IP**
```bash
$nmap 64.233.160.0 - 255
```

**scanning a subnet**
```bash
$nmap 64.233.160.0/24
```

**scanning from a list**
```bash
$nmap -iL list.txt
```


### Useful arguments that NMAP takes?

-iR 5 - Say you were scanning from a list, this arguments will tell Nmap to pick five random hosts from that list

-A - This is for aggressive scan

-PN - scan without ping. (Ping is the time it takes for a packet to be transmitted from your device to a host on the network and back to your device again.)

If you want to save the results from the scan you are conducting using the following arguments -oX to save the output in an XML file or -oN to save the output in a text file.


#### Port Scanning

Port scanning is the technique used to discover open/closed ports and services running in a network. Port scanning lets you understand a host better and possible vulnerabilities to exploit.

***Popular ports you should know***

23- Telnet

53- Domain Name System (DNS)

80/8080- Hypertext Transfer Protocol (HTTP)

3306- MySQL Database

443- HTTP with Secure Sockets Layer (SSL)


**General port scanning**

```bash
$nmap google.com
```

**scan commonly used ports**

```bash
$nmap -f google.com
```

**scan a specific port**
```bash
$nmap -p 8080 google.com
```

**scan multiple specific port**
```bash
$nmap -p 8080,443,23,3000 google.com
```

**scan multiple port by name**
```bash
$nmap -p smtp,https,http google.com
```

**scanning all port**
```bash
$nmap -p "*" google.com
```

#### Firewall evasion

The is no doubt most network administrators will try to come up with an intrusion protective mechanism for the network, this is to prevent attackers from having a precise map of their network. Let's try and look for ways in which we can try and evade possible firewalls.

**Randomizing hosts from a range**

Using Nmap with '--randomize-hosts' argument randomizes the scanning order of the specified targets.

```bash
$nmap --randomize-hosts 64.233.160.0 - 255
```

**Spoof MAC Address**

For this scan, Nmap is instructed to generate a randomly generated MAC address. This makes your scanning activity difficult to trace by preventing your MAC address from being black-listed or banned by the system.

```bash
$nmap -sT -PN --spoof-mac 0 216.58.223.109
```

**Use a Decoy**

The -D argument is used to hide a Nmap scan by using one or more decoys. When performing a decoy scan Nmap will spoof additional packets from the specified number of decoy addresses. This makes it appear that the target is being scanned by multiple systems at the same time.

```bash
$nmap -D RND:10 216.58.223.109
```


#### Conclusion

I believe this blog post has shed some light on the use of the Nmap tool, especially if you are a beginner. Try doing this and let me know in the comment section what your thoughts are.

Happy hacking guys!