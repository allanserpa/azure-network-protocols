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
  <b>STEP 2A:</b> Back in Wireshark, filter for SSH traffic only
  <br>
  <br>
  <img src="https://i.imgur.com/98yvcaq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br>
  <b>STEP 2B:</b> From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address) and type commands (username, pwd, etc) into the linux     SSH connection and observe SSH traffic spam in WireShark
  <br>
  <b>STEP 2C:</b> Exit the SSH connection by typing ‘exit’ and pressing [Enter]
</p>
<br />

<p>
  <b>STEP 3A:</b> Back in Wireshark, filter for DHCP traffic only
  <br>
  <br>
  <img src="https://i.imgur.com/SlBlyVd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br>
  <b>STEP 3B:</b> From your Windows 10 VM, attempt to issue your VM a new IP address from the command line (ipconfig /renew) and observe the DHCP traffic appearing in   WireShark
</p>
<br />
