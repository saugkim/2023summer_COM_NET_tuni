instruction 

Remote connection quick start guide


**OpenVPN:**

Install an OpenVPN client: OpenVPN GUI (Windows) or OpenVPN Connect (macOS)

Establish the VPN connection using the following config file: GNS3.ovpn (Right-click link and Save link as, or copy and paste the contents to a text editor and save it as an .ovpn file)
(If you chose Save as) Check that the file was saved properly, and not as a web page.

If the connection works, you should be able to use a browser to connect to http://172.16.253.1:3080/

You could in theory do the exercise with the Web GUI, but it's not recommended nor officially supported.


**GNS3:**


Install GNS3 version 2.2.39 (other versions do not work with our server). 

GitHub links (Windows, Mac, source code)

Linux instructions

IOU and Docker support are not needed.

In short: either add the repo and simply install the package via package manager, or, install prerequisite packages and install GNS3 via pip
Nothing else should be needed

In the install commands, you have to specify the version, for example, apt install gns3-gui=2.2.39 or pip install gns3-gui==2.2.39

Make sure that the OpenVPN connection is established.

Run GNS3. In the setup wizard, choose "Run appliances on a remote server (advanced usage)" and click "Next >"
Set the following parameters:
```
Host: 172.16.253.1
Port: 3080 TCP
Authentication not used
Click "Next >"
Click "Finish"
```

**Wireshark:**

In case GNS3 did not install the protocol analyzer Wireshark, you can install it from here (Windows/Mac) or from your packet repository of choice (Linux).

GNS3 Quick start guideFile
