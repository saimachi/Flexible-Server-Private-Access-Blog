# Azure Virtual Networking for Lift-and-Shift Deployments

## Introduction to Azure Virtual Networks

Azure Virtual Networks allow Allow users to configure private connectivity to Azure resources or on-premises resources. The focus of our exploration today is to configure secure communication between a Java web application server and a MySQL database, hosted on Linux Virtual Machines. Even a relatively simple application scenario raises challenges that can be solved through Azure Virtual Networks and supporting security and management technologies:

- How can we ensure that the web application can access the MySQL database server, while preventing network access to the database server from other applications or the Internet?

- What happens if we decide to horizontally scale the web application?

- How can we access the Virtual Machines remotely for management through SSH?

As with other disciplines in application development, there are an established set of network architectures to facilitate cost savings, simplified management, and security for application lift-and-shift migrations. We will explore the *Hub and Spoke* pattern next.

## The Networking Architecture

- Uses ASGs and NSGs to control access. Not an implementation of hub and spoke. <https://docs.microsoft.com/en-us/azure/virtual-network/application-security-groups>
- Direct traffic from App Gateway (WAF) to Azure Firewall, which forwards packets to the application VM. Implements Azure Firewall in the hub VNet. <https://docs.microsoft.com/en-us/azure/architecture/example-scenario/gateway/application-gateway-before-azure-firewall>