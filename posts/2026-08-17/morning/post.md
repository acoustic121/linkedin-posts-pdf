# Morning Post -- 2026-08-17

**Topic:** Cloud & DevOps Tips

---

Every developer gets confused by Git branching at work...
(with real examples you can use right now)

1. Main Branch
 ↳ What: The safe, official branch that holds code live in production.
 ↳ Command/Tool: git checkout main
 Use Case: When you want to see what code is currently running live for real users.

2. Feature Branch
 ↳ What: A separate workspace to build new features without breaking main code.
 ↳ Command/Tool: git checkout -b feature/user-login
 Use Case: When your manager assigns you to build a new login button this week.

3. Hotfix Branch
 ↳ What: A quick emergency branch created directly from main to fix live bugs.
 ↳ Command/Tool: git checkout -b hotfix/fix-crash
 Use Case: When the app crashes at 3am and needs an immediate production fix.

4. Pull Request (PR)
 ↳ What: A review request asking your team to check your code before merging.
 ↳ Command/Tool: gh pr create --title "Add user login"
 Use Case: When you finish your feature and want senior developers to review it.

5. Syncing Branches
 ↳ What: Grabbing the latest updates from main into your feature branch.
 ↳ Command/Tool: git pull --rebase origin main
 Use Case: When your teammate merges their work and you need their updates locally.

6. Branch Cleanup
 ↳ What: Removing temporary feature branches after your code is merged.
 ↳ Command/Tool: git branch -d feature/user-login
 Use Case: When your pull request gets approved and you want to keep Git clean.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always pull the latest main branch before starting any new work.
 ↳ Never commit real secrets or credentials directly into feature branches.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Git #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-17/morning/git-branching-strategy-what-to-use-at-work-cheatsheet.pdf

---

*PDF: [git-branching-strategy-what-to-use-at-work-cheatsheet.pdf](git-branching-strategy-what-to-use-at-work-cheatsheet.pdf)*
