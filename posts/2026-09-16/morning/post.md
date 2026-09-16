# Morning Post -- 2026-09-16

**Topic:** Cloud & DevOps Tips

---

Someone manually changed a server setting in the cloud console at 2 AM, and now your app is broken...
(with real examples you can use right now)

1. Catch Drift in CI/CD Pipelines
 ↳ What: Runs a check to see if cloud resources match your code and outputs a exit status code.
 ↳ Command/Tool: terraform plan -detailed-exitcode
 Use Case: Put this in your GitHub Actions workflow so builds fail automatically if someone manually altered production.

2. Sync State Without Changing Infrastructure
 ↳ What: Updates your state file with real-world cloud changes without modifying or destroying live resources.
 ↳ Command/Tool: terraform apply -refresh-only
 Use Case: When your team manually scaled up a database and you want your state file to safely match reality.

3. Inspect What Terraform Currently Remembers
 ↳ What: Displays the exact properties Terraform has stored in its state file for a single resource.
 ↳ Command/Tool: terraform state show aws_instance.web_server
 Use Case: When an app crashes at 3am and you need to quickly check the server's recorded IP address and settings.

4. Force Recreate a Drifted Resource
 ↳ What: Forces Terraform to destroy and recreate a single damaged resource on the next apply.
 ↳ Command/Tool: terraform apply -replace="aws_instance.web_server"
 Use Case: When someone messed up a server's manual config and you need a clean, fresh instance immediately.

5. Bring Manual Cloud Resources into Code
 ↳ What: Connects an existing cloud resource created in the web console to your Terraform configuration.
 ↳ Command/Tool: terraform import aws_s3_bucket.my_bucket my-app-data-bucket
 Use Case: When your boss asks you to start managing an old manually-created S3 bucket using Terraform.

6. Scan Entire Cloud Account for Hidden Changes
 ↳ What: An open-source tool that scans your actual cloud setup and reports untracked resources.
 ↳ Command/Tool: driftctl scan
 Use Case: When you want a full security audit to find resources created outside of your DevOps pipeline.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always run terraform plan before applying changes to catch accidental drift early.
 ↳ Avoid making manual changes in the cloud portal—always update your Terraform code first.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-16/morning/terraform-drift-detection-catch-changes-before-they-break-prod-cheatsheet.pdf

---

*PDF: [terraform-drift-detection-catch-changes-before-they-break-prod-cheatsheet.pdf](terraform-drift-detection-catch-changes-before-they-break-prod-cheatsheet.pdf)*
