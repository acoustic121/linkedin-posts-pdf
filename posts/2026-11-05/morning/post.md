# Morning Post -- 2026-11-05

**Topic:** Cloud & DevOps Tips

---

Every junior DevOps engineer has copy-pasted the same Terraform resource block 5 times...
(with real examples you can use right now)

1. Basic Scaling with count
 ↳ What: A built-in counter that creates multiple identical copies of any resource.
 ↳ Command/Tool: count = 3 inside resource "aws_instance" "web"
 Use Case: When your team needs 3 identical EC2 instances spun up quickly for load testing.

2. Naming with count.index
 ↳ What: A zero-based index number you can inject directly into resource names and tags.
 ↳ Command/Tool: Name = "web-server-${count.index + 1}"
 Use Case: When your lead asks you to number 5 worker servers cleanly without writing 5 separate files.

3. Feature Flagging with count
 ↳ What: A trick using a ternary operator to deploy a resource only when a condition is true.
 ↳ Command/Tool: count = var.create_bastion ? 1 : 0
 Use Case: When you need an expensive bastion host in production, but want it turned off in dev to save money.

4. Named Resources with for_each
 ↳ What: A loop that builds distinct resources using a map of unique keys and values.
 ↳ Command/Tool: for_each = { dev = "t3.micro", prod = "t3.medium" }
 Use Case: When you need different VM sizes for each environment without duplicating your code.

5. Accessing Values with each.key & each.value
 ↳ What: Built-in pointers that reference the current item name and value inside a for_each loop.
 ↳ Command/Tool: instance_type = each.value with tag Name = each.key
 Use Case: When configuring S3 buckets where every bucket has its own unique name and retention policy.

6. Safe Lists with toset()
 ↳ What: A function that converts a plain list into a set so for_each can safely iterate over it.
 ↳ Command/Tool: for_each = toset(["app-logs", "app-backups", "app-media"])
 Use Case: When you have a list of team bucket names and want to avoid the dangerous index-shift bug of count.

7. Checking Single Items with -target
 ↳ What: A CLI flag to test or apply changes to just one specific item inside your loop.
 ↳ Command/Tool: terraform plan -target='aws_s3_bucket.storage["app-logs"]'
 Use Case: When you add one new item to a 20-item map and want to verify it before running a full apply.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Default to for_each over count whenever your resources have unique names or might be deleted individually.
 ↳ Never remove an item from the middle of a count list, or Terraform will recreate all items after it.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-05/morning/terraform-for_each-count-stop-copy-pasting-resource-blocks-cheatsheet.pdf

---

*PDF: [terraform-for_each-count-stop-copy-pasting-resource-blocks-cheatsheet.pdf](terraform-for_each-count-stop-copy-pasting-resource-blocks-cheatsheet.pdf)*
