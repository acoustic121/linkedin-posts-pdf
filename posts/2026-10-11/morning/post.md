# Morning Post -- 2026-10-11

**Topic:** Cloud & DevOps Tips

---

Every developer wonders what "v1.2.3" actually means when releasing code...
(with real examples you can use right now)

1. Annotated Git Tag
 ↳ What: A permanent bookmark on a specific commit with a message and author details.
 ↳ Command/Tool: git tag -a v1.0.0 -m "First stable production release"
 Use Case: When your team finishes sprint work and you need an exact snapshot of production code.

2. Semantic Versioning: PATCH
 ↳ What: Bumping the last number when you fix bugs without breaking existing features.
 ↳ Command/Tool: git tag -a v1.0.1 -m "Fix login button crash"
 Use Case: When your app crashes at 2 AM and you need to push a quick emergency hotfix.

3. Semantic Versioning: MINOR
 ↳ What: Bumping the middle number when you add new features in a backward-compatible way.
 ↳ Command/Tool: git tag -a v1.1.0 -m "Add export to CSV feature"
 Use Case: When your product manager asks you to release a brand new feature users can try out.

4. Semantic Versioning: MAJOR
 ↳ What: Bumping the first number when you introduce breaking changes that require users to update their setup.
 ↳ Command/Tool: git tag -a v2.0.0 -m "Rewrite auth API with breaking changes"
 Use Case: When your team redesigns the database schema or drops support for old API endpoints.

5. Push Tags to Remote
 ↳ What: Git does not push tags automatically, so you must explicitly sync them to GitHub.
 ↳ Command/Tool: git push origin v1.1.0 (or git push origin --tags)
 Use Case: When your code is on GitHub but your CI/CD pipeline fails to trigger without the release tag.

6. List and Verify Existing Tags
 ↳ What: Display all release tags saved in your repository in alphabetical order.
 ↳ Command/Tool: git tag -l -n
 Use Case: When your team lead asks which exact version was shipped last Tuesday.

7. Checkout a Specific Release
 ↳ What: Switch your working directory to the exact code state of an older release tag.
 ↳ Command/Tool: git checkout v1.0.0
 Use Case: When a customer reports a bug that only happens in an older version of your app.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always prefer annotated tags (`-a`) over lightweight tags so you preserve who tagged the release and why.
 ↳ Never change or reuse an existing tag name after pushing it to production; bump the patch version instead.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Git #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-11/morning/git-tags-semantic-versioning-release-your-code-properly-cheatsheet.pdf

---

*PDF: [git-tags-semantic-versioning-release-your-code-properly-cheatsheet.pdf](git-tags-semantic-versioning-release-your-code-properly-cheatsheet.pdf)*
