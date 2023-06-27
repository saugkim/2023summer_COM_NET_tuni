## Laboratory exercise (remote)

Laboratory work is graded pass/fail and is mandatory to complete the course.

Previously completed laboratory work is valid if there is a record of it in Sisu or Moodle. A previous record may not work correctly with Sisu automation, so please contact Jani if the overall grade does not appear the next day after completing all parts.

Laboratory work is completed remotely using the network simulator GNS3, protocol analyzer Wireshark and an OpenVPN remote connection. 

It is preferred if you can install the software on your computer. We can provide a remote desktop connection (RDP via SSH tunnel) to a virtual machine which has the required software installed upon request.

Remote laboratory exercise can be completed in groups of 1-2 students.  
All group members can work remotely on the same GNS3 project in real time.

Official due date is Thursday, August 31st, at 23:59.

**Pre-lab quiz**  
This quiz tests your readiness for the lab. Some questions might require learning some additional practical knowledge.

You should score over 85% in this quiz in order to pass. There are unlimited attempts.


**Instructions for setting up the remote connection and simulator**  
Instructions are located in the COMM.NET Labs meta course. 

**Remote laboratory instructions**  
Version 2023-06-07: Fixed incorrect network on page 10

**Report submission / Credit for laboratory exercise**   
Follow the instructions and compile a report from the answers in PDF format in English or Finnish  
     - Report style is free form  
     - Short answers are enough (about 1-3 sentences per question)  
     - List all used sources! A simple list is enough. Plagiarism = automatic failure and possible additional consequences  

Save the device configurations as text files or screen captures

Submit two items:  
     - The report in PDF format (should not be zipped)  
     - Configurations (7 configs) zipped in one archive or include the configurations at the end of the report  
    
All group members must submit the report; report must include names of group members

Graded pass/fail. Passing mark is a working implementation and about 66% correct answers.  
     - Failed reports can be resubmitted once if submitted before the due date.  
     - Reports are usually checked within 1-2 weeks(Exception: Reports submitted between June 16th and July 31st will be checked in early August).  


### How to Install & Setup OpenVPN on Windows 11

by ProgrammingKnowledge2  
https://www.youtube.com/watch?v=90w-Q27hX74

configuration and certificate bundle from the links below  
https://www.vpnbook.com/freevpn

IP addresses  
https://jodies.de/ipcalc?host=10.0.2.0&mask1=24&mask2=


http://172.16.253.1:3080/static/web-ui/server/1/projects

Kim_41523769722



### Remote connection quick start guide

**OpenVPN:**

Install an OpenVPN client: OpenVPN GUI (Windows https://openvpn.net/community-downloads/) or OpenVPN Connect (macOS https://openvpn.net/client-connect-vpn-for-mac-os/)

Establish the VPN connection using the following config file: GNS3.ovpn (Right-click link and Save link as, or copy and paste the contents to a text editor and save it as an .ovpn file)
(If you chose Save as) Check that the file was saved properly, and not as a web page.

If the connection works, you should be able to use a browser to connect to   http://172.16.253.1:3080/

You could in theory do the exercise with the Web GUI, but it's not recommended nor officially supported.


**GNS3:**

```
1. Install GNS3 version 2.2.39 (other versions do not work with our server). 

GitHub links (Windows, Mac, source code) https://github.com/GNS3/gns3-gui/releases/tag/v2.2.39

Linux instructions
    - IOU and Docker support are not needed.
    - In short: either add the repo and simply install the package via package manager, or,
    install prerequisite packages and install GNS3 via pip. 
    Nothing else should be needed
    - In the install commands, you have to specify the version, for example, 
    apt install gns3-gui=2.2.39 or pip install gns3-gui==2.2.39

2. Make sure that the OpenVPN connection is established.

3. Run GNS3. In the setup wizard, 
  - choose "Run appliances on a remote server (advanced usage)" 
  - and click "Next >"

4. Set the following parameters:
  - Host: 172.16.253.1
  - Port: 3080 TCP
  - Authentication not used

5. Click "Next >"
6. Click "Finish"
```

**Wireshark:**

In case GNS3 did not install the protocol analyzer Wireshark, you can install it from here (Windows/Mac) or from your packet repository of choice (Linux).



### Basic commands and quick tips

```
(Cisco OS) The question mark ? is your best friend. 
Whenever you don't know what exactly you should input to a command, 
insert a question mark and you will receive hints.

(Cisco OS) Use the tabulator (tab) button to auto complete commands 
after typing a few letters.

(Linux and Cisco OS) You can also input commands with incomplete 
keywords and the system will accept them if they are unambiguous.

  - Example 1: ip address add 10.0.0.1 is the same as ip a a 10.0.0.1
  - Example 2: configure terminal is the same as conf t
```

