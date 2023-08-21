<h1>Cybersecurity Home Lab</h1>

This project is based on CyberKraft's tutorial : https://www.youtube.com/playlist?list=PLUkY1OVVHzVktZOecfiDxdIodK4l5KkwY


<h1>Environment Setup</h1>

For this project, I am using Ubuntu 22.04 LTS as the main host.

- Virtualbox: ```sudo apt install virtualbox```
- Kali: https://www.kali.org/get-kali/#kali-virtual-machines
- Metasploitable2: https://sourceforge.net/projects/metasploitable/files/Metasploitable2/metasploitable-linux-2.0.0.zip/download 
- Windows 10 entreprise: https://info.microsoft.com/ww-landing-windows-10-enterprise.html
- Windows Server 2019: https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019 


<h1>Importing or Creating VM in Virtualbox</h1>

- <b>Kali Linux</b>: Click on "Add" button and locate the .vbox downloaded
- <b>Metasploitable 2</b>: 
    - Click on "New" 
    - Type and version: Linux, Ubuntu 64-bit
    - Hard Disk: Use an existing virtual hard disk file and locate the .vdi downloaded
- <b>Windows 10 Entreprise</b>:
    - Click on "New"
    - Type and Version : Microsoft Windows, Windows 10 64-bit
    - Hard Disk: Create a virtual hard disk file for now
- <b>Windows Server 2019</b>:
    - Click on "New"
    - Type and Version : Microsoft Windows, Windows 2019
    - Hard Disk: Create a virtual hard disk file for now
    
<p>Feel free to rename the VM's name and to choose the snapshot location.</p>

<h1>Verifying Network Configuration</h1>

For each virtual machine change the network adapter to "Bridged Adapter":

![](/img/Verify-Network/1.png)

<p>Once each network adapter has been changed. Turn them on one by one and write down their ip address and gateway. Eventually from Windows machines try to ping Linux machines. Note that Linux machines cannot ping Windows machine due to Windows defender or firewal. This will be dealt with later on.</p>

<p><b>Verify ip address with linux machines</b></p>

```
ip a

ifconfig 	# alternatively
```

<p><b>Verify gateway with linux machines</b></p>

```
ip r
```

