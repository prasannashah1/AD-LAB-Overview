# Active Directory LAB Overview
![wsps](https://github.com/prasannashah1/AD-LAB-Overview/assets/28432698/b0a98434-b965-4545-90fe-d12d9cb23501)<br><br>

<h1>Introduction</h1>
In this lab I created two virtual machines on my virtualbox to simulate Active Directory environment using Windows Server 2019 as a Domain Controller and Windows 10 as a workstation to connect to the Domain Controller. After completing all the required network configurations such as staic IP assignment, DHCP, FQDN I used a powershell script to create 1000 users and connected workstation to the domain controller and logged in with one user created through the powershell script.

<h1>Process</h1>
First I downloaded virtual box, installed it on my computer. Then I downloaded the iso image of both Windows server 2019 and Windows 10. I installed both of the image to the virtualbox.<br><br>
After the installation, I assigned both the virtual machines with Nat Network. First I started with the configuration of Windows Server 2019. I assigned static IP address to the Server, installed ADDS (Active Directory Domain Service), assigned FQDN <b>(mydomain.com)</b> to make it a Domain Controller.<br><br>
For the workstation I assigned it with the DNS address of the IP address of the server so that it could establish connection with the Domain Controller. Then I assgined the workstation with the domain name (mydoamin.com) to make it a memeber of Domain Controller.<br><br>
Now it was time to create a bulk user on ther server. I used a script found on github to create 1000 users on the Domain Controller. For this I used random name generator to create 1000 users. The script and names can be accessed from here (https://github.com/prasannashah1/PowerShell). The screenshot of the user creation using powershell script is shown below:<br><br>

![psuser](https://github.com/prasannashah1/AD-LAB-Overview/assets/28432698/3e7ba94c-061b-4396-bd0f-fa337ed94948)<br>

![psuser1](https://github.com/prasannashah1/AD-LAB-Overview/assets/28432698/368320dc-a5cd-449b-8860-d5a2ce7c9701)<br>

Since the user has been created, it's time to try to login with one of the user. I tried to login with the user with username <b>acoke</b>, the user was successfully logged in from the workstation that was the memeber of the Domain Controller.<br>

![psuser2](https://github.com/prasannashah1/AD-LAB-Overview/assets/28432698/237dde3b-46af-467e-80a6-30a249e84625)<br>

<h1>Conclusion</h1>
In this lab I created Active Directory Environment and also used powershell to create bulk users. I found out Powershell to be the most powerful tool, that can do many things, it saved my lot of work to create users as well as assign username, password, permission to the users. This was a great project for me, I will further try to explore more about Active Directoy such as group policy, password policy, software installation and more.

