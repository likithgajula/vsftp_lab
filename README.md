# 💣 Metasploitable 2 VSFTPD 2.3.4 Exploit Lab

Welcome to my documented penetration testing lab focused on exploiting the vulnerable **vsftpd 2.3.4 FTP service** on Metasploitable 2 using the **Metasploit Framework**.

This repository aims to help beginners get hands-on experience with:

- Setting up a local ethical hacking lab  
- Scanning and enumerating vulnerable services  
- Exploiting a known vulnerability  
- Basic post-exploitation techniques  

---

## 🔥 About the Lab

The lab simulates a real-world scenario where an attacker identifies an exploitable FTP service and gains shell access by exploiting a backdoor vulnerability in vsftpd 2.3.4 (CVE-2011-2523).

---

## 🧰 Tools & Components Used

| Tool/OS           | Role                      |
|-------------------|---------------------------|
| Kali Linux        | Attacker machine          |
| Metasploitable 2  | Vulnerable target VM      |
| VirtualBox/VMware | Virtualization environment|
| Nmap              | Network scanning & enumeration |
| Metasploit        | Exploitation framework    |

---

## 🚦 Network Setup

- Both attacker and target VMs are configured on the same **Host-Only** or **Internal Network** in your virtualization platform.
- Use commands like `ifconfig` or `ip a` to find the IPs.
- Confirm connectivity by pinging the target machine.

---

## 📂 Repository Structure

/
├── README.md # This overview file
├── LAB_GUIDE.md # Detailed step-by-step lab walkthrough
└── images/ # Folder containing screenshots
  ├── nmap.png
  ├── msf.png
  ├── shell.png
  └── post_exploit.png
/
  
---

## 📖 How to Use This Repo

1. Start by reading through the **LAB_GUIDE.md** for a complete walkthrough.  
2. Follow each step on your local VM setup.  
3. Refer to the screenshots in the `images/` folder to visually confirm your progress.  
4. Experiment with additional vulnerable services as outlined in the guide for practice.  

---

## ⚠️ Disclaimer

This project is intended strictly for educational and ethical purposes.  
Do not use these techniques against unauthorized systems or networks.  
Always practice in isolated, controlled lab environments.

---

## 🙌 Acknowledgments

- Offensive Security for creating Metasploitable  
- The Metasploit Framework developers  
- The open cybersecurity community for shared learning  

---

⭐ If you found this helpful, please ⭐ star the repo, share it with peers, and fork to contribute improvements!

---

Feel free to open issues or pull requests for feedback and enhancements.

---

Happy hacking! 🚀
