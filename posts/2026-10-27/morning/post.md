# Morning Post -- 2026-10-27

**Topic:** Cloud & DevOps Tips

---

Every cloud engineer needs to manage user access in Azure Active Directory...
(with real examples you can use right now)

1. User Listing
 ↳ What: Azure AD is like a digital security guard controlling who gets into your cloud building.
 ↳ Command/Tool: az ad user list --output table
 Use Case: When your security manager asks for a quick list of all active users in the company.

2. Creating a New User
 ↳ What: Adding a brand-new digital identity to your Azure account for a new teammate.
 ↳ Command/Tool: az ad user create --display-name "John Doe" --user-principal-name "john@yourdomain.com" --password "TempPass123!"
 Use Case: When HR hires a new developer and you need to set up their account on day one.

3. Group Creation
 ↳ What: A digital folder that holds multiple users so you can manage permissions easily.
 ↳ Command/Tool: az ad group create --display-name "Developers" --mail-nickname "DevGroup"
 Use Case: When you need to give 10 new interns access to the exact same project folder.

4. Adding Users to Groups
 ↳ What: Putting a specific person inside a permission group.
 ↳ Command/Tool: az ad group member add --group "Developers" --member-id "<user-object-id>"
 Use Case: When a team member transfers to the engineering department.

5. Granting Role Permissions (RBAC)
 ↳ What: Giving someone specific permissions like reading or editing cloud resources.
 ↳ Command/Tool: az role assignment create --assignee "john@yourdomain.com" --role "Reader" --resource-group "AppRG"
 Use Case: When your manager asks you to let a junior dev view server logs without breaking production.

6. Creating Service Principals
 ↳ What: A safe non-human account used by applications and automated scripts to log in.
 ↳ Command/Tool: az ad sp create-for-rbac --name "MyAppScript" --role contributor
 Use Case: When your automated build script needs permission to deploy code at midnight.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always assign roles to groups instead of giving permissions to individual users.
 ↳ Never hardcode application secret keys inside your public GitHub repositories.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-27/morning/azure-active-directory-manage-users-access-in-the-cloud-cheatsheet.pdf

---

*PDF: [azure-active-directory-manage-users-access-in-the-cloud-cheatsheet.pdf](azure-active-directory-manage-users-access-in-the-cloud-cheatsheet.pdf)*
