    # Cybersecurity Lab Setup

Building an isolated virtual lab for penetration testing and ethical hacking practice

           



# Cybersecurity Home Lab Setup

A hands-on cybersecurity lab environment built using VirtualBox/VMware, Kali Linux, and targeted virtual machines to practice penetration testing, network monitoring, and security analysis.

---

## 📋 Table of Contents
- [Objective](#-objective)
- [Lab Topology & Architecture](#-lab-topology--architecture)
- [Hardware & Software Requirements](#-hardware--software-requirements)
- [Lab Setup & Configurations](#-lab-setup--configurations)
  - [Step 1: Hypervisor Installation](#step-1-hypervisor-installation)
  - [Step 2: Kali Linux VM Configuration](#step-2-kali-linux-vm-configuration)
  - [Step 3: Target VM Setup (Metasploitable / Windows)](#step-3-target-vm-setup-metasploitable--windows)
- [Verification & Testing](#-verification--testing)
- [Lessons Learned & Skills Demonstrated](#-lessons-learned--skills-demonstrated)
- [Disclaimer](#-disclaimer)

---

## 🎯 Objective
The primary goal of this lab is to create an isolated, secure environment to:
* Practice penetration testing techniques and tools pre-installed on **Kali Linux**.
* Understand network segmentation and virtual networking (Host-Only / NAT Networks).
* Conduct vulnerability assessments against target virtual machines.

---

## 📐 Lab Topology & Architecture

```text
[ Physical Host Machine ]


         │
         ├──► Hypervisor (VirtualBox / VMware Workstation)
                 │
                 ├──► NAT / Internal Network (192.168.56.0/24)
                 │         │
                 │         ├──► [ Attacker ] Kali Linux (IP: 192.168.56.10)
                 │         └──► [ Target ] Metasploitable2 / Windows VM (IP: 192.168.56.20)


🛠️ Hardware & Software Requirements
Hardware Specs:
Host OS: Windows 11 / macOS / Linux

CPU: Quad-Core Processor (Intel i5/i7 or AMD Ryzen equivalent)

RAM: 16 GB Recommended (Minimum 8 GB)

Storage: 50 GB free SSD storage

Software Used:
Hypervisor: VirtualBox v7.x / VMware Workstation Player

Attacker OS: Kali Linux 2024.x (64-bit ISO or Virtual Machine Image)

Target OS: Metasploitable 2 / Windows Server / DVWA

🚀 Lab Setup & Configurations
Step 1: Hypervisor Installation
Download and install Oracle VirtualBox (or VMware Workstation).

Configure a isolated virtual network (e.g., Host-Only Network or NAT Network) to prevent lab traffic from leaking to your local home network.

Step 2: Kali Linux VM Configuration
Created a new VM with the following specifications:

RAM: 4096 MB

Processors: 2 Cores

Network Adapter: Set to Host-Only Adapter or NAT Network.

Booted up Kali Linux and ran basic update commands:

Bash
sudo apt update && sudo apt upgrade -y
Step 3: Target VM Setup
Imported the target machine image (e.g., Metasploitable 2).

Assigned the target VM to the same isolated network adapter as Kali Linux.

Verified local IP address allocation using ifconfig or ip a.

🔍 Verification & Testing
Network Connectivity Test:
Ran a ping check from Kali Linux to ensure communication with the target machine without accessing the external internet:

Bash
ping -c 4 192.168.56.20
Network Discovery:
Scanned the local virtual network using nmap to discover active hosts and open ports:

Bash
nmap -sV 192.168.56.0/24
💡 Lessons Learned & Skills Demonstrated
Networking: Understanding IP assignment, subnets, and host-only network isolation.

System Administration: Allocating system resources (RAM, CPU, storage) across virtual environments.

Security Practices: Ensuring vulnerable virtual machines remain strictly isolated from production networks.

⚠️ Disclaimer
This lab project is created strictly for educational and self-learning purposes. All testing and activities were performed within an isolated, self-contained environment owned by the author. Unintended or unauthorized testing on external systems is illegal.
