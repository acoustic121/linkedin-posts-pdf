# Morning Post -- 2026-10-19

**Topic:** Cloud & DevOps Tips

---

Every cloud engineer touches these 6 Azure services on day one...
(with real examples you can use right now)

1. Resource Groups
 ↳ What: A digital folder that groups all related cloud assets for a single project.
 ↳ Command/Tool: az group create --name my-rg --location eastus
 Use Case: When your manager asks you to clean up a demo project, you delete one folder and everything vanishes safely.

2. Azure Virtual Machines
 ↳ What: A full computer running in Microsoft's datacenter that you control remotely.
 ↳ Command/Tool: az vm create --resource-group my-rg --name web-server --image Ubuntu2204 --generate-ssh-keys
 Use Case: When your team needs to host a legacy app that requires a custom background service.

3. Blob Storage
 ↳ What: An infinite online hard drive designed for unstructured files like images, logs, and backups.
 ↳ Command/Tool: az storage blob upload --account-name mystore --container-name assets --file ./logo.png --name logo.png
 Use Case: When your website users need a place to upload profile photos and resume PDFs.

4. Azure App Service
 ↳ What: A managed platform to deploy websites and APIs without touching virtual machines or OS updates.
 ↳ Command/Tool: az webapp up --resource-group my-rg --name my-cool-api --runtime "NODE:18LTS"
 Use Case: When you built a web application over the weekend and want it live with a public URL in 2 minutes.

5. Azure Virtual Network (VNet)
 ↳ What: An isolated private network that lets your cloud services talk to each other securely.
 ↳ Command/Tool: az network vnet create --resource-group my-rg --name main-vnet --subnet-name app-subnet
 Use Case: When your database should only talk to your internal API and never be visible to the open internet.

6. Azure Key Vault
 ↳ What: A tamper-proof digital safe for passwords, database strings, and API keys.
 ↳ Command/Tool: az keyvault secret set --vault-name team-vault --name db-password --value "supersecret123"
 Use Case: When you need to stop hardcoding database credentials directly into your GitHub repository.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always delete your test Resource Group after practicing so you never get a surprise bill.
 ↳ Don't expose database ports like 3306 or 5432 directly to the public internet; keep them inside a VNet.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-19/morning/microsoft-azure-101-core-services-every-cloud-beginner-needs-cheatsheet.pdf

---

*PDF: [microsoft-azure-101-core-services-every-cloud-beginner-needs-cheatsheet.pdf](microsoft-azure-101-core-services-every-cloud-beginner-needs-cheatsheet.pdf)*
