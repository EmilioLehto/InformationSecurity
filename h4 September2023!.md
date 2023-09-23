-h4 September2023!

x) Read or watch and summarize (This subtask x does not require tests with a computer. Some bullets per article is enough for your summary, feel free to write more if you like)
€ Schneier 2015: Applied Cryptography: 2.3 One-Way Functions and 2.4 One-Way Hash Functions.
	2.3 one way functions:  A one way function in simple terms is a function that is easy to compute in one way but difficult to compute the other way. Event though it is hard to compute backwards we want a method that makes it easier, this is where a trapdoor  one way function comes at hand. Without the trapdoor function it would be useless to use a one way function as they would be almost impossible to decrypt. 
	2.4 one way hash function: A hash function accepts a variable-size message “W” as input  called the pre-image and produces a fixed size message digest J(W) as output called the hash value. 
A good hash function is also collision free, meaning that is hard to generate two pre-images with the same hash value. It I just naturally very unlikely that they will have the same hash value. 
 There is no secrecy in the process and the value of a hash function is on its one-wayness. 
Message authentication codes (MAC):  is data authentication code (DAC),  that holds on top of a one way hash function also a secret key. Only the individual with the key can decrypt the hash function. 

Särökaari 2018: Phishing trough email (video, 33 min)

The video seminar gave in-depth information on what is phishing, why do individuals practice it, how before from any phishing attacks, how to do it, and the statistics that he found in his research when sending phishing emails. 
Firstly, what is phishing and why individuals do it? 
Phishing is the practice of sending emails that appear to come from a reputable source (colleagues, friends, family, or company one works in), to gain influence over ones personal data or to send malicious attachments to illegitimate sites to cause harm on the individual. 
Why do individuals click phishing links?
Contrary to popular belief individuals are well aware of the possibility of phishing links, however they tested sending phishing links to 1200 students and asked the people who clicked it why they did it, 34% clicked the link because of curiosity. A fact I found astounding. 
What to beware? 
It was recommended to use SPF and DMARC to combat against phshing emails and that these methods would throw a majority of the malicious emails into the spam box as the technology will check if the email and domain is from a reputable and legitimate source. However this can be used to ones detriment if the attacker gets a domain name that can fool one by being close enough to the original one and configure SPF and DKIM in their systems then it can bypass the original point. 
It is also recommended to use URL whitelisting to have only specific domains allowed in your email and everything else is blocked.


a) Install Hashcat. Test it with a sample hash. See Karvinen 2022: Cracking Passwords with Hashcat

step one:
-First I need to update my system before i can start installing hashcat by putting the command "sudo apt-get update" and adding my password 

![IMG_9072](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/422e2ef9-4bed-42fd-a487-328effa27cb9)
![IMG_9073](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/28e01b30-45fb-4ec9-8c5b-a537fda69519)


Step two: 
- now after the update i can install hashcat by putting the command "sudo apt-get -y install hashid hashcat wget"
  ![IMG_9074](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/7c8298dc-8994-4e14-8ee2-46b8a5e781d2)


Step three: 
-I then add the commands "mkdir hashed" and "cd hashed"
![IMG_9076](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/83751054-3790-474b-bf70-97efef248686)


Step four: 
- I then want to install the library that will hold all the word, letter and number list from github by using the command: "wget https://github.com/danielmiessler/SecList/raw/Passwords/Leaked-Databases/rockyou.txt.tat.gz. This will install the rockyou.txt.tar.gz library into the hashcat.
![IMG_9078](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/6f0a60c7-81d7-4e74-b698-402a667a563b)


Step five:
-Now that we have the library we could use an example of a hash that we would like to crack. this hash is 6b1628b016dff46e6fa35684be6acc96 and we will use the command "hashid -m 6b1628b016dff46e6fa35684be6acc96" to see the options in our disposal that we can use. 
![IMG_9080](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/00a4aff8-548e-4b20-abe7-68733ed49485)

Step six: 
-We will now use the command 'hashcat -m 0 '6b1628b016dff46e6fa35684be6acc96' rockyou.txt -0 solved 
from this command it will test the first library of keywords if any of them match to the password. and hopefully we will get it to crack or move to the next library.
![IMG_9082](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/97e37d34-f7a0-4854-ad78-ee783fe5ea20)


b) Crack this hash: 8eb8e307a6d649bc7fb51443a06a216f

I used the same method as from the last exercise to crack this hash.
![IMG_9084](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/729561e2-bcd4-4e56-84c6-a80b1309b4ce)
![IMG_9085](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/b587c812-9ade-444f-bd7c-e4b9cb500363)


c) Gone phising. Create a phising email. In addition to the email, you must explain your tactics and the scennario where the phising email is used. (This subtasks does not require tests with a computer).

I decided to use our teachers name and last name for my phishing email as that would be the easiest for me to exploit as I already know the students he teaches and some of his colleagues. I would use this email to send some malicious websites that the students would click to release malware. I could for example send an email letting the students know about an extra assignment or extra information for the course and in that, there would be a malicious link. 
I can imagine this wont work for all students but a quantity might fall becasue of curiosity or just because they didnt pay much attention on the email. 
![image](https://github.com/EmilioLehto/InformationSecurity/assets/113890358/0007b0e1-d317-4e0f-81cf-fb5c28987422)



