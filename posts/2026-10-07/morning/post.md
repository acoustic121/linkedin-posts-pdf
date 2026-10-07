# Morning Post -- 2026-10-07

**Topic:** Cloud & DevOps Tips

---

Storing API keys in plain text on GitHub is like leaving your house keys under the doormat with a sign pointing to them.
(with real examples you can use right now)

1. Installing the Plugin
 ↳ What: Adding the secrets plugin to your Helm setup so you can encrypt files.
 ↳ Command/Tool: helm plugin install https://github.com/jkroepke/helm-secrets
 Use Case: When you are setting up your laptop for a new project and need to handle database passwords securely.

2. Generating Encryption Keys
 ↳ What: Creating a secure key pair with Age to lock and unlock your secret files.
 ↳ Command/Tool: age-keygen -o key.txt
 Use Case: When you need a quick, free way to encrypt files locally without paying for complex cloud setups.

3. Encrypting Your Secrets File
 ↳ What: Turning your plain-text database passwords into unreadable gibberish.
 ↳ Command/Tool: export SOPS_AGE_KEY_FILE=$(pwd)/key.txt && helm secrets encrypt -i secrets.yaml
 Use Case: When your boss asks you to commit the database password to Git but you want to keep your job.

4. Viewing Encrypted Secrets Safely
 ↳ What: Reading the hidden content in your terminal without saving it to a plain-text file.
 ↳ Command/Tool: export SOPS_AGE_KEY_FILE=$(pwd)/key.txt && helm secrets view secrets.yaml
 Use Case: When you need to double-check if you typed the API key correctly before deploying.

5. Editing Secrets on the Fly
 ↳ What: Opening and modifying your encrypted secrets directly in your favorite terminal editor.
 ↳ Command/Tool: export SOPS_AGE_KEY_FILE=$(pwd)/key.txt && helm secrets edit secrets.yaml
 Use Case: When the database team changes the password at 3 AM and you need to update it immediately.

6. Deploying with Secrets
 ↳ What: Telling Helm to decrypt your secrets in memory and deploy them directly to Kubernetes.
 ↳ Command/Tool: export SOPS_AGE_KEY_FILE=$(pwd)/key.txt && helm secrets upgrade --install my-app ./my-chart -f values.yaml -f secrets.yaml
 Use Case: When you want to roll out a new feature without exposing any passwords in your CI/CD logs.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always add your private key files (like key.txt) to your .gitignore file immediately.
 ↳ Never commit your raw private keys to Git, even if you think the repository is private.

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-07/morning/helm-secrets-plugin-keep-sensitive-values-out-of-git-cheatsheet.pdf

---

*PDF: [helm-secrets-plugin-keep-sensitive-values-out-of-git-cheatsheet.pdf](helm-secrets-plugin-keep-sensitive-values-out-of-git-cheatsheet.pdf)*
