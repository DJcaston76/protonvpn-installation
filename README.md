<p align="center">
<img src="https://i.pcmag.com/imagery/reviews/066pfhdQmzHcmyEMaZtToWq-103.fit_scale.size_1028x578.v1691430001.png" alt="ProtonVPN logo"/>
</p>

<h1>ProtonVPN - Implementation and Installation</h1>
This tutorial outlines the installation and use of a vpn known as Proton VPN.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install Proton VPN](https://youtu.be/E7_CcrvsZ_A)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Proton VPN

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
  

<h2>Installation Steps</h2>

**Step 1: Create the VM within Microsoft Azure**
- Create a resource group called "vpn-practice_group"
- Create a VM called "vpn-pratice"
- Use Windows 10 Pro, version 22H2 and Standard_D4s_v3 - 2cpus, 16 GiB memory
- Make sure it auto populates to "vpn-practice_group" for its resource group before the "Review and Create" step
- Make sure to choose a region you don't live in
- Note the username and password you're creating for Windows 10

<br/>

<p>
<img width="812" alt="Screenshot 2023-09-21 174042" src="https://github.com/DJcaston76/protonvpn-installation/assets/145403292/0423ef29-2e5d-4431-b8ce-d0043b1bc352"></p>

**_These are the settings you can use to create your VM. Use a different region._**

</p>

<p>
<img width="691" alt="Screenshot 2023-09-21 174453" src="https://github.com/DJcaston76/protonvpn-installation/assets/145403292/a66996b7-4e78-4773-bdfb-0ebb88cd8de1"></p>

**_Make sure to checkmark the bottom part about licensing so you don't run into any issues._**

<br/>

**Step 2: Find current IP Address**
- Take not of the Public IPv4 Address from (WhatIsMyIPAddress.com)

<br/>

<p>
<img width="835" alt="Screenshot 2023-09-21 175422" src="https://github.com/DJcaston76/protonvpn-installation/assets/145403292/dddfee24-fac9-4122-8cb5-8304f2962a34">
</p>

**_This is one way to find your current IP Address._**

**Step 3: Log into the VM via RDP**
- Copy the Public IP Address from the VM (Virutal Machines > "vpn-pratice" > copy Public IP address)
- Log in, using your Windows 10 username and password

<br/>

<p>
<img width="835" alt="Screenshot 2023-09-21 180022" src="https://github.com/DJcaston76/protonvpn-installation/assets/145403292/46623bd7-a705-4bcf-8151-1817c4a1268d">
</p>

****

<p>
<img width="778" alt="Screenshot 2023-09-21 180601" src="https://github.com/DJcaston76/protonvpn-installation/assets/145403292/5caf5a59-75af-49f2-a558-24a70e7f4f2e">
</p>

**_This is what RDP looks like on Windows. You'll use the username and password you created when you set up Windows in the VM, here.._**



<br/>

**Step 4: Find IP Address of the Virtual Machine**
- Open a web broswer and search "WhatIsMyIPAddress.com"
- If done correctly you should be given a new IP Address inside of the virtual machine
<br/>

<p>
<img width="797" alt="Screenshot 2023-09-21 181005" src="https://github.com/DJcaston76/protonvpn-installation/assets/145403292/302718f5-3b91-44e6-9e1b-c74c239816a4">
</p>

****

<br/>

**Step 5: Install Proton VPN**
- Create a new account within Proton VPN
- Download and install Proton VPN for your apporiate OS

<br/>

<p>
<img width="935" alt="Screenshot 2023-09-21 181534" src="https://github.com/DJcaston76/protonvpn-installation/assets/145403292/5bc59eae-deca-47fc-a9e8-d31d058d6593">
</p>

**_When you're installing Proton VPN, you'll need to accept all of their terms._**

<br/>

**Step 6: Connect to Proton VPN**
- Once inside of Proton VPN make sure to click "Quick Connect"
- Take note of the VPN generated by the VPN
- After this guide you should end up with 3 totally different IP Addresses

<br/>

<p>
<img width="500" alt="Screenshot 2023-09-21 182419" src="https://github.com/DJcaston76/protonvpn-installation/assets/145403292/fff4b80f-8a12-442a-b918-9f857e2d2875">

**_Make sure you launch the Configuration Wizard after installing MySQL._**
</p>

<br/>

**Step 7: Make Changes in the IIS Admin Panel**
- Search for IIS > Right click it to run it as admin
- At the "vm-osticket" level, open the PHP Manager > Select a principal > browse to and open the "php.cgi" file
- At rhe "vm-osticket" level, restart the server from the right sidebar menu

<br/>

<p>
<img width="1039" alt="Screen Shot 2023-06-25 at 12 45 47 PM" src="https://github.com/yeahglo/osticket-prereqs/assets/91516100/01d2b90c-94cc-4d71-84fb-3925afb9ca70">
</p>

**_Click "Register new PHP version"._**

<br/>

**Step 8: Install osTicket Files and Set Up Installer**
- Download osTicket files
- Open a 2nd file explorer window, navigate to C: > inetpub > wwwroot
- Drag the "Upload" folder from the osTicket files to "wwwroot" to copy files over
- Rename the file, from "Upload" to "osTicket"
- At rhe "vm-osticket" level in the admin for IIS, restart the server from the right sidebar menu again
- Navigate to Sites > Default > osTicket
- From the right sidebar, click "Browse *:80"

<br/>

<img width="1230" alt="Screen Shot 2023-06-25 at 12 47 14 PM" src="https://github.com/yeahglo/osticket-prereqs/assets/91516100/1a13b8ef-070e-485d-aec7-277af282d283">

**_Drag the "Upload" folder over to "wwwroot" and rename it to "osTicket"._**

<img width="1036" alt="Screen Shot 2023-06-25 at 12 54 11 PM" src="https://github.com/yeahglo/osticket-prereqs/assets/91516100/8138f47e-57a8-4fd3-bc92-f5f140847e6c">

**_Click "Browse *:80" on the right sidebar so that it opens in the web browser._**

<br/>

**Step 9: Enabling PHP Extensions and Configuring File Permissions**
- Navigate back Sites > Default > osTicket in the admin IIS panel
- Open PHP Manager at this level and scroll down to click "Enable or disable an extension"
- Enable the following 3 extensions: php_imap.dll, php_intl.dll, and php.opcache.dll
- Refresh the osTicket Installer in your browser _(Note: you should see more checkmarks where it lists the extensions.)_
- Navigate to your C: Drive > inetpub > wwwroot > osTicket > Include > ost-sampleconfig.php
- Remove the "sample" part of the name, so that it reads "ost-config.php"
- Right click on the folder > Advanced > Disable Inheritance > Remove All
- Set New Permissions > Everyone (click "Check Names" to populate) > Check Full Control so that it applies all permissions

<br/>
