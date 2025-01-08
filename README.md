# Active-Directory-Project

## Objective
The AD Project aimed to set up and configure an Active Directory (AD) environment while leveraging Splunk for telemetry and analysis. The goal was to simulate an attack using a brute force technique and analyze the attack data using Splunk, showcasing skills in AD setup, log management, and cybersecurity analysis.

### Skills Learned
<ul>
  <li>Gained proficiency in setting up and managing Active Directory services.</li>
  <li>Learned to configure static IPs, DNS servers, and network environments</li>
  <li>Used Splunk to collect and analyze telemetry data from multiple machines.</li>
  <li>Conducted brute force attack simulations and reviewed corresponding logs.</li>
  <li>Developed skills in virtual machine management and system configurations.</li>
</ul>

### Tools Used
<ul>
  <li>Splunk Enterprise: For data collection, telemetry, and log analysis.</li>
  <li>VirtualBox: Virtualization tool to set up project environments..</li>
  <li>Crowbar: Tool for brute force attack simulations.</li>
  <li>rockyou.txt: A password list for brute force attempts.</li>
  <li>Windows Server: Platform for setting up AD Domain Services.</li>
</ul>

## Steps
<b>Configure Splunk Server</b><br>
Disable DHCP and assign static IP settings based on the project diagram.
Set the DNS server to Google's DNS (8.8.8.8).
Install Splunk Enterprise and VirtualBox Guest Additions ISO on the server.

<b>Set Up Splunk Forwarder and Sysmon</b><br>
Install Splunk Forwarder and Sysmon on the target machine.
Configure Splunk to collect telemetry data from the server and target PC.

<b>Configure Windows Server</b><br>
Assign a static IP to the Windows Server.
Install Active Directory Domain Services.
Create a new forest to establish a new domain.

<b>Join the Target Machine to the Domain</b><br>
Connect the target machine to the newly created domain.
Create two user accounts (A and B) on the domain server.

<b>Simulate a Brute Force Attack</b><br>
Configure the attacker machine (Kali) with a static IP.
Use Crowbar with the "rockyou.txt" password file to perform a brute force attack on the target machine.
Enable Remote Desktop Protocol (RDP) on the target machine to facilitate the attack.

<b>Analyze Logs Using Splunk</b><br>
Access Splunk to review logs showing attack details.
Analyze event logs, including 20 login attempts, to identify the attacker’s name, IP address, and methods.
