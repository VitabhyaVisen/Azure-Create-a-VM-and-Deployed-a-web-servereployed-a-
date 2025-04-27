# Azure-Create-a-VM-and-Deployed-a-web-servereployed-a-
Project Overview
This project demonstrates how to create a Virtual Machine (VM) in Microsoft Azure and deploy a fully functional web server on it. It is a beginner-to-intermediate level cloud project designed to build foundational skills in Azure cloud management, networking, and web server configuration. By the end of this project, you will have a publicly accessible web server hosted on an Azure VM.

The project covers all essential steps, from setting up the Azure environment to configuring the web server and verifying its deployment through a browser.

Objectives
Create and configure a Virtual Machine on Microsoft Azure.

Connect to the VM securely using SSH (Linux) or RDP (Windows).

Install a web server (Apache/Nginx on Linux, IIS on Windows) on the VM.

Configure firewall settings to allow HTTP/HTTPS traffic.

Deploy a sample web page on the web server.

Access the web server through the VM's public IP address.

Technologies Used
Microsoft Azure Portal / Azure CLI

Ubuntu Server 20.04 LTS (or any other Linux distribution) (or Windows Server if preferred)

Apache2 (for Linux-based setup) / IIS (for Windows-based setup)

SSH (for Linux VM connection)

Remote Desktop Protocol (RDP) (for Windows VM connection)

Steps Performed
Azure Resource Group Setup

Created a new Resource Group to organize and manage Azure resources.

Virtual Machine Creation

Selected appropriate OS image (Ubuntu 20.04 LTS or Windows Server 2019).

Configured VM size (Standard B1s for testing purposes).

Created authentication credentials (SSH Key Pair for Linux or password for Windows).

Enabled Inbound Port Rules for SSH (port 22) and HTTP (port 80) during setup.

Connecting to the Virtual Machine

For Linux: Used SSH client (e.g., Terminal, PuTTY) to securely connect.

For Windows: Used Remote Desktop Connection (RDP).

Installing the Web Server

For Linux:

Updated the system packages using sudo apt update.

Installed Apache2 using sudo apt install apache2.

Verified Apache2 service was running.

For Windows:

Installed IIS Web Server using Server Manager.

Confirmed IIS was running through default welcome page.

Configuring the Firewall

Modified the Network Security Group (NSG) to ensure that ports 80 (HTTP) and optionally 443 (HTTPS) were open.

Ensured local firewalls within the VM allowed incoming HTTP traffic.

Deploying a Sample Web Page

Edited the default index.html file or uploaded a custom HTML page to /var/www/html/ (Linux) or C:\inetpub\wwwroot (Windows).

Testing the Deployment

Accessed the deployed website through a web browser using the public IP address of the VM.

Verified successful loading of the sample web page.

Outcome
✅ A fully functional web server was deployed on Azure.
✅ The web server was accessible publicly using the VM's public IP address.
✅ Learned practical skills in Azure VM creation, web server deployment, and cloud network configuration.

Future Enhancements
Automate VM creation and web server deployment using Azure ARM templates or Terraform.

Enable HTTPS using a free SSL certificate (e.g., Let's Encrypt for Linux servers).

Scale the application by creating multiple VMs behind an Azure Load Balancer.

Implement monitoring and alerting using Azure Monitor.
