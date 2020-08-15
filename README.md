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
        - Create an NSG rule to block all outbound traffic from the back-end subnet to the Internet
        - Associated the back-end NSG to the back-end subnet
        - Created a public IP address for the webserver VM.
        - Created a NIC for the webserver VM.
        - Created a Web Server VM in the front-end subnet
        - Created a public IP address for the MySQL VM
        - Created a NIC for the MySQL VM
        - Created a MySQL VM in the back-end subnet
