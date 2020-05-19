# Anthem

[![N|Solid](https://tryhackme.com//img/THMlogo.png)](https://tryhackme.com/room/anthem)

Anthem is a Windows machine from TryHackMe. Some of skills required for this machine are:
  - Nmap
  - Web browser inspector
  - Some CMD commands
# WriteUp
### Task 1
Task 1 is for information gathering. Just deploy and start looking for clues. 
#### #1 to #3 
Just nmap usage. Nmap your deployed machine and search for some ports
#### #4  
In #4 you should investigate about web crawling methods. There is a specific file name used for web crawlers in other to gather information about a certain web page.
#### #5 to #6
If you've answered previous questions, this two would be easy
#### #7 to #8
There's a certain page which gives you a hint about the pattern used in email addresses. But how to know the email address without the name of the Administrator? Just Google everything out normal (a poem (?) ) and you'll find out the name.

### Task 2
Damn flags, spent two days looking for them. Use the web browser inspector to search for every flag. Almos all of them are found on the source code. Just one flag is found on meta tags inside Umbraco Client. Haven't log in on Umbraco? Use previous gathered information on Task 1 and you'll get in.

### Task 3
#### #1 to #2
Use Remmina to log in with the same user and password found on Task 1 and 2. That should led to user.txt. 
#### #3 to #4
Once logged in, open the file explorer and enable invisible files. You'll find a directory name "backup" with a restore.txt file inside. But oh no! we can't read it. Simple trick ma men (Google back me up). Use `icacls` on cmd prompt and reset all permissions on that file. Found admin password, found everything.

## You root the machine!

Look for more rooms on: https://tryhackme.com/

#### Some social media
- https://github.com/Andres20141684/TryHackMe-Writeups
- https://www.linkedin.com/in/andresvallenasarevalo/

See you around!
SandSlash