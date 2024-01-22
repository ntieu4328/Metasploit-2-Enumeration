<h1>Metasploit 2 Enumeration</h1>

<h2>Description</h2>
The project consists of the enumeration of the Metasploitable 2 system. Enumeration is extracting information from a system. The information that is gained can be used to exploit or fix vulnerabilities. I will do this enumeration as if I were a threat actor trying to exploit the Metasploitable 2 system. The Kali Linux machine that was made will be the attacking machine, so everything will be done on that machine.

<h2>Walk-through:</h2>

<h3>Terminal Enumeration</h3>

Discover the machine:
```bash
netdiscover
```
This command will scan the network and see what systems are on it.
![netdiscover](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/af912537-1e3f-4200-a47b-4b0181eeb700)
</br>
</br>

Ping the IP:
```bash
ping 10.0.2.4
```
This is to make sure that we can connect to the system. This is also to make sure that we can send and receive packets.
![ping](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/4ad99a29-51b2-4b0e-973d-117e78611030)
</br>
</br>

Discover what ports are open:
```bash
sudo nmap -sV 10.0.2.4
```
The -sV option added to nmap returns the open ports and show what service/version it is.
![nmap sV](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/9f2896bc-b1ab-4475-a720-ba567b459a6f)
![nmap](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/14e9a626-5889-4aed-886d-9cbc36252471)

<h3>Nessus Enumeration</h3>
Create new scan:

![nessus dashboard_LI](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/335ed479-ff04-4cfc-9831-fecb1b947263)

Choose Advanced Scan:

![Advanced Scan](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/6cf5f9af-fc63-4a84-bdab-6097128cf747)

Name the scan and put the IP of the Metasploitable 2 system:

![name   targets](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/a8728a0c-c26c-4161-92e8-c0b030066ba4)

Discovery -> Host Discovery -> Use fast network discovery:

![use fast network discovery](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/c95288b5-0c09-4627-912c-193df77bac26)

Discovery -> Port Scanning -> TCP:

![Network Port scanners TCP](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/3e95a749-bef2-4531-a6b5-f14bc58c4b2e)

Leave everything else as default.

Click on the scan that you created and launch:

![launch scan](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/4d638911-18cd-4d3b-8bf9-39ed66d27866)

My results:

![nessus scan](https://github.com/ntieu4328/Metasploit-2-Enumeration/assets/156137990/b8a004d6-6571-4d84-b722-41fab6b3e6a4)

You can look through each vulnerability that Nessus identifies. Nessus gives you a description of the vulnerability and how threat actors can exploit it. Nessus also gives you solutions on how to fix the vulnerability.

<b>You have finished the enumeration process. Let's start hacking!!!!!!</b>
