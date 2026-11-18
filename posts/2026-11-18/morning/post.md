# Morning Post -- 2026-11-18

**Topic:** Cloud & DevOps Tips

---

Every cloud beginner accidentally gives full admin rights to everyone...
(with real examples you can use right now)

1. Check Your Own Permissions
 ↳ What: See all roles and permissions currently assigned to your Azure account.
 ↳ Command/Tool: az role assignment list --assignee me --output table
 Use Case: When you get an annoying 'Access Denied' error while deploying resources.

2. Grant View-Only Access
 ↳ What: Give someone access to look at resources without letting them change anything.
 ↳ Command/Tool: az role assignment create --assignee intern@company.com --role "Reader" --resource-group "demo-rg"
 Use Case: When an auditor or intern needs to inspect settings without breaking production.

3. Allow Resource Management
 ↳ What: Give full access to manage resources, but block access control management.
 ↳ Command/Tool: az role assignment create --assignee dev@company.com --role "Contributor" --resource-group "dev-rg"
 Use Case: When your developer needs to create VMs and databases in their dev workspace.

4. Search Built-in Roles
 ↳ What: Discover pre-made Azure roles tailored for specific services.
 ↳ Command/Tool: az role definition list --query "[?contains(roleName, 'Storage')].roleName" --output table
 Use Case: When you want to find the exact role for a storage admin without guessing.

5. Revoke Access Immediately
 ↳ What: Remove a user's permissions safely when they no longer need them.
 ↳ Command/Tool: az role assignment delete --assignee user@company.com --role "Reader" --resource-group "demo-rg"
 Use Case: When a contractor finishes their project and offboards from your team.

6. Secure App-to-App Access
 ↳ What: Grant permissions directly to an application instead of using hardcoded secrets.
 ↳ Command/Tool: az role assignment create --assignee <app-id> --role "Storage Blob Data Reader" --scope <storage-id>
 Use Case: When your app crashes at 3am because it can't read files securely.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always follow the Principle of Least Privilege: start with Reader and add access only when required.
 ↳ Never grant the Owner role to fix a quick permission error during testing.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-18/morning/azure-rbac-control-who-can-touch-your-cloud-resources-cheatsheet.pdf

---

*PDF: [azure-rbac-control-who-can-touch-your-cloud-resources-cheatsheet.pdf](azure-rbac-control-who-can-touch-your-cloud-resources-cheatsheet.pdf)*
