# Creating a Virtual Machine in Azure Portal

This repository provides step-by-step guidance on how to create a virtual machine in Azure Portal, based on the [ScribeHow Guide](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw).

## Prerequisites
- An active [Microsoft Azure account](https://azure.microsoft.com/)
- Basic knowledge of cloud computing

## Steps to Create a Virtual Machine

### 1. Sign in to Azure Portal
1. Go to [Azure Portal](https://portal.azure.com/)
2. Log in with your Microsoft account credentials

### 2. Navigate to Virtual Machines
1. In the Azure Portal, search for **Virtual Machines** in the top search bar.
2. Click **Create** → **Azure virtual machine**.

### 3. Configure Basic Settings
1. **Subscription**: Choose your active subscription.
2. **Resource Group**: Select an existing resource group or create a new one.
3. **Virtual Machine Name**: Enter a unique name for the VM.
4. **Region**: Select the region closest to your users.
5. **Image**: Choose an OS (e.g., Windows Server, Ubuntu, etc.).
6. **Size**: Select a VM size based on your needs.

### 4. Configure Administrator Account
1. Choose **Authentication type** (Password or SSH key).
2. Provide an admin username and password (or SSH key for Linux VMs).

### 5. Configure Networking
1. In the **Networking** tab, select **Virtual Network** (create a new one if needed).
2. Choose **Subnet** and public IP settings as required.
3. Select security rules (allow inbound SSH/RDP if necessary).

### 6. Configure Additional Options (Optional)
1. **Management**: Enable monitoring and diagnostics as needed.
2. **Advanced**: Add scripts or custom extensions.
3. **Tags**: Assign metadata tags if required.

### 7. Review and Create
1. Click **Review + Create**.
2. Wait for validation and then click **Create** to deploy the VM.

### 8. Access the Virtual Machine
1. Navigate to **Virtual Machines** in Azure.
2. Click on the newly created VM.
3. Use **Connect** to access via RDP (Windows) or SSH (Linux).

## Additional Resources
- [Azure VM Documentation](https://docs.microsoft.com/en-us/azure/virtual-machines/)
- [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/)

---

This guide is synced with the [ScribeHow tutorial](https://scribehow.com/shared/Creating_a_Virtual_Machine_in_Azure_Portal__fYuQoaltQpCPlWh0tOfCaw).
