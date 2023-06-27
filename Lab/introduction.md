## COMM.NET Labs

This course page is bi-lingual. You can view the course in English by selecting any other display language than Finnish in Moodle.

Tämä kurssisivu on kaksikielinen. Sivu näkyy suomeksi jos Moodlessa on valittuna suomi näyttökielenä. Sivu näkyy englanniksi jos valittuna on mikä tahansa muu kieli.

Tälle sivulle on koottu yhteen ohjeita seuraavien kurssien laboratorioharjoitusten suorittamista varten:

> COMM.NET.200 Tietoverkkotekniikat I  
> COMM.NET.210 Tietoverkkojen laboratoriotyöt I  
> COMM.NET.400 Computer Networking II  
> COMM.NET.410 Networking Laboratory II  

Harjoitukset voi suorittaa omatoimisesti käyttäen OpenVPN-yhteyttä, verkkoprotokolla-analysaattori Wiresharkia ja tietoverkkosimulaattori GNS3:sta.

Jos et pysty asentamaan vaadittuja ohjelmistoja, voimme pyynnöstä tarjota etätyöpöytäyhteyden palvelimelle, johon ohjelmistot on asennettu.

Yhteystiedot: jani.urama@tuni.fi

Includes deletion of all projects! / Kaikki projektit poistetaan samalla!
If something doesn't work on the server, please send an e-mail / Jos jokin asia palvelimella ei toimi, lähetä sähköpostia, kiitos!


## Remote connection quick start guide

### OpenVPN:

1. Install an OpenVPN client: OpenVPN GUI (Windows) or OpenVPN Connect (macOS)

2. Establish the VPN connection using the following config file: GNS3.ovpn (Right-click link and Save link as, or copy and paste the contents to a text editor and save it as an .ovpn file)

3. (If you chose Save as) Check that the file was saved properly, and not as a web page.

4. If the connection works, you should be able to use a browser to connect to http://172.16.253.1:3080/  
- You could in theory do the exercise with the Web GUI, but it's not recommended nor officially supported.


### GNS3:

1. Install GNS3 version 2.2.39 (other versions do not work with our server). 
  
+ [GitHub links](https://github.com/GNS3/gns3-gui/releases/tag/v2.2.39) (Windows, Mac, source code)
  
+ Linux instructions  
    - IOU and Docker support are not needed.  
    - In short: either add the repo and simply install the package via package manager, or, install prerequisite packages and install GNS3 via pip  
        - Nothing else should be needed  
    - In the install commands, you have to specify the version, for example, apt install gns3-   gui=2.2.39 or pip install gns3-gui=2.2.39

2. Make sure that the OpenVPN connection is established.  
3. Run GNS3. In the setup wizard, choose "Run appliances on a remote server (advanced usage)" and click "Next >"  
4. Set the following parameters:  
>  Host: 172.16.253.1  
>  Port: 3080 TCP  
>  Authentication not used    
5. Click "Next >"  
6. Click "Finish"  


### Wireshark:

In case GNS3 did not install the protocol analyzer Wireshark, you can install it from here (Windows/Mac) or from your packet repository of choice (Linux).

[GNS3 Quick start guide](https://github.com/saugkim/2023summer_COM_NET_tuni/edit/main/Lab/gns3-quick-start.pdf)


## Basic commands and quick tips

(Cisco OS) The question mark ? is your best friend. Whenever you don't know what exactly you should input to a command, insert a question mark and you will receive hints.

(Cisco OS) Use the tabulator (tab) button to auto complete commands after typing a few letters.

(Linux and Cisco OS) You can also input commands with incomplete keywords and the system will accept them if they are unambiguous.  
 + Example 1: ip address add 10.0.0.1 is the same as ip a a 10.0.0.1  
 + Example 2: configure terminal is the same as conf t  

[Command reference sheet (Linux and Cisco OS)](https://github.com/saugkim/2023summer_COM_NET_tuni/edit/main/Lab/cmd-en.pdf)

