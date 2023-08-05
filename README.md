<h1 align="center"><b><i>Cybersecurity Lab</i></b></h1>

In this project, I'll guide you through setting up your own virtual lab environment for cybersecurity practice, learning and practice various cybersecurity techniques. The goal of this cybersecurity lab is to provide you with hands-on experience in tackling real-world challenges. From penetration testing and vulnerability assessments to network security and malware analysis, having a lab is obviously essential. For this you need fundamentals knowledge on virtualization and VMs, because we will build a virtual lab using what we call Virtual Machines. Virtual machines allow you to experiment and explore various cybersecurity scenarios in a safe and isolated environment.

> "A Virtual Machine (VM) is a compute resource that uses software instead of a physical computer to run programs and deploy apps. One or more virtual “guest” machines run on a physical “host” machine.  Each virtual machine runs its own operating system and functions separately from the other VMs, even when they are all running on the same host. This means that, for example, a virtual MacOS virtual machine can run on a physical PC." VMware

</br>

## Introduction
Cybersecurity is a critical field in the digital age, and hands-on practice is essential to develop practical skills. A cybersecurity lab provides a controlled environment for learners to experiment with various tools and techniques without the risk of causing harm to real systems.

In this tutorial, you will learn how to set up a virtual lab using virtualization software like VMware or VirtualBox. The lab will consist of multiple virtual machines interconnected to simulate a network environment. We'll explore various cybersecurity exercises, including vulnerability scanning, penetration testing, and more.

**As said previously you first need to understand the purpose of virtualization, click on the image below !</br></br>**
[<img alt="VMs?" width="500px" src="https://techs.b-cdn.net/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2021/05/what-is-a-virtual-machine.jpg.webp"/>][VM?]</br>

## Prerequisites
Before you begin, ensure you have the following :

- **Hardware Requirements** : A computer with sufficient resources to run virtualization software and multiple VMs simultaneously. Recommended specifications include a multi-core processor, at least 8GB of RAM, and ample free disk space.
- **Virtualization Software** : Download and install a virtualization platform such as VMware Workstation, VMware Fusion (for macOS users), or VirtualBox (available on Windows, macOS, and Linux).
- **Internet Connectivity** : You'll need an active internet connection to download virtualization software and VM images.

## Setting up the Virtualization Software
This section will guide you through the installation and configuration process of the virtualization software, I would recommend VirtualBox to be honest, it can handle more integration tools than VMware and more hard disc formats. Follow the appropriate sub-section based on your operating system :

- ### Installing VMware Workstation (Windows)
  - Download : Visit the VMware website (https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html) and download VMware Workstation.
  - Installation : Double-click the downloaded installer and follow the on-screen instructions to install VMware Workstation.
  - License : After installation, you may need to enter a license key or use the trial version. (Commercial Usage)

- ### Installing VMware Fusion (macOS)
  - Download : Visit the VMware website (https://www.vmware.com/products/fusion/fusion-evaluation.html) and download VMware Fusion.
  - Installation : Double-click the downloaded DMG file and follow the on-screen instructions to install VMware Fusion.
  - License : After installation, you may need to enter a license key or use the trial version. (Commercial Usage)

- ### Installing VirtualBox (Windows, macOS, Linux)
  - Download : Visit the VirtualBox website (https://www.virtualbox.org/wiki/Downloads) and download the appropriate version for your operating system.
  - Installation : Double-click the downloaded installer and follow the on-screen instructions to install VirtualBox.
  - Once the virtualization software is installed, make sure to configure it to match your system's resources (e.g., RAM allocation, CPU cores).

## Downloading VM Images
To create a diverse cybersecurity lab environment, we'll use pre-configured VM images for different exercises. Here's how to download and import VM images:

- ### VM Image Sources
  - Kali Linux : (https://www.kali.org/get-kali/#kali-installer-images), if you are here today I assume you know what is Kali Linux !
  - VulnHub : VulnHub (https://www.vulnhub.com/) provides a vast collection of VMs with various vulnerabilities to practice penetration testing.
  - SANS SIFT Workstation : The SANS SIFT Workstation (https://www.sans.org/tools/sift-workstation/) is a popular digital forensics and incident response VM.
  - OWASP Broken Web Application Project VM : The OWASP BWAP VM (https://sourceforge.net/projects/owaspbwa/) is a collection of vulnerable web applications that is distributed on a Virtual Machine.

- ### Importing VMs
  - Download : Visit the respective website and download the VM image in the compatible format (e.g., OVA, VMDK).
  - Import VM : Open your virtualization software and go to the import option. Browse to the downloaded VM image and start the import process.
  - Ensure that the VMs are compatible with your virtualization software and meet the hardware requirements.
> To create a secure cybersecurity lab environment, it is essential to configure the virtual machines appropriately. When importing VM images, consider using either "Host-Only" or "NAT" networking modes to enhance security.

- ### Importance of "Host-Only" or "NAT" Networking

  - **Host-Only Networking** : In "Host-Only" mode, the virtual machine is isolated from the external network and can only communicate with the host machine and other VMs in the same host-only network. This isolation provides an extra layer of security, preventing VMs from directly accessing the internet or other networks.

  - **NAT (Network Address Translation) Networking** : NAT mode allows the VM to access the internet and external networks through the host machine's network connection. However, external networks cannot directly initiate connections to the VM. This setup acts as a firewall for the VM, adding another security boundary between the VM and potential external threats.

> By choosing "Host-Only" or "NAT" networking, you reduce the attack surface of your virtual machines, as they are shielded from direct exposure to the external network or the internet. This setup is particularly crucial when working with potentially vulnerable VM images or engaging in exercises involving penetration testing and exploitation.
> Always carefully consider the networking configuration based on the lab's objectives and exercise requirements. Avoid using "Bridged" networking mode, as it may expose VMs directly to the host network and the internet, increasing the risk of unintended consequences and potential security breaches.


</br>

**Here is a tutorial to install Kali Linux on VirtualBox, click on the image below !</br></br>**
[<img alt="Kali" width="500px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/Kali_2020.4.png/1200px-Kali_2020.4.png?20210203104823"/>][kali]</br>

## Test Your Lab !
I have Kali Linux and Metasploitable 3 in my lab.</br></br>
<img alt="KaliScreen" width="470px" src="https://github.com/IbrahimBenHariz/Cybersecurity-Lab/blob/main/Ressources/Kali%20VM.png"/>
<img alt="MetaScreen" width="500px" src="https://github.com/IbrahimBenHariz/Cybersecurity-Lab/blob/main/Ressources/Metasploitable%203.png"/>

Then let's run a simple nmap check !</br></br>

<img alt="KaliScreen" align="left" width="470px" src="https://github.com/IbrahimBenHariz/Cybersecurity-Lab/blob/main/Ressources/Kali%20VM%20NMAP.png"/>
<img alt="MetaScreen" width="500px" src="https://github.com/IbrahimBenHariz/Cybersecurity-Lab/blob/main/Ressources/Metasploitable%203%20IP.png"/> </br>

### There you go ! Don't hesitate to customize your lab, you can even add virtual routers, firewalls...
</br>

**Get Metasploitable 3 VM just here :** </br></br>
https://github.com/rapid7/metasploitable3/</br>
https://hackersploit.org/metasploitable3-installation-guide/


## Reach Out To Me <img alt="Contact Icon" width="40px" src="https://github.com/IbrahimBenHariz/IbrahimBenHariz/blob/main/PortfolioResources/ReachOutToMe.png"/>

[<img alt="LinkedIn" align="left" width="45px" src="https://github.com/IbrahimBenHariz/IbrahimBenHariz/blob/main/PortfolioResources/LinkedInIcon.svg"/>][linkedin]
[<img alt="Outlook" align="left" width="48px" src="https://github.com/IbrahimBenHariz/IbrahimBenHariz/blob/main/PortfolioResources/OutlookIcon.svg"/>][outlook]
[<img alt="Discord" align="left" width="47px" src="https://github.com/IbrahimBenHariz/IbrahimBenHariz/blob/main/PortfolioResources/DiscordIcon.svg"/>][discord]
[<img alt="Reddit" align="left" width="48px" src="https://github.com/IbrahimBenHariz/IbrahimBenHariz/blob/main/PortfolioResources/RedditIcon.png"/>][reddit]
[<img alt="Hack The Box" align="left" width="48px" src="https://github.com/IbrahimBenHariz/IbrahimBenHariz/blob/main/PortfolioResources/HackTheBoxIcon.svg"/>][hackthebox]
[<img alt="Try Hack Me" align="left" width="50px" src="https://github.com/IbrahimBenHariz/IbrahimBenHariz/blob/main/PortfolioResources/TryHackMeIcon.png"/>][tryhackme]
[<img alt="Credly" align="left" width="48px" src="https://github.com/IbrahimBenHariz/IbrahimBenHariz/blob/main/PortfolioResources/CredlyIcon.svg"/>][credly]

[kali]: https://www.youtube.com/watch?v=l0JgWilK6ok
[linkedin]: https://www.linkedin.com/in/ibrahim-benhariz
[outlook]: mailto:ibrahim.benhariz@outlook.com
[discord]: https://discord.com/users/1111590525066297464
[reddit]: https://www.reddit.com/user/IbrahimBenHariz
[hackthebox]: https://app.hackthebox.com/profile/1525863
[tryhackme]: https://tryhackme.com/p/IbrahimBenHariz
[credly]: https://www.credly.com/users/ibrahim-ben-hariz
[VM?]: https://techie-show.com/what-is-a-virtual-machine/
