# VNet-Blog

Blog about using declarative IaC to create virtual networks in Azure following network design patterns.

## Outline 

Goal is to deploy a Java app that references MySQL using Azure Virtual Networking.

1. Very brief introduction to Azure Virtual Networks (including Hub and Spoke deployment model). This blog assumes prior knowledge of networking

2. Explanation of the sample app & Azure deployment

    - [Airsonic Media Player](https://github.com/airsonic-advanced/airsonic-advanced)
    - Web Server runs Apache Tomcat on Ubuntu; MySQL database runs on Ubuntu
    - Architecture diagram

3. ARM template deployment