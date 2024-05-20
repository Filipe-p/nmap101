# Nmap 101

´namp´ is a wildly use network scanning tool that has survived the test of time, is maintained and open source. You can perform host discovery, port scanning and guess operating system. We'll also look at how to manipulate and store the output.

### Agenda

- Disclaimer
- Pre requisists 
- Installing namo
- Basic Usage
- Host Discovery, DNS, TCP, UDP
- OS detection, Fingerprinting, Throtling
- 

### Disclaimer

Remember scanning a network is likely to trigger alarms with your thorough request. Create a simple local network or prob servers that have been setup for this purpose.

### Pre requisits

- namp
- network to scan 
- Linux fundamentals

### Installing nmap

Linux system
```bash
$ sudo apt install nmap
```

You can also built from source or install distro/OS specific https://nmap.org/download.html


### Basic Usage

Basics usage is the following 


```python
# Syntax

$ nmap -flags-opt <ip/submask>

# example scanning ip range using submask
$ nmap 192.168.1.0/29  

```




#### Host Discovery, DNS, TCP, UDP




#### OS & Service Version Discover

```python
# -sV flag

$ namp -sV scan3.certmike.com

# Very Verbose, Service discovery, write plain text to file, seach scan2.certmike.com
$ namp -vV -sV -oN certmikr-scan2-os_discovery-read.txt scan2.certmike.com

```


#### Speed / Throtle of Scanning

Easiest way is using timing templates

| Template | Description               |
|----------|---------------------------|
| -T5      | Insane                    |
| -T4      | Aggressive                |
| -T3      | Normal                    |
| -T2      | Polite                    |
| -T1      | Sneaky                    |
| -T0      | Paranoid (mostly useless) |

```python
# Using insane timing template
$ nmap -T5 192.168.1.0/29  

```


