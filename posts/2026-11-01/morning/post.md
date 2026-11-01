# Morning Post -- 2026-11-01

**Topic:** Cloud & DevOps Tips

---

Every developer using Terraform eventually breaks their local state file...
(with real examples you can use right now)

1. Create a Dedicated Azure Resource Group
 ↳ What: Sets up a clean folder in Azure to hold your backend resources.
 ↳ Command/Tool: az group create --name rg-tfstate --location eastus
 Use Case: When starting a new cloud project and needing an organized home for state.

2. Create a Secure Storage Account
 ↳ What: Provides encrypted, scalable cloud storage for your state files.
 ↳ Command/Tool: az storage account create --name tfstatestore123 --resource-group rg-tfstate --sku Standard_LRS
 Use Case: When your team needs secure, remote storage for cloud infrastructure.

3. Create the Blob Storage Container
 ↳ What: Acts like a safe folder inside your storage account for state files.
 ↳ Command/Tool: az storage container create --name tfstatecontainer --account-name tfstatestore123
 Use Case: When separating your state files for dev, staging, and prod environments.

4. Add the Azure Backend Block
 ↳ What: Tells Terraform to read and write state to Azure instead of your laptop.
 ↳ Command/Tool: backend "azurerm" { resource_group_name = "rg-tfstate" storage_account_name = "tfstatestore123" container_name = "tfstatecontainer" key = "prod.tfstate" }
 Use Case: When working on a shared codebase with multiple developers.

5. Migrate Local State to Azure
 ↳ What: Copies your existing local state file into Azure Blob Storage automatically.
 ↳ Command/Tool: terraform init
 Use Case: When moving a local prototype project into team production.

6. Verify Remote State Contents
 ↳ What: Displays all resources currently tracked inside your remote state file.
 ↳ Command/Tool: terraform state list
 Use Case: When your manager asks what infrastructure Terraform is managing right now.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Keep your backend storage account in a dedicated resource group separate from app resources.
 ↳ Never commit Azure storage access keys directly into your Git repository.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-01/morning/terraform-remote-state-in-azure-storage-step-by-step-guide-cheatsheet.pdf

---

*PDF: [terraform-remote-state-in-azure-storage-step-by-step-guide-cheatsheet.pdf](terraform-remote-state-in-azure-storage-step-by-step-guide-cheatsheet.pdf)*
