# Morning Post -- 2026-10-18

**Topic:** Cloud & DevOps Tips

---

Stop pasting permanent AWS access keys into GitHub repo secrets...
(with real examples you can use right now)

1. Enable the OIDC Token Permission
 ↳ What: Gives your GitHub Actions workflow permission to mint a temporary digital ID token.
 ↳ Command/Tool: permissions: { id-token: write, contents: read }
 Use Case: When your workflow needs to talk to AWS or GCP without you hardcoding a password.

2. Create the Cloud Identity Provider
 ↳ What: Tells your cloud account to trust GitHub as a legitimate login provider.
 ↳ Command/Tool: aws iam create-open-id-connect-provider --url https://token.actions.githubusercontent.com --client-id-list sts.amazonaws.com
 Use Case: When your security lead tells you to delete all permanent IAM user keys before the audit.

3. Lock Down the IAM Trust Policy
 ↳ What: Restricts cloud access so only your exact repository and branch can assume the role.
 ↳ Command/Tool: StringEquals: { "token.actions.githubusercontent.com:sub": "repo:org/app:ref:refs/heads/main" }
 Use Case: When you want to guarantee that only code merged into main can deploy to production.

4. Exchange Tokens for AWS Credentials
 ↳ What: The official GitHub Action that trades the GitHub token for short-lived cloud credentials.
 ↳ Command/Tool: uses: aws-actions/configure-aws-credentials@v4
 Use Case: When your pipeline needs to push a container to ECR without exposing long-lived access keys.

5. Test Caller Identity in the Pipeline
 ↳ What: An AWS CLI command to verify which role your pipeline is actually using.
 ↳ Command/Tool: aws sts get-caller-identity
 Use Case: When the build fails with Access Denied and you need to see who AWS thinks you are.

6. Cap the Session Duration
 ↳ What: Sets an automatic expiration timer so temporary credentials die right after your job runs.
 ↳ Command/Tool: role-duration-seconds: 900
 Use Case: When you want temporary credentials to expire in 15 minutes so nobody can reuse them.

7. Connect to Google Cloud with Workload Identity
 ↳ What: The Google Cloud equivalent that maps GitHub tokens directly to service account permissions.
 ↳ Command/Tool: uses: google-github-actions/auth@v2
 Use Case: When deploying a frontend build to Google Cloud Storage without downloading a JSON service key.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by setting the token lifetime to 15 minutes (900 seconds) so nothing lingers after deployment.
 ↳ Don't use wildcards (*) in your trust policy subject claim, or any public repo could assume your role.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #GitHubActions #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-18/morning/github-actions-oidc-connect-to-cloud-without-storing-secrets-cheatsheet.pdf

---

*PDF: [github-actions-oidc-connect-to-cloud-without-storing-secrets-cheatsheet.pdf](github-actions-oidc-connect-to-cloud-without-storing-secrets-cheatsheet.pdf)*
