# Azure-CLI -- 
✔The Repo consists of Azure CLI scripts for reference.
<br>
<br>
## Multi-Tier Architecture Implementation --
✨ A virtual network for multi-tier applications using an Azure CLI script.
<br>
<br>
This script sample creates a virtual network with front-end and back-end subnets. <br> Traffic to the front-end subnet is limited to HTTP and SSH, while traffic to the back-end subnet is limited to MySQL, port 3306.<br> After running the script, you have two virtual machines, one in each subnet, that you can deploy web server and MySQL software to.<br>
#### ✔Steps used --
        - Created a virtual network with front-end and back-end subnet
        - Created an NSG for backend subnet
        - Created an NSG rule to allow HTTP traffic in from the internet to the frontend subnet
        - Created an NSG rule to allow SSH traffic in from the internet to the frontend subnet
        - Associated the front-end NSG with frontend subnet
        - Created an NSG for backend subnet
        - Created an NSG rule to block all outbound traffic from the back-end subnet to the Internet
        - Associated the back-end NSG to the back-end subnet
        - Created a public IP address for the webserver VM.
        - Created a NIC for the webserver VM.
        - Created a Web Server VM in the front-end subnet
        - Created a public IP address for the MySQL VM
        - Created a NIC for the MySQL VM
        - Created a MySQL VM in the back-end subnet
## Virtual Network Peering --

<p>Virtual network peering enables you to seamlessly connect networks in Azure Virtual Network. The virtual networks appear as one for connectivity purposes. The traffic between virtual machines uses the Microsoft backbone infrastructure. Like traffic between virtual machines in the same network, traffic is routed through Microsoft's private network only.<br></p>

Azure supports the following types of peering:

        - Virtual network peering: Connect virtual networks within the same Azure region.
        - Global virtual network peering: Connecting virtual networks across Azure regions.
        
<br>The benefits of using virtual network peering, whether local or global, include:

- A low-latency, high-bandwidth connection between resources in different virtual networks.
- The ability for resources in one virtual network to communicate with resources in a different virtual network.
- The ability to transfer data between virtual networks across Azure subscriptions, Azure Active Directory tenants, deployment models, and Azure regions.
- The ability to peer virtual networks created through the Azure Resource Manager.
- The ability to peer a virtual network created through Resource Manager to one created through the classic deployment model. 

##### ✔Steps Used --
        - Created a resource group
        - Created virtual network 1
        - Created virtual network 2
        - Getting the id for VNet1
        - Getting the id for VNet2
        - Peering VNet1 to VNet2
        - Peering VNet2 to VNet1
## Cleaning up Deployment --

        - az group delete --name MyResourceGroup --yes
Deletes the created resources.
<br>
<br>
<br>
That's it!<br> 
This how Multi-Tier Architecture and Vnet Peering are being implemented in <a href = "https://azure.microsoft.com/en-in/features/azure-portal/" > Azure </a>
<br>For more reference can read and refer the following documentation ➡ <a href = "https://docs.microsoft.com/en-us/azure/virtual-network/" > Documentation </a>
<br>
<br>
Cheerio!! 🙋🏻‍♀️
