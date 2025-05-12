# Instructor's Guide — GOSSIP Lab

This lab tests the student's ability to detect vulnerabilities in a web application's login, exploit an SQL injection, crack passwords, and deduce through narrative analysis who sabotaged a coworker.

Through this lab, students will achieve an understanding of:

- Identification and exploitation of an SQL injection using SQLMap.
- Extraction and decryption of MD5 passwords.
- Narrative analysis of simulated user panels.
- Logical deduction from cross-messages.
- Accessing a final flag through realistic login usage.

## Machine Specifications 🖥️

- **System:** Ubuntu Server (no GUI)
- **Web Server:** Apache
- **Site Path:** `/var/www/html/gossip/`
- **Vulnerable Content:** Login form vulnerable to SQL Injection (`login.php`)
- **Database:** `gossip_db` with MD5 hashed users and passwords
- **System Users:** None, everything is web-based

- **Users in the database:**
    - Diego → coffee123 → `md5('coffee123')`
    - Sarah → password! → `md5('password!')`
    - Karen → trustno1 → `md5('trustno1')`
    - William → securepass → `md5('securepass')`

- **Flag accessible from the web panel of:** `William`
- **Flag content:** `4GEEKS{D13G0_Y0u_4re_f1red!!!}`

> **Note:** No privilege escalation or SSH connection is required.

### Machine Credentials

```bash
servername: gossip-lab
username: student
password: 4geeks-lab
```

## Expected Steps for the Student

1. **Perform network reconnaissance to identify the machine.**
     - Use tools like `nmap`, `netdiscover`, or `arp-scan`.
     - Identify an IP with port **80 (HTTP)** open.

2. **Access the website from the browser.**
     - Enter the discovered IP in the browser to load the Alabama Suites landing page.

3. **Identify the vulnerable form at `/gossip/login.php`.**
     - Manually input values to test its functionality.

4. **Use SQLMap to exploit the vulnerability.**
     - Extract the `gossip_db` database and the `users` table.
     - Retrieve the MD5 hashed passwords.

5. **Crack the passwords using John, Hashcat, or CrackStation.**
     - Obtain access credentials for users: Diego, Sarah, Karen, and William.

6. **Log in as each user and analyze the panel content.**
     - Read cross-messages and false or distracting content.

7. **Deduce that Karen sabotaged Diego.**
     - The justification appears in her panel in a message addressed to Freddy.

8. **Retrieve the flag from William's panel.**
     - The flag is clearly visible on his dashboard.

