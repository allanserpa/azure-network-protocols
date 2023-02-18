<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DHCP Traffic 
- Observe DNS Traffic 
- Observe RDP Traffic

<h2>Actions and Observations</h2>

<p>
  <b>STEP 1A:</b> Use Remote Desktop to connect to your Windows 10 Virtual Machine
  <br>
  <b>STEP 1B:</b> Within your Windows 10 Virtual Machine, Install Wireshark
  <br>
  <b>STEP 1C:</b> Open Wireshark and filter for ICMP traffic only
  <br>
  <br>
  <img src="https://i.imgur.com/CS3uiRi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br>
  <b>STEP 1D:</b> Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM then observe ping requests and replies within     WireShark
  <br>
  <b>STEP 1E:</b> From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in       WireShark
  <br>
  <b>STEP 1F:</b> Initiate a perpetual/non-stop ping with the -t command from your Windows 10 VM to your Ubuntu VM 
  <br>
  <br>
  <img src="https://i.imgur.com/AQKRKok.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br>
  <b>STEP 1G:</b> Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic
  <br>
  <br>
  <img src="https://i.imgur.com/m2lVkVt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br>
  <b>STEP 1H:</b> Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity
  <br>
  <b>STEP 1I:</b> Re-enable ICMP traffic for the Network Security Group your Ubuntu VM is using
  <br>
  <br>
  <img src="https://i.imgur.com/QLmihDq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br>
  <b>STEP 1J:</b> Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity (should start working)
  <br>
  <b>STEP 1K:</b> Stop the ping activity (control c)

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
