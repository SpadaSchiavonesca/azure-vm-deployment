# Creating a Virtual Machine in Azure Portal

This guide provides step-by-step instructions on how to create a virtual machine (VM) in the Microsoft Azure Portal.  This process involves configuring the VM's settings, choosing an operating system, setting up networking, and deploying the VM.

**This guide follows the process outlined in this ScribeHow:** [Creating a Virtual Machine in Azure Portal](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw)

## Prerequisites

*   An active Azure subscription.  If you don't have one, you can create a free account: [https://azure.microsoft.com/en-us/free/](https://azure.microsoft.com/en-us/free/)

## Steps

1.  **Sign in to the Azure Portal:**
    *   Open your web browser and navigate to [https://portal.azure.com/](https://portal.azure.com/).
    *   Sign in with your Azure account credentials.
    *   [View Step 1 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=Open%20your-,web,-browser%20and)

2.  **Navigate to Virtual Machines:**
    *   In the Azure portal, search for "Virtual machines" in the search bar at the top.
    *   Select "Virtual machines" under the "Services" section.
     *   [View Step 2 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=search%20bar.-,Virtual%20machines,-Click%20to%20select)

3.  **Create a New Virtual Machine:**
    *   On the Virtual machines page, click "+ Create" and then select "Azure virtual machine".
    *   [View Step 3 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=machines%20page.-,Create,-%2B%20Create)

4.  **Configure Basic Settings (Basics Tab):**
    *   **Project Details:**
        *   Select your Azure subscription.
        *   Create a new resource group or select an existing one.  A resource group is a container that holds related resources for an Azure solution.  Give it a descriptive name (e.g., "MyVMResourceGroup").
    *   **Instance Details:**
        *   Enter a name for your virtual machine (e.g., "MyTestVM").
        *   Choose the Azure region where you want to deploy your VM.
        *   Select an availability option if needed (for high availability).  For a basic VM, you can often leave this as "No infrastructure redundancy required."
        *   Choose a "Security type", in most cases “Standard” should be chosen.
        *   Select an operating system image (e.g., "Ubuntu Server 20.04 LTS," "Windows Server 2019 Datacenter").
    *   **Administrator Account:**
        *   Choose an authentication type:
            *   **SSH public key (for Linux VMs):**  Recommended for security.  You'll need to provide an SSH public key.  You can generate an SSH key pair using tools like `ssh-keygen` on Linux/macOS or PuTTYgen on Windows.
            *   **Password (for Windows or Linux VMs):**  Choose a strong password.
        *   Enter a username for the administrator account.
        *   Provide either the SSH public key or the password, depending on your chosen authentication type.
    *   **Inbound Port Rules:**
        *   Configure inbound port rules to allow network traffic to your VM.
        *   For a web server, you'll typically need to allow:
            *   HTTP (port 80)
            *   HTTPS (port 443)
            *   SSH (port 22) - for remote access (especially important for Linux VMs).
        *  Select desired ports.
    *  [View Step 4 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=Create%20virtual%20machine-,Basics,-Project%20details)
5. **Configure Disks (Disks Tab):**
     * Choose OS disk type. For cost saving, Standard HDD is often sufficient for testing.
     * You can add additional data disks if needed, but for a basic setup, the default OS disk is usually enough.
    *   [View Step 5 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=the%20VM.-,Disks,-Click%20to%20select)
6.  **Configure Networking (Networking Tab):**
    *   **Virtual Network:**  Create a new virtual network or select an existing one. The virtual network provides a private network for your VM to communicate with other resources in Azure.
    *   **Subnet:**  Create a new subnet or select an existing one within your virtual network.
    *   **Public IP:**  Choose whether to assign a public IP address to your VM.  If you want to access your VM from the internet, you'll need a public IP.  You can create a new one or select an existing one.
    *   **NIC Network Security Group:** A network security group (NSG) acts as a firewall for your VM, controlling inbound and outbound traffic. You can create a new NSG or use a basic one.  Make sure the inbound port rules you configured in the "Basics" tab are also allowed by the NSG.
    *   [View Step 6 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=scroll%20down.-,Networking,-Click%20to%20select)

7.  **Configure Management (Management Tab):**
    *   Configure options such as monitoring, diagnostics, and auto-shutdown.  For a basic setup, you can often leave these at their default settings.
    *   [View Step 7 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=scroll%20down.-,Management,-Click%20to%20select)

8. **Configure Advanced settings (Advanced Tab):**
	* Configure options such as extensions, custom data, and user data, proximity placement groups, VM generations... For a basic setup, you can often leave these at their default settings.
    *   [View Step 8 in ScribeHow]( https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=scroll%20down.-,Advanced,-Click%20to%20select)
    

9.  **Configure Tags (Tags Tab):**
    *   (Optional) Add tags to organize your Azure resources. Tags are name-value pairs that enable you to categorize resources and view consolidated billing.
    *   [View Step 9 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=scroll%20down.-,Tags,-Click%20to%20select)

10. **Review and Create:**
    *   Review the configuration settings on the "Review + create" tab.  Ensure that all settings are correct.
    *   Click "Create" to deploy your virtual machine.  Azure will validate your settings, and if everything is valid, the deployment process will begin.
    *   [View Step 10 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=scroll%20down.-,Review%20%2B%20create,-Click%20to%20select)
11. **Download Private Key (if applicable):**
	* If you chose SSH public key authentication, you will be prompted to download the private key file (.pem).  Download this file and store it securely.  You'll need it to connect to your VM via SSH.
    *   [View Step 11 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=Create-,Download%20private%20key%20and%20create%20resource,-Click%20to%20select)

12. **Wait for Deployment:**
    *   The deployment process may take several minutes.  You can monitor the progress in the Azure portal.
     *   [View Step 12 in ScribeHow](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw#:~:text=Wait%20a%20bit,notifications%20bell.)

13. **Connect to Your VM:**
    *   Once the deployment is complete, navigate to the "Virtual machines" page and select your newly created VM.
    *   You'll see the VM's details, including its public IP address (if you assigned one) and its status.
    *   To connect:
        *   **SSH (Linux):** Use an SSH client (like PuTTY on Windows, or the `ssh` command on Linux/macOS) and the private key file you downloaded.  The command will be similar to:  `ssh -i your_private_key.pem username@your_vm_public_ip`
        *   **RDP (Windows):**  Use the Remote Desktop Connection application (mstsc.exe) on Windows. Enter the VM's public IP address and your administrator credentials.

## Next Steps

*   **Install a Web Server:** Once you've connected to your VM, you'll need to install a web server (e.g., Apache, Nginx, IIS) to host your website.  The specific steps will depend on your chosen operating system and web server.
* **Configure Firewall**: Ensure that firewall rules allow inbound traffic.
*	**Deploy Web Application**: move you application to VM and start a service.
*   **Configure DNS:**  If you want to use a custom domain name, you'll need to configure DNS records to point to your VM's public IP address.

This guide provides a basic overview of creating a VM in Azure. For more advanced configurations and features, refer to the official Azure documentation.
