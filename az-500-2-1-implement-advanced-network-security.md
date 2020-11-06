# 2.1. Implement advanced network security

## Secure the connectivity of virtual networks (VPN authentication, Express Route encryption)

Virtual private network (VPN) connections are a common way of establishing secure communication channels between networks, and this is no different when working with virtual networking on Azure. Connection between Azure virtual networks and an on-premises VPN device is a great way to provide secure communication between your network and your virtual machines on Azure.

To provide a dedicated, private connection between your network and Azure, you can use ExpressRoute. ExpressRoute lets you extend your on-premises networks into the Microsoft cloud over a private connection facilitated by a connectivity provider. With ExpressRoute, you can establish connections to Microsoft cloud services, such as Microsoft Azure, Microsoft 365, and Dynamics 365. This improves the security of your on-premises communication by sending this traffic over the private circuit instead of over the internet. You don't need to allow access to these services for your end users over the internet, and you can send this traffic through appliances for further traffic inspection.

An architectural diagram showing an ExpressRoute Circuit connecting the customer network with Azure resources.

To easily integrate multiple virtual networks in Azure, virtual network peering establishes a direct connection between designated virtual networks. Once established, you can use network security groups to provide isolation between resources in the same way you secure resources within a virtual network. This integration gives you the ability to provide the same fundamental layer of security across any peered virtual networks. Communication is only allowed between directly connected virtual networks.

## Configure Network Security Groups (NSGs) and Application Security Groups (ASGs)

For communication between virtual machines, network security groups are a critical piece to restrict unnecessary communication. Network security groups operate at layers 3 & 4, and provide a list of allowed and denied communication to and from network interfaces and subnets. Network security groups are fully customizable, and give you the ability to fully lock down network communication to and from your virtual machines. By using network security groups, you can isolate applications between environments, tiers, and services.

## Create and configure Azure Firewall

* [Azure Firewall documentation](https://docs.microsoft.com/en-us/azure/firewall/)
* [Tutorial: Deploy and configure Azure Firewall using the Azure portal](https://docs.microsoft.com/en-us/azure/firewall/tutorial-firewall-deploy-portal)

## Configure Azure Front Door service as an Application Gateway

## Configure a Web Application Firewall (WAF) on Azure Application Gateway

Application Gateway is a Layer 7 load balancer that also includes a web application firewall (WAF) to provide advanced security for your HTTP-based services. The WAF is based on rules from the OWASP 3.0 or 2.2.9 core rule sets, and provides protection from commonly known vulnerabilities such as cross-site scripting and SQL injection.

## Configure Azure Bastion

* [Azure Bastion documentation](https://docs.microsoft.com/en-us/azure/bastion/)

## Configure a firewall on a storage account, Azure SQL, KeyVault, or App Service

## Implement Service Endpoints

To isolate Azure services to only allow communication from virtual networks, use virtual network service endpoints. With service endpoints, Azure service resources can be secured to your virtual network. Securing service resources to a virtual network provides improved security by fully removing public internet access to resources, and allowing traffic only from your virtual network. This reduces the attack surface for your environment, reduces the administration required to limit communication between your virtual network and Azure services, and provides optimal routing for this communication.

## Implement DDoS protection

Any resource exposed to the internet is at risk of being attacked by a denial-of-service attack. These types of attacks attempt to overwhelm a network resource by sending so many requests that the resource becomes slow or unresponsive. To mitigate these attacks, Azure DDoS provides basic protection across all Azure services and enhanced protection for further customization for your resources. DDoS protection blocks attack traffic and forwards the remaining traffic to its intended destination. Within a few minutes of attack detection, you are notified using Azure Monitor metrics.
