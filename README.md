# Try Hack Me Solutions

[tryhackme.com](https://tryhackme.com/) is a website containing cyber security problems/questions. 

Try Hack Me is organized into rooms that might have many problems relating to a central theme. To attempt the problems, one needs to open a connection to AttackBox, a web-based connection to a Kali machine. Alternatively you can use OpenVPN. For free users there exists a time limit on using the machine, but people with subscriptions, it is unlimited max machine open is 3. 



## Path

1. Start with the tutorial which will help you set up
2. Next do an easy challenges such as [Vulnversity](https://tryhackme.com/room/vulnversity) although this one is a bit long ans something like [Web Fundamentals](https://tryhackme.com/room/webfundamentals) might be easier 
3. Do some more easy/tutorial ones to get your feet wet



<a name=top></a>

## Index

1. [Tutorial](#begin)
2. [Web Fundamentals](#webf)
3. [Vulnversity](#vulnversity)
4. [Burp Suite](#burp)



<a name=begin></a>

### [Tutorial](https://tryhackme.com/room/tutorial)

1. Start a machine, this will take ~ 1-2 minutes for pro accounts
2. (Recommended) have two windows if 2+ monitors, 1 for Kali Linux window and another for the instructions
3. Follow instructions to get the flag and submit it



<a name=webf></a>

### [Web Fundamentals](https://tryhackme.com/room/webfundamentals)

Good place to start out

Instead of using curl in the command line, using postman to send requests might be easier



<a name=vulnversity></a>

### [Vulnversity](https://tryhackme.com/room/vulnversity)

1. Run `nmap -A -sC -p- -oN vul.nmap 10.10.IP ADDRESS HERE*` on the instance of Kali 

2. Wait >10 minutes for it to resolve

3. Scan for hidden files by doing `gobuster dir -u http://<ip>:3333 -w /usr/share/wordlists`

4. Go to the \<ip>/internal/index.html on firefox (**Make sure u aren't using http or https before the url**)

5. Follow the rest of the steps till yo get to injecting the PHP code

6. Make sure download the PHP file from GitHub, rename it to be a .phtml and change the IP to the TMP IP address

   ![screen1](./img/screen1.png)

7. Save, upload, listen, then submit file

8. Then the netcat should allow you in such that you can gain control and find out things about the machine

9. Follow https://n0w4n.nl/vulnversity/#crayon-60458bd07482b875406373 to gain admin privileges

10. Follow the rest of the instructions and you should be done! 🥳

Resources: 

* https://n0w4n.nl/vulnversity/
* https://www.youtube.com/watch?v=hvYWCegfEZs&ab_channel=JohnHammond



<a name=burp></a>

### [Burp Suite](https://tryhackme.com/room/rpburpsuite)

Follow instructions, mostly straight forward

Task 6 (some step in the middle) the question that starts with "Return to your web browser and navigate to the web application hosted on the VM we deployed just a bit ago", implies localhost:8080, but does not work, literally just do tryhackme.com for that one request



## OpenVPN

1. Download OpenVPN and install it
2. Download the configuration files from TryHackMe
3. Load the config file onto OpenVPN
4. Connect
5. ssh into server



🔝[Back to Top](#top)