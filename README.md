<p align="center">
<img src="https://i.imgur.com/H2XSqm3.png" height="60%" width="60%" alt="Microsoft Remote Desktop"/>
</p>

<h1>Remote Desktop Setup in Azure</h1>
For my final project, I will show how to setup and connect to a remote machine using Remote Desktop by Microsoft. This will be done through Microsoft Azure utilizing two VMs. I will also be using Remote Desktop on my home device to remote into the VMs. To further demonstrate my knowledge, I will use Wireshark to observe different types of network traffic such as ICMP, SSH, and DHCP, DNS, and RDP traffic. At the end, I will demonstrate how to clean up Azure to save resources.

<h2>Video Demonstration</h2>

#Link goes here

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Wireshark
- Powershell

<h2>Operating Systems Used</h2>

- Windows 10 Pro (22H2)
- Ubuntu Server 20.04 LTS

<h2>Deployment Steps</h2>

- Login to portal.azure.com
<p>
<img src="https://i.imgur.com/dLfNB7m.png" height="80%" width="80%" alt="Login to the Azure Portal." />
</p>

- Create Resource Group (Final-Project)
<p>
<img src="https://i.imgur.com/Pq4SZeU.png" height="80%" width="80%" alt="Create the Resource Group." />
</p>

- Create Virtual Machines (VM1 and VM2)
<p>
<img src="https://i.imgur.com/fLzOYTO.png" height="80%" width="80%" alt="Create the Virtual Machines." />
</p>

- Remote into VM1 running Windows 10
<p>
<img src="https://i.imgur.com/789B3fL.png" height="80%" width="80%" alt="Remote into the Virtual Machine running Windows 10." />
</p>

- Install Wireshark and filter for IMCP traffic only
- Get the IP for the Ubuntu VM and ping it from the Windows 10 VM
- Observe ping requests and replies in Wireshark
<p>
<img src="https://i.imgur.com/zjAio23.png" height="80%" width="80%" alt="Run Wireshark and observe pings between VM's." />
</p>

- Ping a public website (CourseCareers.com) from Powershell and observe the traffic in Wireshark
<p>
<img src="https://i.imgur.com/wxHThBH.png" height="80%" width="80%" alt="Ping a public website and observe traffic." />
</p>

- Disable ICMP traffic in the Network Security Group for the Ubuntu VM
- Re-enable ICMP Traffic in the NSG for Ubuntu VM
<p>
<img src="https://i.imgur.com/p21kpBO.png" height="80%" width="80%" alt="Re-enable ICMP traffic in the Network Security Group." />
</p>

- Stop the perpetual ping
<p>
<img src="https://i.imgur.com/1jXVySi.png" height="80%" width="80%" alt="Stop the perpetual ping." />
</p>

- Filter for SSH traffic in Wireshark
- SSH into Ubuntu VM from the Windows 10 VM via the Ubuntu private IP Address
<p>
<img src="https://i.imgur.com/QA0O3L5.png" height="80%" width="80%" alt="SSH into Ubuntu VM from Windows 10 VM." />
</p>

- Type commands into the Linux SSH connection
- Observe traffic in Wireshark
<p>
<img src="https://i.imgur.com/BA2jNO7.png" height="80%" width="80%" alt="Observe traffic in Wireshark from Linux commands." />
</p>

- Filter for DHCP traffic in Wireshark
- From Windows 10 VM, issue a new IP in command line using ipconfig/renew
- Observe the DHCP traffic
<p>
<img src="https://i.imgur.com/u1DPCGc.png" height="80%" width="80%" alt="Issue a new IP and observe DHCP traffic from Windows 10 VM." />
</p>

- Filter to DNS traffic
- From Windows 10 VM, use nslookup to find google.com’s IP Address
- Observe the DNS traffic
<p>
<img src="https://i.imgur.com/IA7fefK.png" height="80%" width="80%" alt="Filter to DNS traffic and use nslookup to find google.com’s IP Address. Observe the network traffic." />
</p>

- Filter to RDP traffic (tcp.port == 3389)
- Observe the nonstop traffic
<p>
<img src="https://i.imgur.com/Qdm2HtR.png" height="80%" width="80%" alt="Filter to RDP and observe the nonstop traffic." />
</p>

- End Remote Desktop Connection
- Delete the Resource Group (Final-Project)
<p>
<img src="https://i.imgur.com/7OBvYM4.png" height="80%" width="80%" alt="Delete the resource group." />
</p>
