## Week 16 Homework 

#### Step 1: Google Dorking


- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is? Yes- Karl Fitzgerald

![image](https://user-images.githubusercontent.com/96030770/164365649-bc8f334b-f783-43a0-8219-f092ddab7690.png)

- How can this information be helpful to an attacker? Having access to all the executive & manager names allows the attacker to  to send phishing emails directly to any member of Altoro Mutual.

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

#### Step 4: Recon-ng

- Install the Recon module `xssed`. 
- Set the source to `demo.testfire.net`. 
- Run the module. 

Is Altoro Mutual vulnerable to XSS: 

### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- Command for Zenmap to run a service scan against the Metasploitable machine: 
 
- Bonus command to output results into a new text file named `zenmapscan.txt`:

- Zenmap vulnerability script command: 

- Once you have identified this vulnerability, answer the following questions for your client:
  1. What is the vulnerability:

  2. Why is it dangerous:

  3. What mitigation strategies can you recommendations for the client to protect their server:

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  

