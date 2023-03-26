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

