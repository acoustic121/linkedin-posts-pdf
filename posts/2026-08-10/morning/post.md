# Morning Post -- 2026-08-10

**Topic:** Cloud & DevOps Tips

---

We have all broken our code with a wrong Git command and panicked just a little.
(with real examples you can use right now)

1. Discard uncommitted local changes
 ↳ What: Throw away edits you haven't saved to your history yet, like erasing a messy whiteboard drawing.
 ↳ Command/Tool: git restore filename.txt
 Use Case: When you mess up a file while experimenting and just want to start over from the last saved state.

2. Unstage a file you added by mistake
 ↳ What: Take a file out of your staging area without losing the changes inside it.
 ↳ Command/Tool: git restore --staged filename.txt
 Use Case: When you accidentally typed `git add .` and included a temporary log file you didn't mean to track.

3. Undo your last commit but keep your code
 ↳ What: Step back in time by one commit while keeping all your recent code changes safely on your screen.
 ↳ Command/Tool: git reset --soft HEAD~1
 Use Case: When you realize you forgot to add one tiny file to your very last commit.

4. Erase your last commit and your changes
 ↳ What: Travel back in time and completely wipe out your last commit and any changes tied to it.
 ↳ Command/Tool: git reset --hard HEAD~1
 Use Case: When you completely went down the wrong path and want to pretend the last 30 minutes never happened.

5. Safely undo a public commit
 ↳ What: Create a brand new commit that does the exact opposite of an old mistake, like hitting the 'undo' button in a shared document.
 ↳ Command/Tool: git revert <commit-hash>
 Use Case: When a bad update broke the app in production and your team needs a clean fix without messing up history.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always run `git status` before typing any reset command to see where you stand
 ↳ Never use `git reset --hard` on code that has already been pushed to a shared team branch

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Git #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-10/morning/how-to-undo-mistakes-in-git-git-reset-revert-restore-cheatsheet.pdf

---

*PDF: [how-to-undo-mistakes-in-git-git-reset-revert-restore-cheatsheet.pdf](how-to-undo-mistakes-in-git-git-reset-revert-restore-cheatsheet.pdf)*
