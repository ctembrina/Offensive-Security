<h1>Offensive Security</h1>



<h2>Description</h2>
Offensive Security - VM
(Breaking into computer systems, exploiting software bugs, and finding loopholes in applications to gain unauthorized access.
<br />


<h2>Utilities Used</h2>

- <b>TryHackMe VM</b> 
- <b>GoBuster</b>



<h2>Lab walk-through:</h2>

<p align="center">
Using the VM, accessed the fakebank site, opened the terminal by clicking on the Terminal icon on the right of the screen:
  
<br/>
<img src="https://i.imgur.com/zHfInJD.png"height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Using a command-line security application (GoBuster) I used the following command into the terminal to find potential hidden pages on the FakeBank's website. 
Command = gobuster -u http://fakebank.thm -w wordlist.txt dir
(Gobuster scans the website with each word in the list, finding pages that exist on the site also shows the pages in the list of page/directory names status: 200 )
<br />
<img src="https://i.imgur.com/oscRdzz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Found a vulnerability in the report above in the application, an exploit to the Bank. There is a secret bank transfer page found. 
http://fakebank.htm/bank-transfer ( providing a access to steal from a bank account) 

<br/>
<img src="https://i.imgur.com/YtQJT3Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
The exploit allowed funds to be transferred from one account to another.
<br/>
<img src="https://i.imgur.com/dmavw0I.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Account page showing a successful transfer:  <br/>
<img src="https://i.imgur.com/6UDGvJv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />



<h2>Final Comments</h2>

Attacker was using Gobuster (a fast directory / vhost / DNS brute-forcing tool)

For a financial bank these are the most critical data to protect -

PII (identity theft risk)

Account & payment card data (fraud/theft risk)

Authentication credentials & biometrics (account takeover risk)

Transaction records & financial logs (integrity risk)

Internal & regulatory data (compliance and reputational risk)

MY recommendation is to lean on multiple frameworks for some secure coding, some compliance, and some for operational control -  

Dev/Secure coding → OWASP Top 10 + ASVS.

Enterprise security controls → NIST CSF + CIS Controls.

Compliance → PCI DSS, ISO 27001, SOX (depending on regulatory requirements).

Banking-specific oversight → FFIEC Cybersecurity Framework.



<h2>TryHackMe Lab Completion</h2>
<br/>
<img src="https://i.imgur.com/gyXSiIf.png"height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />



