# Morning Post -- 2026-10-21

**Topic:** Cloud & DevOps Tips

---

Ever tried finding a single photo in a phone gallery with 50,000 unorganized pictures?
(with real examples you can use right now)

1. What is an Azure Resource Group
 ↳ What: A container that holds related resources for an Azure solution.
 ↳ Command/Tool: az group create
 Use Case: When your boss asks you to keep all project Alpha servers in one tidy bucket so you can delete them easily later.

2. Creating a Resource Group
 ↳ What: Making a brand new digital folder in your Azure subscription.
 ↳ Command/Tool: az group create --name myResourceGroup --location eastus
 Use Case: When you are starting a brand new pet project and need a clean slate.

3. Listing Existing Resource Groups
 ↳ What: Checking what folders you currently have in your cloud account.
 ↳ Command/Tool: az group list --output table
 Use Case: When you log in on Monday morning and forgot what weird resource names you created over the weekend.

4. Deleting a Resource Group
 ↳ What: Wiping out the folder and everything inside it with a single command.
 ↳ Command/Tool: az group delete --name myResourceGroup
 Use Case: When a testing sandbox is no longer needed and you want to stop paying for it.

5. Moving Resources Between Groups
 ↳ What: Dragging and dropping a server from one digital folder to another.
 ↳ Command/Tool: az resource move
 Use Case: When a database was accidentally created in the wrong project folder and needs to be shifted.

6. Locking a Resource Group
 ↳ What: Putting a literal padlock on the folder so nobody can accidentally delete it.
 ↳ Command/Tool: az lock create
 Use Case: When you finally finish setting up the production database and want to protect it from tired fingers at 3 AM.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always name your resource groups based on the project and environment, like 'rg-projectalpha-dev'.
 ↳ Avoid putting dev and production resources in the same resource group.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-21/morning/azure-resource-groups-organise-your-cloud-like-a-tidy-folder-cheatsheet.pdf

---

*PDF: [azure-resource-groups-organise-your-cloud-like-a-tidy-folder-cheatsheet.pdf](azure-resource-groups-organise-your-cloud-like-a-tidy-folder-cheatsheet.pdf)*
