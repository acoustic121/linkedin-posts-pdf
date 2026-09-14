# Morning Post -- 2026-09-14

**Topic:** Cloud & DevOps Tips

---

Managing separate environments for Dev and Prod used to feel like juggling flaming swords.
(with real examples you can use right now)

1. List All Workspaces
 ↳ What: Shows all active environment state files available in your project folder.
 ↳ Command/Tool: terraform workspace list
 Use Case: When you open a project on Monday morning and forgot which environment you were working on.

2. Create a New Environment
 ↳ What: Creates a fresh, isolated state file for a new stage like dev or staging.
 ↳ Command/Tool: terraform workspace new dev
 Use Case: When your lead asks you to build a safe cloud playground without touching live servers.

3. Switch Between Environments
 ↳ What: Moves your terminal context safely to a different target environment.
 ↳ Command/Tool: terraform workspace select prod
 Use Case: When you finish testing in dev and need to deploy the exact code to production.

4. Confirm Active Workspace
 ↳ What: Displays the exact environment your next Terraform command will apply to.
 ↳ Command/Tool: terraform workspace show
 Use Case: When you are about to run a destroy command and need 100% certainty before clicking enter.

5. Dynamic Naming in Code
 ↳ What: Uses the active workspace name directly inside your resource configuration files.
 ↳ Command/Tool: name = "app-${terraform.workspace}"
 Use Case: When you want AWS buckets automatically tagged as app-dev or app-prod without repeating code.

6. Delete Old Workspaces
 ↳ What: Deletes an unused workspace state once its resources are destroyed.
 ↳ Command/Tool: terraform workspace delete feature-test
 Use Case: When you complete a quick client demo and want to clean up unused environment states.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always run 'terraform workspace show' right before 'terraform apply' to avoid expensive mistakes.
 ↳ Avoid using workspaces as your only security boundary for production—use separate cloud accounts too.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-14/morning/terraform-workspaces-manage-dev-staging-prod-easily-cheatsheet.pdf

---

*PDF: [terraform-workspaces-manage-dev-staging-prod-easily-cheatsheet.pdf](terraform-workspaces-manage-dev-staging-prod-easily-cheatsheet.pdf)*
