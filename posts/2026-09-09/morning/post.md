# Morning Post -- 2026-09-09

**Topic:** Cloud & DevOps Tips

---

Writing the same 50 lines of Terraform for every new AWS environment gets old fast.
(with real examples you can use right now)

1. Calling a Local Module
 ↳ What: A way to package your Terraform files in a folder and run them like a single reusable function.
 ↳ Command/Tool: module "web_server" { source = "./modules/ec2" }
 Use Case: When you need the exact same EC2 setup for Dev, Staging, and Prod without duplicating code.

2. Defining Module Input Variables
 ↳ What: Parameter inputs that let you customize each module call (like setting server size or environment tag).
 ↳ Command/Tool: variable "instance_type" { default = "t3.micro" }
 Use Case: When your manager asks for a t3.micro in Dev but a c5.xlarge in Production.

3. Returning Module Outputs
 ↳ What: Values exported by a module so other parts of your infrastructure can read and use them.
 ↳ Command/Tool: output "vpc_id" { value = aws_vpc.main.id }
 Use Case: When your EC2 module needs the ID of the VPC created by your network module.

4. Using the Public Terraform Registry
 ↳ What: Pre-built, tested modules created by AWS, Azure, and the community that you can use instantly.
 ↳ Command/Tool: source = "terraform-aws-modules/vpc/aws"
 Use Case: When you need a production-ready AWS VPC with subnets and NAT gateways in 10 lines of code.

5. Initializing Module Dependencies
 ↳ What: The command that downloads and prepares all external and local modules before running plans.
 ↳ Command/Tool: terraform init
 Use Case: When you add a new module to your code and Terraform says it cannot find the source.

6. Pinning Module Versions
 ↳ What: Locking a remote module to a specific release so sudden upstream updates never break your infra.
 ↳ Command/Tool: version = "~> 5.0"
 Use Case: When an open-source module releases a breaking change while you are deploying on a Friday afternoon.

7. Multi-Instance Deployments with for_each
 ↳ What: Creating multiple identical module stacks across different regions or environments in one block.
 ↳ Command/Tool: for_each = toset(["us-east-1", "eu-west-1"])
 Use Case: When the business expands into Europe and wants an exact clone of your US app cluster.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start small: turn one simple S3 bucket with tagging into a reusable local folder module first.
 ↳ Never hardcode values like VPC IDs or region names inside a module—always pass them as variables.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-09/morning/terraform-modules-reuse-infrastructure-code-like-a-pro-cheatsheet.pdf

---

*PDF: [terraform-modules-reuse-infrastructure-code-like-a-pro-cheatsheet.pdf](terraform-modules-reuse-infrastructure-code-like-a-pro-cheatsheet.pdf)*
