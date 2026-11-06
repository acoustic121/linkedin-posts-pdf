# Morning Post -- 2026-11-06

**Topic:** Cloud & DevOps Tips

---

Every beginner struggles with local terraform.tfstate files until they try Terraform Cloud...
(with real examples you can use right now)

1. Remote State Storage
 ↳ What: Storing your infrastructure state file safely in the cloud instead of on your laptop.
 ↳ Command/Tool: terraform init
 Use Case: When your laptop crashes right before a release and your team needs the state file.

2. Terminal Authentication
 ↳ What: Connecting your local terminal securely to your free Terraform Cloud account.
 ↳ Command/Tool: terraform login
 Use Case: When you want to trigger cloud deployments directly from your favorite terminal.

3. Workspace Selection
 ↳ What: Separating your infrastructure environments like Dev and Prod inside the cloud.
 ↳ Command/Tool: terraform workspace select dev
 Use Case: When your lead asks you to test a firewall change in Dev without touching Production.

4. Remote Plan & Apply
 ↳ What: Executing plan and apply on HashiCorp servers instead of burning your laptop CPU.
 ↳ Command/Tool: terraform plan
 Use Case: When your weak laptop freezes up while building a massive cloud network.

5. Secret Management with Variable Sets
 ↳ What: Storing cloud API keys safely in Terraform Cloud so they never leak into Git.
 ↳ Command/Tool: TF_VAR_aws_secret_key
 Use Case: When your senior dev catches you almost uploading plain-text passwords to GitHub.

6. Automated Git CI/CD
 ↳ What: Triggering infrastructure builds automatically whenever code is pushed to your repository.
 ↳ Command/Tool: git push origin main
 Use Case: When you want your cloud setup to update instantly after your pull request gets approved.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with the free tier of Terraform Cloud—it takes less than 5 minutes to set up.
 ↳ Never commit your local terraform.tfstate or API keys to GitHub repositories.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-06/morning/terraform-cloud-free-remote-state-cicd-for-your-infra-cheatsheet.pdf

---

*PDF: [terraform-cloud-free-remote-state-cicd-for-your-infra-cheatsheet.pdf](terraform-cloud-free-remote-state-cicd-for-your-infra-cheatsheet.pdf)*
