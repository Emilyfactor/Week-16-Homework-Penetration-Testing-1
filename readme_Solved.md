## Week 16 Homework 

#### Step 1: Google Dorking


- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is? Yes- Karl Fitzgerald

![image](https://user-images.githubusercontent.com/96030770/164365649-bc8f334b-f783-43a0-8219-f092ddab7690.png)

- How can this information be helpful to an attacker? Having access to all the executive & manager names allows the attacker to send phishing emails directly to any member of Altoro Mutual.

#### Step 2: DNS and Domain Discovery

Enter the IP address for `demo.testfire.net` into Domain Dossier and answer the following questions based on the results:

  1. Where is the company located: Sunnyvale, CA 94085

![image](https://user-images.githubusercontent.com/96030770/164366786-8bbdc639-02f4-4825-a2f9-f0952b08ed40.png)

  2. What is the NetRange IP address: 65.61.137.64 - 65.61.137.127

![image](https://user-images.githubusercontent.com/96030770/164366854-b590f500-36cf-4c6a-9f60-62208e84b358.png)

  3. What is the company they use to store their infrastructure: Rackspace Backbone Engineering

![image](https://user-images.githubusercontent.com/96030770/164366926-bc0051e1-4e69-416b-8191-e46316484d72.png)

  4. What is the IP address of the DNS server: 65.61.137.117

![image](https://user-images.githubusercontent.com/96030770/164366966-ba9b7386-30eb-4d5c-908d-903c0aaee310.png)


#### Step 3: Shodan

- What open ports and running services did Shodan find:

![image](https://user-images.githubusercontent.com/96030770/164367307-20ef55f3-dcdb-457e-86d8-3fa49b73e453.png)

#### Step 4: Recon-ng

![image](https://user-images.githubusercontent.com/96030770/164369621-e35afdcd-7369-45a1-ba7c-8dd0f7f9d5c2.png)

- Install the Recon module `xssed`. 

![image](https://user-images.githubusercontent.com/96030770/164369685-2d750f17-3bf8-4fef-a0fb-bbd8de1b5219.png)

![image](https://user-images.githubusercontent.com/96030770/164369727-4e4fb1fa-6ca2-480c-ae02-3168d70cf9d8.png)

![image](https://user-images.githubusercontent.com/96030770/164369845-41d09037-32a3-47b4-8323-9a30001ac314.png)

- Set the source to `demo.testfire.net`.

![image](https://user-images.githubusercontent.com/96030770/164369897-72f1f152-1a60-40f5-ad2a-328aa36794dd.png)

![image](https://user-images.githubusercontent.com/96030770/164369982-fe9e67c7-35d5-40c2-823d-930f084b6cf4.png)

- Run the module. 

![image](https://user-images.githubusercontent.com/96030770/164370450-1696f35e-7ff5-4968-8a04-cc5e3083666a.png)

Is Altoro Mutual vulnerable to XSS? Yes

![image](https://user-images.githubusercontent.com/96030770/164370390-91e5401a-e590-4c40-a386-c3a59ab71630.png)


### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- Command for Zenmap to run a service scan against the Metasploitable machine: 
 
![image](https://user-images.githubusercontent.com/96030770/164372545-a0a392f0-4af2-4d55-b52d-0549c40b59ad.png)

# Bonus 
  -In the same command, output the results into a new text file named zenmapscan.txt.

nmap -T4 -A -oN zenmapscan.txt 192.168.0.10

![image](https://user-images.githubusercontent.com/96030770/164375190-c1b7e7cd-e848-4e67-97cb-713f5738ae7d.png)


- Zenmap vulnerability script command: 

![image](https://user-images.githubusercontent.com/96030770/164373703-1b754c32-87e5-4568-9ef2-27432d9ead30.png)

- Once you have identified this vulnerability, answer the following questions for your client:
  1. What is the vulnerability? Zenmap is able to enumerate the vulnerable serive ports: 

![image](https://user-images.githubusercontent.com/96030770/164373752-2508e548-0df0-473a-b1d5-34b86e64a241.png)

![image](https://user-images.githubusercontent.com/96030770/164374151-0760994f-f192-450d-b659-251d3ebc3b93.png)

![image](https://user-images.githubusercontent.com/96030770/164374184-a27a824d-95ae-4189-9390-4fd94ba73646.png)

  2. Why is it dangerous? It allows the hacker to load a backdoor attack using VSFTPD 2.3.4. This attack will trigger the malicious code by sending a sequence of specific bytes on port 21, if successful, will result in opening the backdoor on port 6200 of the system and running as root. 

  3. What mitigation strategies can you recommendations for the client to protect their server? After being reported, patches were released by Microsoft (MS17--10) and Red Had for Linux (RHSA-2017:1390 5,6,& 7). The vsFPTD 2.3.4 patch was released on July 3, 2011 followed by Red Had's version these patches are constantly monitered and updated. Another recommendation is to run file audits on your system to determine all files and records are in a good state. This is used to detect changes to the system that may have been authorized. Intrusion detection (IDS) is a software that monitors a system or network for unauthorized activity.  

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  

