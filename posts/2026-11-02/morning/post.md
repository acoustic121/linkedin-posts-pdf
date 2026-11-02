# Morning Post -- 2026-11-02

**Topic:** Cloud & DevOps Tips

---

Every DevOps engineer eventually inherits cloud resources created manually in the console...
(with real examples you can use right now)

1. Write the Skeleton Block
 ↳ What: Tell Terraform which resource type and local name you plan to import.
 ↳ Command/Tool: resource "aws_s3_bucket" "legacy_bucket" {}
 Use Case: When your manager asks you to manage an existing S3 bucket with Terraform.

2. The Classic CLI Import
 ↳ What: Connects an existing cloud resource ID directly to your state file.
 ↳ Command/Tool: terraform import aws_s3_bucket.legacy_bucket my-existing-bucket-name
 Use Case: When you need a quick command to link a single existing cloud resource.

3. The Modern Import Block
 ↳ What: Write your import intent directly in code so your whole team sees it in Git.
 ↳ Command/Tool: import { to = aws_s3_bucket.legacy_bucket id = "my-existing-bucket-name" }
 Use Case: When you want peer reviews on your infrastructure imports before applying.

4. Auto-Generate TF Code
 ↳ What: Asks Terraform to write the resource HCL configuration for you automatically.
 ↳ Command/Tool: terraform plan -generate-config-out=generated.tf
 Use Case: When you import a complex database and don't want to write 30 settings by hand.

5. Inspect Imported State
 ↳ What: View all actual cloud settings Terraform pulled into your state file.
 ↳ Command/Tool: terraform state show aws_s3_bucket.legacy_bucket
 Use Case: When you need to copy missing attributes into your permanent code file.

6. Verify Zero Changes
 ↳ What: Check if your local code matches your real cloud setup perfectly.
 ↳ Command/Tool: terraform plan
 Use Case: When you want to guarantee Terraform won't modify or delete your bucket on apply.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always back up your terraform.tfstate file before running manual CLI imports.
 ↳ Don't forget that classic import only updates state, it does not write code for you.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-02/morning/terraform-import-bring-existing-infrastructure-under-iac-control-cheatsheet.pdf

---

*PDF: [terraform-import-bring-existing-infrastructure-under-iac-control-cheatsheet.pdf](terraform-import-bring-existing-infrastructure-under-iac-control-cheatsheet.pdf)*
