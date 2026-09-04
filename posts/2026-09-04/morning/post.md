# Morning Post -- 2026-09-04

**Topic:** Cloud & DevOps Tips

---

Every cloud engineer runs these core Terraform commands almost every single day.
(with real examples you can use right now)

1. Initialize Your Working Directory
 ↳ What: Downloads cloud provider plugins and sets up your project backend.
 ↳ Command/Tool: terraform init
 Use Case: Run this the very first time you clone an infrastructure repo from GitHub.

2. Clean Up Code Formatting
 ↳ What: Automatically aligns spacing and indentation across all configuration files.
 ↳ Command/Tool: terraform fmt
 Use Case: Run this before opening a pull request so your code looks clean to your team.

3. Check for Syntax Errors
 ↳ What: Checks your configuration files for syntax mistakes without contacting the cloud.
 ↳ Command/Tool: terraform validate
 Use Case: Catch typos in your resource blocks before waiting for cloud credentials to load.

4. Preview Cloud Changes
 ↳ What: Creates an execution plan showing exactly what will be added, changed, or deleted.
 ↳ Command/Tool: terraform plan
 Use Case: Use this when your lead asks what impact your new server changes will have.

5. Deploy Your Infrastructure
 ↳ What: Provisions and configures real cloud resources defined in your files.
 ↳ Command/Tool: terraform apply
 Use Case: Spin up your complete test environment in AWS or Azure with one confirmation.

6. Inspect Real-World State
 ↳ What: Displays a human-readable view of everything Terraform is currently managing.
 ↳ Command/Tool: terraform show
 Use Case: Quickly look up an assigned public IP address or ARN without opening the cloud console.

7. Clean Up and Delete Everything
 ↳ What: Destroys all remote objects managed by your configuration files safely.
 ↳ Command/Tool: terraform destroy
 Use Case: Shut down your sandbox lab on Friday evening so you don't get billed over the weekend.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always read the output of terraform plan carefully before typing 'yes'.
 ↳ Never manually edit or delete the terraform.tfstate file by hand.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-04/morning/automate-cloud-infrastructure-with-10-terraform-commands-cheatsheet.pdf

---

*PDF: [automate-cloud-infrastructure-with-10-terraform-commands-cheatsheet.pdf](automate-cloud-infrastructure-with-10-terraform-commands-cheatsheet.pdf)*
