# Accessing MySQL Flexible Server in a Virtual Network from On-Premises

## What will we build?

The ARM template provided with this post will provision Azure Database for MySQL Flexible Server in a virtual network; a VPN Gateway to connect to the virtual network from on-premises; and a Virtual Machine, which will function as a DNS forwarder.

### The Challenge

Azure Database for MySQL Flexible Server, one of Microsoft's PaaS MySQL offerings, supports a native virtual network deployment to avoid data exfiltration and meet industry compliance requirements. Moreover, Azure VPN Gateway Point-to-Site connections are popular to facilitate communication with resources located in an Azure virtual network from on-premises workstations. By default, MySQL Flexible Server is accessible from on-premises through its private IP address, but not its DNS name. This post demonstrates that a low-cost Windows Server 2019 VM can serve as a DNS forwarder for on-premises workstations accessing MySQL Flexible Server in a virtual network through its DNS name.  

#### How does Flexible Server Name Resolution Work?

TODO

### ARM Template

TODO

### Resources

This post assumes the following fundamental knowledge:

#### Networking

- [Overview of Azure Virtual Networking](https://docs.microsoft.com/azure/virtual-network/virtual-networks-overview)
- [Overview of Azure VPN Gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways)
- [Overview of Azure VPN Gateway Point-to-Site Connections](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about)

#### Azure Database for MySQL (Flexible Server)

- [Overview of Azure Database for MySQL - Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/overview)
- [Overview of Private Network Access for Azure Database for MySQL - Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-networking-vnet)
