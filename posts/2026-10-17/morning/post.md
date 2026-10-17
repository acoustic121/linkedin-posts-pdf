# Morning Post -- 2026-10-17

**Topic:** Cloud & DevOps Tips

---

Every developer has accidentally pushed broken code or an API key and immediately regretted it.
(with real examples you can use right now)

1. Pre-Commit Hook
 ↳ What: A local script that runs automatically right before Git creates your commit.
 ↳ Command/Tool: .git/hooks/pre-commit
 Use Case: Catching formatting bugs and syntax errors before they ever leave your laptop.

2. Secret Scanner Check
 ↳ What: A security check that blocks commits containing API keys, AWS credentials, or passwords.
 ↳ Command/Tool: gitleaks protect --staged
 Use Case: When you accidentally paste a database password into your code while testing.

3. Husky Framework
 ↳ What: A modern tool that shares Git hooks with your entire team via package config.
 ↳ Command/Tool: npx husky init
 Use Case: When onboarding a new junior dev and you want their hooks configured automatically.

4. Commit Message Validator
 ↳ What: A gatekeeper hook that ensures commit messages follow standard naming rules.
 ↳ Command/Tool: .git/hooks/commit-msg
 Use Case: When your team requires ticket IDs like "JIRA-101: fix navbar" in every commit.

5. Code Linter & Formatter
 ↳ What: An automated check that formats code cleanly so commits stay uniform.
 ↳ Command/Tool: npx prettier --check .
 Use Case: When teammates waste time arguing over tabs versus spaces in pull request reviews.

6. Pre-Push Test Runner
 ↳ What: A safety check that runs your unit tests before your branch hits GitHub.
 ↳ Command/Tool: .git/hooks/pre-push
 Use Case: When you want to be 100% sure your changes won't break the shared develop branch.

7. The Emergency Bypass
 ↳ What: A built-in Git flag that lets you skip all local hook checks in an emergency.
 ↳ Command/Tool: git commit -m "hotfix" --no-verify
 Use Case: When production is down at 2am and you need to push a one-line emergency patch instantly.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Keep pre-commit hooks fast; if they take over 5 seconds, devs will bypass them.
 ↳ Remember that files inside .git/hooks are never pushed to GitHub—use Husky or pre-commit framework to share them.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Git #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-17/morning/git-hooks-automate-checks-before-every-commit-cheatsheet.pdf

---

*PDF: [git-hooks-automate-checks-before-every-commit-cheatsheet.pdf](git-hooks-automate-checks-before-every-commit-cheatsheet.pdf)*
