# Morning Post -- 2026-08-26

**Topic:** Cloud & DevOps Tips

---

Every developer has accidentally almost pushed an API key to GitHub...
(with real examples you can use right now)

1. .env Files
 ↳ What: A plain text file that holds secret keys and app settings outside your code.
 ↳ Command/Tool: cat .env
 Use Case: When you need to connect to a local database without hardcoding your password in the app.

2. Terminal Export
 ↳ What: A command to set temporary configuration variables directly inside your current terminal session.
 ↳ Command/Tool: export DB_PORT=5432
 Use Case: When you want to run a script with custom debug settings just once in your command prompt.

3. .gitignore File
 ↳ What: A security checklist file that tells Git to completely ignore secret configuration files.
 ↳ Command/Tool: echo ".env" >> .gitignore
 Use Case: When you are getting ready to push code to GitHub and want to block private keys from leaking.

4. Docker Environment Flags
 ↳ What: A way to pass configuration settings into a container when it boots up.
 ↳ Command/Tool: docker run -e APP_ENV=production my-app
 Use Case: When your containerized app needs to switch between local testing and live production mode.

5. Kubernetes Secrets
 ↳ What: A cluster object designed to securely store passwords and tokens for containerized apps.
 ↳ Command/Tool: kubectl create secret generic db-pass --from-literal=pass=1234
 Use Case: When your backend pods running in the cloud need database credentials injected at startup.

6. Cloud Secret Vaults
 ↳ What: A fully managed cloud service that stores, encrypts, and rotates production credentials.
 ↳ Command/Tool: aws secretsmanager get-secret-value --secret-id my-api-key
 Use Case: When your live production server needs to safely retrieve database credentials at runtime.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Keep a .env.example file with fake sample values in Git so your team knows which variables to set.
 ↳ Never print your full environment variables object in app logs to avoid exposing secrets in production.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Security #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-26/morning/environment-variables-secrets-manage-config-safely-cheatsheet.pdf

---

*PDF: [environment-variables-secrets-manage-config-safely-cheatsheet.pdf](environment-variables-secrets-manage-config-safely-cheatsheet.pdf)*
