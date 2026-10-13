# Morning Post -- 2026-10-13

**Topic:** Cloud & DevOps Tips

---

You are halfway through a feature and your manager says: "Drop everything, production is down."
(with real examples you can use right now)

1. Quick Save
 ↳ What: Temporarily hides your uncommitted changes so your workspace is clean.
 ↳ Command/Tool: git stash
 Use Case: When you need to switch branches immediately without committing broken code.

2. Stash with a Label
 ↳ What: Saves your uncommitted work with a custom message so you know what it is later.
 ↳ Command/Tool: git stash push -m "wip: checkout button fix"
 Use Case: When you juggle multiple tasks and don't want to guess what stash@{0} contains.

3. Include New Files
 ↳ What: Saves modified files plus brand-new untracked files you just created.
 ↳ Command/Tool: git stash -u
 Use Case: When standard git stash ignores the new files you just added to the project.

4. View Your Saved Work
 ↳ What: Lists every stash you have saved along with their IDs and messages.
 ↳ Command/Tool: git stash list
 Use Case: When you return from the weekend and need to see what you paused on Friday.

5. Restore and Delete
 ↳ What: Re-applies your latest stashed changes and removes them from the stash list.
 ↳ Command/Tool: git stash pop
 Use Case: When the urgent bug is resolved and you are ready to continue your feature.

6. Restore Without Deleting
 ↳ What: Re-applies your stashed changes but keeps the stash saved in your list as a backup.
 ↳ Command/Tool: git stash apply
 Use Case: When you want to test your stashed code across two different branches safely.

7. Clean Up Old Stashes
 ↳ What: Deletes a specific stash you no longer need so your list stays tidy.
 ↳ Command/Tool: git stash drop stash@{0}
 Use Case: When an experiment failed and you want to discard the shelved code permanently.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always add a message with `git stash push -m` so you never lose context.
 ↳ Don't treat stash like long-term storage; finish or commit it within a few days.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Git #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-13/morning/git-stash-save-your-work-without-committing-cheatsheet.pdf

---

*PDF: [git-stash-save-your-work-without-committing-cheatsheet.pdf](git-stash-save-your-work-without-committing-cheatsheet.pdf)*
