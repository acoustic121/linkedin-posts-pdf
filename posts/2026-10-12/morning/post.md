# Morning Post -- 2026-10-12

**Topic:** Cloud & DevOps Tips

---

Every developer has accidentally pasted a password into GitHub at least once.
(with real examples you can use right now)

1. What are GitHub Secrets
 ↳ What: A safe vault inside GitHub to store passwords and API keys so nobody can steal them.
 ↳ Command/Tool: GitHub Settings > Secrets and variables > Actions
 Use Case: When your app needs to talk to a database without exposing your password in the code.

2. Adding Your First Secret
 ↳ What: Creating a secure name-and-value pair that your code can read like a hidden variable.
 ↳ Command/Tool: Click 'New repository secret'
 Use Case: When you get an API key from a service like WeatherAPI and need to use it in your build pipeline.

3. Using Secrets in YAML Files
 ↳ What: Calling your saved secret inside a workflow file using special environment syntax.
 ↳ Command/Tool: ${{ secrets.MY_API_KEY }}
 Use Case: When your automated test script needs to log into a third-party tool safely.

4. Masking Secrets in Logs
 ↳ What: A built-in GitHub feature that automatically hides your sensitive passwords with stars (***) if they print on screen.
 ↳ Command/Tool: echo "::add-mask::${{ secrets.MY_SECRET }}"
 Use Case: When a debugging step accidentally tries to print your password in the console logs.

5. Environment-Specific Secrets
 ↳ What: Creating separate secrets for testing and production so your dev code can't touch live money.
 ↳ Command/Tool: GitHub Environments feature
 Use Case: When your staging deployment needs a different database key than your live website.

6. Checking for Leaks Early
 ↳ What: A tool that scans your code before you upload it to make sure no passwords are hiding in plain sight.
 ↳ Command/Tool: trufflehog or gitlint
 Use Case: When you want to double-check your code before your boss finds a security bug.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always name your secrets in ALL_CAPS so they are easy to spot.
 ↳ Never print your secret values directly in your workflow run commands.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #GitHub #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-12/morning/github-actions-secrets-store-api-keys-the-safe-way-cheatsheet.pdf

---

*PDF: [github-actions-secrets-store-api-keys-the-safe-way-cheatsheet.pdf](github-actions-secrets-store-api-keys-the-safe-way-cheatsheet.pdf)*
