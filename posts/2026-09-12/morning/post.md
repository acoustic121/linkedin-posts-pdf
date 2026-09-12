# Morning Post -- 2026-09-12

**Topic:** Cloud & DevOps Tips

---

Every Terraform beginner gets confused about what plan and apply actually do under the hood...
(with real examples you can use right now)

1. Terraform Init
 ↳ What: Downloads necessary cloud provider plugins and sets up your working directory.
 ↳ Command/Tool: terraform init
 Use Case: When you clone a new infrastructure project from GitHub and need to prepare your machine.

2. Terraform Refresh
 ↳ What: Queries your cloud provider to update your local state file with real-world changes.
 ↳ Command/Tool: terraform refresh
 Use Case: When a teammate manually edits an AWS server setting in the console and you need to detect it.

3. Terraform Plan
 ↳ What: Compares your code against the real world and shows changes without touching anything.
 ↳ Command/Tool: terraform plan
 Use Case: When your senior engineer asks to review your server updates before you actually build them.

4. Save Plan Output
 ↳ What: Saves the exact plan to a file so nobody can change settings in between.
 ↳ Command/Tool: terraform plan -out=tfplan
 Use Case: When you want to ensure the exact blueprint you reviewed is what gets built in production.

5. Terraform Apply
 ↳ What: Makes actual cloud API calls to build, update, or remove your cloud resources.
 ↳ Command/Tool: terraform apply
 Use Case: When your team gives the green light to deploy the new database for your app.

6. Targeted Apply
 ↳ What: Tells Terraform to update only one specific resource instead of your entire stack.
 ↳ Command/Tool: terraform apply -target=aws_instance.web_server
 Use Case: When your boss asks you to fix just the web server without touching the production database.

7. Terraform Destroy
 ↳ What: Deletes every single piece of cloud infrastructure tracked in your current project.
 ↳ Command/Tool: terraform destroy
 Use Case: When your temporary test environment is done and you want to avoid getting billed overnight.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always run terraform plan and read the (+/-) symbols carefully before applying.
 ↳ Never edit the terraform.tfstate file manually in a text editor.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-12/morning/terraform-plan-vs-apply-what-actually-happens-under-the-hood-cheatsheet.pdf

---

*PDF: [terraform-plan-vs-apply-what-actually-happens-under-the-hood-cheatsheet.pdf](terraform-plan-vs-apply-what-actually-happens-under-the-hood-cheatsheet.pdf)*
