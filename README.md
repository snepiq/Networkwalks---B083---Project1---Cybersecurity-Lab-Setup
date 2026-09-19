Markdown
# 🔐 Cybersecurity Lab Environment Setup

### A hands-on cybersecurity lab environment built using VirtualBox/VMware, Kali Linux, to practice penetration testing, network monitoring, and security analysis practice.

![Skill](https://img.shields.io/badge/Skill-Cybersecurity-444444?style=flat&labelColor=a10000)
![Ver](https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0078d7?style=flat&labelColor=000000)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-v2026.2-e65c00?style=flat&logo=kalilinux&logoColor=white&labelColor=000000)
![Skill](https://img.shields.io/badge/Skill-Linux-444444?style=flat&labelColor=a10000)
![Penetration Testing](https://img.shields.io/badge/%EF%A3%BF-Penetration%20Testing-a10000?style=flat&logo=kalilinux&logoColor=white&labelColor=000000)
![GitHub](https://img.shields.io/badge/GitHub-Repository-444444?style=flat&logo=github&logoColor=white&labelColor=0078d7)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-Lab-444444?style=flat&logo=kalilinux&logoColor=white&labelColor=a10000)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-Reference-444444?style=flat&labelColor=a10000)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-Practice-e65c00?style=flat&logo=kalilinux&logoColor=white&labelColor=000000)
![Author](https://img.shields.io/badge/Ayorinde%20Michael%20-Author-a10000?style=flat) 



## 📋 Table of Contents
- Objective
- Lab Architecture 
- Hardware & Software Requirements -- hardware--software-requirements
- Lab Setup & Configurations](#-lab-setup--configurations
  - Step 1: Hypervisor Installation --- Step-1-hypervisor-installation
  - Step 2: Kali Linux VM Configuration --- Step-2-kali-linux-vm-configuration
  - Step 3: Target VM Setup Metasploitable / Windows -- Step-3-target-vm-setup-metasploitable--windows
- Verification & Testing
- Lessons Learned & Skills Demonstrated](#-lessons-learned--skills-demonstrated)



## 🎯 Objective
The primary goal of this lab is to create an isolated, secure environment to:


    *Practice penetration testing techniques and tools pre-installed on **Kali Linux**.
    
    *Understand network segmentation and virtual networking (Host-Only / NAT Networks).
    
    *Conduct vulnerability assessments against target virtual machines.
    

## 📐 Lab Architecture
         ├──► Hypervisor (VirtualBox / VMware Workstation)
                 │
                 ├──► NAT / Internal Network 
                 │         
                        ├──► [ Attacker ] Kali Linux 


🛠️ Hardware & Software Requirements
Hardware Specs:

    *Host OS: Windows 11 / macOS / Linux
    
    *CPU: Quad-Core Processor (Intel i5/i7 or AMD Ryzen equivalent)

    *RAM: 16 GB Recommended (Minimum 8 GB
    
    *Storage: 50 GB free SSD storage

Software Used:

    *VirtualBox v7.x / VMware Workstation Player
    
    *Kali Linux 2026.2 (64-bit ISO or Virtual Machine Image)


🚀 Lab Setup & Configurations
Step 1: Hypervisor Installation

    *Download and install Oracle VirtualBox (or VMware Workstation).
    
    *Configure a isolated virtual network (e.g., Host-Only Network or NAT Network) to prevent lab traffic from leaking to your local home             network.

Step 2: Kali Linux VM Configuration

    *Created a new VM with the following specifications;
    
    *RAM: 4096 MB
    
    *Processors: 2 Cores
    
    *Network Adapter: Set to Host-Only Adapter or NAT Network.
    
    *Booted up Kali Linux and ran basic update commands: Bash
    
    sudo apt update && sudo apt upgrade -y


Step 3: Target VM Setup

    *Imported the target machine image (e.g., Metasploitable 2).
    
    *Assigned the target VM to the same isolated network adapter as Kali Linux.
    
    *Verified local IP address allocation using ifconfig or ip a.

🔍 Verification & Testing

    *Network Connectivity Test: Ran a ping check from Kali Linux to ensure communication with the target machine without accessing the external       internet
    
    *Network Discovery: Scanned the local virtual network using nmap to discover active hosts and open ports

💡 Lessons Learned & Skills Demonstrated

    **Networking**: Understanding IP assignment, subnets, and host-only network isolation.
    
    **System Administration**: Allocating system resources (RAM, CPU, storage) across virtual environments.
    
    **Security Practices**: Ensuring vulnerable virtual machines remain strictly isolated from production networks.

    
