<p align="center">
<img src="https://user-images.githubusercontent.com/126641333/227748772-068be7e5-3251-4e69-a753-1b9492c04fa8.png"/>
</p>

<h1>Vulnerability Management Using Tenable Nessus </h1>
vulnerability scanning and vulnerability remediation. These are two of the main steps in the Vulnerability Management Lifecycle. We will be using Nessus Essentials to scan local VMs hosted on VMWare Workstation in order run credentialed scans to discover vulnerabilities, remediate some of the vulnerabilities, then perform a rescan to verify remediation. </br>


<h2>Prerequiste</h2>

- Install VMWare Player
- Downloading Windows 10 ISO
- Download and Install Nessus Essentials

<h2>Setup Virtual Machine</h2>
Use the ISO file you downloaded from Microsoft to create your VM. Set up the disc size, hardware and network adapater. You can set up with the following specification, Memory 4GB, Processors 4 and Network Adapter "Bridged" or "NAT" 

<img src="https://user-images.githubusercontent.com/126641333/227749224-7e31948c-331a-4d2f-862e-7681fe9b1b86.png"/>

<h2>Ensure Connectivity to the VM</h2>
We can obtain the the IP addresses of the host machine and VM by going searching for 'cmd' in the windowns search bar, then using the 'ipconfig' command to get the IPv4 amongst other information such as IPv6, default getaway, subnet mask etc. Then using the 'ping' command you can try to ping each machine to see if you get a reply back. 

<h2> Creating a new scan in Nessus</h2>
Once you login to Nessus, click on Create a New Scan, choose Basic scan. In the new window, under Settings, give the scan a name, this could be anyting you want to identify the scan with, description and under Target put the IP address of the VM, you should have the IP address from the previous step. 
<img src="https://user-images.githubusercontent.com/126641333/227749577-6e2e8a13-c499-4c78-bbef-5a0274db9d42.png"/>


<h2>Inspecting the first Scan (no Credentials)</h2>
After running the first scan, you will be able to see the results by clicking on the scan. You can navigate to the vulnerability tab to see what vulnerabilities Nessus was able to find. You can deep dive into each vunlnerability to find out more information. This section will be somewhat limited due to the scan being uncredentialed. 

<img src="https://user-images.githubusercontent.com/126641333/227749834-cbd30aa7-cb70-4455-9850-1116de4ac41b.png"/>

<img src="https://user-images.githubusercontent.com/126641333/227749844-19f2bdff-9735-4a5a-af29-a13324be1216.png"/>

<h2>Configuring VM for Credentialed Scan</h2>
The following is provided by Nessus. 
Go to your VM and do the following 
<ul>
  <li> Enable Remote Registry</li>
  <li> Enable Printer and File Sharing </li> 
  <li> Disable Firewall </li> 
  <li> Disable User Account Control </li>
</ul>
<img src="https://user-images.githubusercontent.com/126641333/227750028-ea86a7e6-5db2-4d06-9a60-d32e54a5d0c8.png"/>
<img src="https://user-images.githubusercontent.com/126641333/227750031-2af3f0e4-d607-4d39-a3cd-a585817175be.png"/>
<img src="https://user-images.githubusercontent.com/126641333/227750042-ace75c56-8bd2-47c6-9e52-0322f27cf1be.png"/>
<img src="https://user-images.githubusercontent.com/126641333/227750047-605b081d-d6e5-4bdc-9adb-3a475276af62.png"/>

