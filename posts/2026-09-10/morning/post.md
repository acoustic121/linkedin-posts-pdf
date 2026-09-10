# Morning Post -- 2026-09-10

**Topic:** Cloud & DevOps Tips

---

Every junior engineer has panicked when their local terraform state file disappeared.
(with real examples you can use right now)

1. What is Terraform State
 ↳ What: A JSON file that remembers what cloud infrastructure you built.
 ↳ Command/Tool: terraform.tfstate
 Use Case: When your laptop crashes and you lose this file, Terraform forgets all your servers exist.

2. The Danger of Local Storage
 ↳ What: Keeping this file only on your personal computer.
 ↳ Command/Tool: pwd
 Use Case: When your teammate runs the same script and creates duplicate servers because their laptop doesn't know what you built.

3. Remote State Storage
 ↳ What: Saving your state file safely in the cloud where everyone can see it.
 ↳ Command/Tool: AWS S3 Bucket
 Use Case: When your boss asks you to let the team update the infrastructure safely together.

4. State Locking
 ↳ What: A traffic light system that stops two people from editing the cloud at the same exact time.
 ↳ Command/Tool: AWS DynamoDB
 Use Case: When you and a coworker click apply at 3 AM and accidentally break the production database.

5. Configuring Backend in Code
 ↳ What: Telling Terraform where to safely store your shared state file.
 ↳ Command/Tool: backend "s3" { }
 Use Case: When you want your project to automatically save state to the cloud on every run.

6. Migrating Existing State
 ↳ What: Safely moving your local state file up into the cloud storage.
 ↳ Command/Tool: terraform init
 Use Case: When you finally decide to stop risking local files and move everything to S3.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always set up remote state before writing your second resource.
 ↳ Never commit your local state file to GitHub.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-10/morning/terraform-remote-state-why-you-should-never-store-it-locally-cheatsheet.pdf

---

*PDF: [terraform-remote-state-why-you-should-never-store-it-locally-cheatsheet.pdf](terraform-remote-state-why-you-should-never-store-it-locally-cheatsheet.pdf)*
