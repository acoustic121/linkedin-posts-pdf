# Morning Post -- 2026-11-03

**Topic:** Cloud & DevOps Tips

---

Every DevOps engineer faces a stuck server that just needs a fresh restart...
(with real examples you can use right now)

1. Find the Stuck Resource
 ↳ What: List all tracked resources to find the exact name of the broken server.
 ↳ Command/Tool: terraform state list
 Use Case: When your web server is acting weird and you need its exact Terraform address.

2. Preview a Resource Replacement
 ↳ What: See what Terraform will rebuild before actually deleting anything.
 ↳ Command/Tool: terraform plan -replace="aws_instance.web_server"
 Use Case: When your boss asks to confirm that only the broken web server will be rebuilt.

3. Force Recreate a Resource (Modern Way)
 ↳ What: Safely rebuild a specific broken resource in one simple step.
 ↳ Command/Tool: terraform apply -replace="aws_instance.web_server"
 Use Case: When the app crashes at 3am because a server corrupted its local files.

4. Mark a Resource as Broken (Legacy Way)
 ↳ What: Tag a resource so Terraform automatically rebuilds it during the next run.
 ↳ Command/Tool: terraform taint aws_instance.web_server
 Use Case: When you are maintaining older Terraform projects that still use legacy commands.

5. Unmark a Resource if You Change Your Mind
 ↳ What: Remove the broken tag so Terraform leaves the server alone.
 ↳ Command/Tool: terraform untaint aws_instance.web_server
 Use Case: When you accidentally marked the production server for deletion and need to stop it.

6. Zero-Downtime Server Replacement
 ↳ What: Tell Terraform to build the new server before deleting the old one.
 ↳ Command/Tool: lifecycle { create_before_destroy = true }
 Use Case: When replacing a live web server without taking down the website for users.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Use -replace instead of taint because it does not alter state permanently if you cancel.
 ↳ Always run terraform plan before apply so you do not accidentally delete the wrong server.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-03/morning/terraform-taint-replace-force-recreate-a-broken-resource-cheatsheet.pdf

---

*PDF: [terraform-taint-replace-force-recreate-a-broken-resource-cheatsheet.pdf](terraform-taint-replace-force-recreate-a-broken-resource-cheatsheet.pdf)*
