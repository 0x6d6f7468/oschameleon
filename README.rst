===========
OSChameleon
===========

| **OS Fingerprint Obfuscation for modern Linux  Kernels.**
| *Author: Anton Hinterleitner is111012@fhstp.ac.at*

Description: Fools the probes of nmap scanner

Prerequisites:
 * Linux (tested with Debian/Ubuntu)
 * Python 2.7+, 3.6+
 * python-nfqueue=0.6 (currently need to install library manually from https://github.com/sruon/nfqueue-bindings-py3)
 * requirements.txt

Recorded logs are stored to:
    /var/log/honeypot/

Usage:
    sudo python3.6 oschameleonRun.py
        --template      path to the nmap fingerprint, either absolute or relative to the execution folder
        --server        sets an exception for the iptables to access over ssh. the ssh port should either be changed to 63712 or the port number in stack_packet/helper.py
        --public_ip     either fetches the server public ip or gets the ip set for the interface
        --interface     the network interface
        --debug         debugging output


**Note: This script flushes iptables before and after usage!**
