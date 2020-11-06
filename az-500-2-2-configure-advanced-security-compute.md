# 2.2. Configure advanced security for compute

## Configure endpoint protection

## Configure and monitor system updates for VMs

## Configure authentication for Azure Container Registry

## Configure security for different types of containers

## Implement vulnerability management

## Configure isolation for AKS

## Configure security for container registry

## Implement Azure Disk Encryption

Azure Disk Encryption (ADE) is a capability that helps you encrypt your Windows and Linux IaaS virtual machine disks. ADE leverages the industry standard BitLocker feature of Windows and the DM-Crypt feature of Linux to provide volume encryption for the OS and data disks. The solution is integrated with Azure Key Vault to help you control and manage the disk-encryption keys and secrets (and you can use managed identity for Azure services for accessing the key vault).

When you apply the Disk Encryption management solution, you can satisfy the following business needs:

* IaaS VMs are secured at rest by using industry-standard encryption technology to address organizational security and compliance requirements.
* IaaS VMs boot under customer-controlled keys and policies. You can audit their usage in your key vault.

In addition, if you use Azure Security Center, you're alerted if you have VMs that aren't encrypted. The alerts display as High Severity, and the recommendation is to encrypt these VMs.

Your organization can apply ADE to their virtual machines to be sure any data stored on VHDs is secured to their organizational and compliance requirements. Because boot disks are also encrypted, they can control and audit usage.

## Configure authentication and security for Azure App Service

## Configure SSL/TLS certs

## Configure authentication for Azure Kubernetes Service

## Configure automatic updates
