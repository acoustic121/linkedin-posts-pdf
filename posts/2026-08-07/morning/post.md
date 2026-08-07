# Morning Post -- 2026-08-07

**Topic:** Cloud & DevOps Tips

---

Every junior engineer has manually clicked through the AWS console to build a server...
(with real examples you can use right now)

1. Infrastructure as Code
 ↳ What: Writing human-readable configuration files to create and manage cloud servers automatically.
 ↳ Command/Tool: terraform --version
 Use Case: When your manager asks you to spin up three identical test servers in under two minutes.

2. The Blueprint
 ↳ What: A text file that describes what cloud resources you want to build.
 ↳ Command/Tool: main.tf
 Use Case: When you want to define a simple virtual machine in code instead of using a web browser.

3. Initialization
 ↳ What: Downloading the necessary provider plugins so Terraform can talk to your cloud provider.
 ↳ Command/Tool: terraform init
 Use Case: When you start a new project and need to download the AWS helper tools.

4. The Preview
 ↳ What: A dry-run command that shows you what changes Terraform is about to make.
 ↳ Command/Tool: terraform plan
 Use Case: When you want to double-check your work before touching any real production servers.

5. Building the Magic
 ↳ What: The command that actually creates the real infrastructure in your cloud account.
 ↳ Command/Tool: terraform apply
 Use Case: When your team lead says the staging environment is ready to be built.

6. Cleaning Up
 ↳ What: Safely deleting all the cloud resources you created so you don't get charged extra.
 ↳ Command/Tool: terraform destroy
 Use Case: When you finish your weekend testing and want to wipe the slate clean.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always run a plan before you apply so you never accidentally delete the wrong server.
 ↳ Never commit your cloud passwords or secret keys directly into your code files.

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-07/morning/terraform-in-5-minutes-infrastructure-as-code-explained-cheatsheet.pdf

---

*PDF: [terraform-in-5-minutes-infrastructure-as-code-explained-cheatsheet.pdf](terraform-in-5-minutes-infrastructure-as-code-explained-cheatsheet.pdf)*
