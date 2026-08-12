# Morning Post -- 2026-08-12

**Topic:** Cloud & DevOps Tips

---

Ever got hit with an 'Access Denied' error in the cloud at 2 PM?
(with real examples you can use right now)

1. IAM Users
 ↳ What: A permanent identity created for a person or application to log into AWS.
 ↳ Command/Tool: aws iam create-user --user-name john-doe
 Use Case: When a new junior developer joins your engineering team on Monday morning.

2. IAM Groups
 ↳ What: A collection of users that all share the exact same permissions.
 ↳ Command/Tool: aws iam create-group --group-name Developers
 Use Case: When you want to give 10 new developers read access without setting permissions 10 times.

3. IAM Policies
 ↳ What: A JSON document that explicitly grants or denies access to specific services.
 ↳ Command/Tool: aws iam attach-user-policy --policy-arn arn:aws:iam::aws:policy/ReadOnlyAccess --user-name john-doe
 Use Case: When your manager asks you to let the intern view database logs but prevent them from deleting tables.

4. IAM Roles
 ↳ What: A temporary permission badge that a service or user can assume for a short time.
 ↳ Command/Tool: aws iam create-role --role-name EC2S3Role --assume-role-policy-document file://trust-policy.json
 Use Case: When your app running on EC2 needs to upload images to S3 without saving passwords inside the code.

5. Access Keys
 ↳ What: A secret key pair used to authenticate terminal CLI tools and automation scripts.
 ↳ Command/Tool: aws iam create-access-key --user-name john-doe
 Use Case: When you want to run cloud commands from your laptop terminal instead of clicking in the browser web console.

6. Multi-Factor Authentication (MFA)
 ↳ What: An extra security layer requiring a temporary phone code along with your password.
 ↳ Command/Tool: aws iam enable-mfa-device --user-name john-doe --serial-number arn:aws:iam::123456789012:mfa/john-doe --authentication-code1 123456 --authentication-code2 654321
 Use Case: When you want to protect your production cloud environment from being hacked if credentials leak.

7. Policy Simulator
 ↳ What: A testing tool to check if a permission works before applying it to real users.
 ↳ Command/Tool: aws iam simulate-principal-policy --policy-source-arn arn:aws:iam::123456789012:user/john-doe --action-names s3:GetObject
 Use Case: When you want to double-check that a new dev can read files without accidentally granting delete access.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by creating a read-only user and observe what happens when you attempt to delete resources.
 ↳ Never commit hardcoded IAM Access Keys or Secrets into public GitHub repositories!

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #AWS #IAM #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-12/morning/what-is-iam-cloud-permissions-made-simple-cheatsheet.pdf

---

*PDF: [what-is-iam-cloud-permissions-made-simple-cheatsheet.pdf](what-is-iam-cloud-permissions-made-simple-cheatsheet.pdf)*
