<p align="center">
<img src="https://i.imgur.com/QurLqjG.png" height="40%" width="60%"/>
</p>

<h1>Setting up ProtonVPN and Observing Its Effect on IP Address</h1>
In this project, I observed the impact of a virtual private network (VPN) on IP address, location, and web browsing. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
-	Remote Desktop
-	ProtonVPN (free version)


<h2>Operating System Used </h2>

- Windows 10 (21H2)

<h2>High-Level Steps</h2>

-	Create a Windows 10 virtual machine in Azure
-	Remote Desktop into the VM
-	Use whatismyipaddress.com to find the IP address and location for the VM
-	Download the free version of ProtonVPN (create an account if there is no pre-existing account)
-	In ProtonVPN, connect to a server in another country
-	Use whatismyipaddress.com to find the new IP address and location for the VM
-	Browse a webpage to see if there are any changes to the URL or language
-	Delete Resource Groups in Azure after completion


<h2>Synopsis</h2>

<p>
<img src="https://i.imgur.com/TzVwBK5.png" height="70%" width="70%"/>
</p>
<p>
I started out by creating a Windows 10 VM in Azure (under the “Essentials” section, notice that the location of the VM is East US). I copied and pasted the public IP address into Remote Desktop and connected to the VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/N08akoR.png" height="70%" width="70%"/>
</p>
<p>
Once I was in the VM, I opened up Microsoft Edge and searched “whatismyipaddress.com.” This website showed the IP address along with the IP location. Since the website was being used inside the VM, the IP address shown was the same as the one assigned by Microsoft Azure (in the top left corner). Also, the Region for the VM was set to East US (different region from where I was located), and the website showed that the IP location is Washington, Virginia.
</p>
<br />

<p>
<img src="https://i.imgur.com/933DqMe.png" height="70%" width="70%"/>
</p>
<p>
Now that we are aware of the IP address and location of the VM, let’s see how it changes when using a VPN! I had previously created a free ProtonVPN account for this lab, so I logged into my account and downloaded the ProtonVPN.
</p>
<br />

<p>
<img src="https://i.imgur.com/YcKiEZd.png" height="70%" width="70%"/>
</p>
<p>
I selected a server in Japan, and noticed the changes in ProtonVPN. One of the significant changes was that my IP address in the VPN turned out different from the VM’s IP address (compare the IP address in the top left corner of my screen to the IP address in the top left corner of the VPN).
</p>
<br />

<p>
<img src="https://i.imgur.com/k0d4oAM.png" height="70%" width="70%"/>
</p>
<p>
I still had whatismyipaddress.com open in the Edge browser, so I simply refreshed the page to view any changes. According to the website, my IP address was presently the one shown in the VPN, and my location was Tokyo, Japan! This is because my physical computer was connected to the VM, which was connected to a VPN server in Japan, making it look similar to the website like I was in Japan.
</p>
<br />

<p>
<img src="https://i.imgur.com/FPGISSi.png" height="70%" width="70%"/>
</p>
<p>
Evidently, when I searched the term “amazon” using Google, the search results were in Japanese. This further confirmed that the VPN worked. I cleaned up my lab upon conclusion.
</p>
<br />

<p>
✨ It was an interesting project and I had fun working on it.
</p>
<br />
