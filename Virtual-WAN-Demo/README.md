# Azure Virtual WAN Demo Environment

## :heavy_check_mark: Overview
This is a Terraform based demonstration of Azure Virtual WAN. The environment is designed to provide a simple foundation that you can add additional services (VPNs, ExpressRoute, Firewalls etc.) into, allowing the demonstration of concepts and technologies. 

## :question: What does this Lab deploy?

![Virtual WAN Demo Lab](https://raw.githubusercontent.com/jakewalsh90/Terraform-Azure/main/Virtual-WAN-Demo/images/Virtual-WAN-Demo-Lab.png?raw=true)

This lab deploys the following:
1. A Resource Group in two Azure Regions (based on variables)
2. A Virtual WAN in the Primary Region
3. A Virtual WAN Hub in two Azure Regions
4. A vNet in each Azure Region which is connected to the Virtual WAN Hub.
6. A Subnet and NSG in each of the above vNets.
7. A Subnet in each Region to be used for Azure Bastion.  
8. Azure Bastion in each Region to allow for access to the VMs for Testing. 
9. A Virtual Machine in each Azure Region (in the Regional vNets), to allow testing of Connectivity. 
10. A Custom Script Extension that runs on both VMs to add a few testing Apps (using Chocolatey) and allows ICMP through Windows Firewall for testing. 