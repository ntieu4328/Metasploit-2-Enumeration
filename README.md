<h1>Metasploit 2 Enumeration</h1>

<h2>Description</h2>
The project consists of the enumeration of the Metasploitable 2 system. Enumeration is extracting information from a system. The information that is gained can be used to exploit or fix vulnerabilities. I will do this enumeration as if I were a threat actor trying to exploit the Metasploitable 2 system. The Kali Linux machine that was made will be the attacking machine, so everything will be done on that machine.

<h2>Walk-through:</h2>

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
This is to make sure that we can connect to the system and that we can send and receive packets.
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
