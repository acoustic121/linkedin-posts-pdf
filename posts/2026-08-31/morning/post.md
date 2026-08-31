# Morning Post -- 2026-08-31

**Topic:** Cloud & DevOps Tips

---

Every developer has sent a Pull Request that took 3 days to review...
(with real examples you can use right now)

1. Keep PRs Small
 ↳ What: Break your work into tiny, bite-sized code changes instead of one huge update.
 ↳ Command/Tool: git diff --stat main..feature-branch
 Use Case: When you want your teammate to review your code in 5 minutes instead of 3 days.

2. Write Descriptive Titles
 ↳ What: Start your PR title with clear prefixes like feat, fix, or docs so everyone knows what changed.
 ↳ Command/Tool: gh pr create --title "fix: resolve login button timeout"
 Use Case: When your senior engineer opens GitHub and needs to know instantly what you fixed.

3. Clean Up Your Commit History
 ↳ What: Combine multiple messy "fixed typo" commits into one neat commit before requesting a review.
 ↳ Command/Tool: git rebase -i HEAD~3
 Use Case: When you made 10 tiny commits while testing and want to hide the messy trial-and-error.

4. Add a PR Template
 ↳ What: Use a standard checklist in your repository so you never forget to add context or test steps.
 ↳ Command/Tool: .github/PULL_REQUEST_TEMPLATE.md
 Use Case: When your manager asks "Did you test this on staging?" and you want to prove you did.

5. Sync Main Before Opening PR
 ↳ What: Bring the latest changes from the main branch into your branch to avoid merge conflicts early.
 ↳ Command/Tool: git fetch origin && git rebase origin/main
 Use Case: When three other teammates merged their code while you were working on your feature.

6. Self-Review Before Requesting Review
 ↳ What: Check your own diff on GitHub before tagging teammates to catch accidental debug prints.
 ↳ Command/Tool: git diff HEAD~1
 Use Case: When you want to catch leftover console logs before your reviewer sees them.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Keep PRs under 200 lines of code so reviewers can give fast, thoughtful feedback.
 ↳ Avoid submitting 2,000-line monster PRs right before Friday deployment.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Git #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-31/morning/pull-request-best-practices-every-team-should-follow-cheatsheet.pdf

---

*PDF: [pull-request-best-practices-every-team-should-follow-cheatsheet.pdf](pull-request-best-practices-every-team-should-follow-cheatsheet.pdf)*
