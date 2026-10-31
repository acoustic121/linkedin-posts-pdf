# Morning Post -- 2026-10-31

**Topic:** Cloud & DevOps Tips

---

Every time you click around the Azure portal to build a server, imagine having to do it 50 more times tomorrow.
(with real examples you can use right now)

1. What is Terraform?
 ↳ What: A tool that lets you write code to build cloud resources instead of clicking buttons.
 ↳ Command/Tool: terraform version
 Use Case: When your team needs to create an identical testing environment in seconds without manual clicking.

2. The Azure Provider
 ↳ What: The translator that lets Terraform talk to Microsoft Azure to build your stuff.
 ↳ Command/Tool: provider "azurerm" { features {} }
 Use Case: When you need to tell Terraform which cloud account to build your virtual machines in.

3. Initializing the Workspace
 ↳ What: Downloading the specific plugin needed to talk to Azure.
 ↳ Command/Tool: terraform init
 Use Case: When you start a new project and need to download the Azure tools to your local machine.

4. Planning Your Changes
 ↳ What: A preview mode showing you what Terraform is going to build before it actually does it.
 ↳ Command/Tool: terraform plan
 Use Case: When your boss asks what changes you are about to make to the production environment.

5. Applying the Code
 ↳ What: The command that actually creates the resources in your Azure account.
 ↳ Command/Tool: terraform apply
 Use Case: When you are ready to deploy a new web server for a client demo.

6. Cleaning Up
 ↳ What: Deleting everything you created so you do not get charged money overnight.
 ↳ Command/Tool: terraform destroy
 Use Case: When your testing session is over and you want to wipe clean your cloud bill.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with a tiny resource like a Resource Group before building complex virtual machines.
 ↳ Never commit your Azure passwords or access keys directly into public GitHub repositories.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-31/morning/azure-provider-in-terraform-deploy-resources-to-azure-in-minutes-cheatsheet.pdf

---

*PDF: [azure-provider-in-terraform-deploy-resources-to-azure-in-minutes-cheatsheet.pdf](azure-provider-in-terraform-deploy-resources-to-azure-in-minutes-cheatsheet.pdf)*
