# GOSSIP - Alabama Suites Internal Panel

Welcome to **GOSSIP**, a lab where you will test your skills in detecting SQL injection vulnerabilities, cracking passwords, and reading between the lines to uncover the real saboteur.

This application simulates the internal system of a corporate hotel called **Alabama Suites**, where everything seems calm... until you start digging into the data. Your goal will be to access the application's database, retrieve all user passwords, log in as each user, and **discover who is sabotaging Diego**.

<how-to-start>
   
## 🌱 How to Start This Lab

Follow these instructions to get started:

1. **Download the virtual machine** from this [link](https://storage.googleapis.com/cybersecurity-machines/gossip-lab.ova).
2. **Import the machine** into your preferred virtualization manager (VirtualBox, VMware, etc.).
3. Once the machine is running, you can start the lab!

</how-to-start>

## 📄 Instructions

1. **Discover the machine's IP address**: Use tools like `nmap`, `netdiscover`, or `arp-scan`.

2. **Scan the open ports**  

3. **Visit the webpage in your browser**: Go to `http://<IP>/gossip/` and explore the portal.

4. **Test the login at `/gossip/login.php`**: Not everything is as it seems... use SQLMap! 😉

5. **Use SQLMap to exploit the SQL injection**: Extract the `users` table and retrieve the passwords.

6. **Crack the MD5 passwords**

7. **Uncover the truth**: Read each user's panel and deduce **who is sabotaging Diego?**

Happy hacking!

