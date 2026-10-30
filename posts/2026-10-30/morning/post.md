# Morning Post -- 2026-10-30

**Topic:** Cloud & DevOps Tips

---

Every DevOps beginner starts by saving Terraform state on their laptop...
(with real examples you can use right now)

1. Local State (The Default)
 ↳ What: Storing your Terraform state file directly on your local computer.
 ↳ Command/Tool: terraform init
 Use Case: When you are testing code alone and don't care if state gets deleted.

2. Remote S3 Backend
 ↳ What: Storing state centrally in AWS S3 so your whole team shares one source of truth.
 ↳ Command/Tool: backend "s3" {}
 Use Case: When your teammate needs to make changes to cloud servers you created.

3. State Locking with DynamoDB
 ↳ What: Locking the state file so two people cannot run deployments simultaneously.
 ↳ Command/Tool: dynamodb_table = "terraform-locks"
 Use Case: When you and your coworker hit 'apply' at 3 PM at the exact same time.

4. Migrating Local to Remote
 ↳ What: Safely transferring your existing local state file into your remote cloud storage.
 ↳ Command/Tool: terraform init -migrate-state
 Use Case: When your solo project grows and you need to move it into team production.

5. Remote State Inspection
 ↳ What: Viewing all resources currently tracked inside your remote state without changing anything.
 ↳ Command/Tool: terraform state list
 Use Case: When your manager asks what exact cloud infrastructure exists in production right now.

6. State File Encryption
 ↳ What: Encrypting your remote state file in S3 so sensitive data stays safe at rest.
 ↳ Command/Tool: encrypt = true
 Use Case: When security auditing asks if database passwords in state are protected.

7. Native Backend Auth
 ↳ What: Authenticating to your backend automatically using environment credentials.
 ↳ Command/Tool: AWS_PROFILE=prod terraform init
 Use Case: When switching deployment context between your personal test account and company prod.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always enable DynamoDB state locking whenever you set up an S3 backend.
 ↳ Never manually edit your state file unless you absolutely know what you're doing.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-30/morning/terraform-backends-store-state-remotely-and-safely-cheatsheet.pdf

---

*PDF: [terraform-backends-store-state-remotely-and-safely-cheatsheet.pdf](terraform-backends-store-state-remotely-and-safely-cheatsheet.pdf)*
