# Morning Post -- 2026-10-14

**Topic:** Cloud & DevOps Tips

---

Every developer has waited way too long for their GitHub pipeline to finish building...
(with real examples you can use right now)

1. The Problem: Downloading the Internet Every Time
 ↳ What: GitHub Actions starts a fresh, empty computer for every run, meaning it re-downloads all your project libraries from scratch.
 ↳ Command/Tool: actions/checkout
 Use Case: When your tests take 10 minutes just because it downloads node_modules every single time you push code.

2. The Solution: GitHub Caching
 ↳ What: Saving your downloaded libraries in a secret folder so the next run skips the download step entirely.
 ↳ Command/Tool: actions/cache
 Use Case: When your boss asks why the CI pipeline takes longer than your lunch break.

3. Caching Node Modules (JavaScript/TypeScript)
 ↳ What: Specifically saving your node_modules folder based on the lock file.
 ↳ Command/Tool: actions/setup-node
 Use Case: When you just want your React app to build in 30 seconds instead of 5 minutes.

4. Caching Python Packages (Pip)
 ↳ What: Storing your pip cache directory so pip install only grabs new packages.
 ↳ Command/Tool: actions/cache
 Use Case: When your data science script takes forever installing pandas and numpy on every commit.

5. Cache Key (The Magic Label)
 ↳ What: A unique label using your lock file hash so GitHub knows when to update the cache.
 ↳ Command/Tool: hashFiles('package-lock.json')
 Use Case: When someone adds a new dependency and you need the cache to automatically refresh.

6. Cache Restore (Bringing It Back)
 ↳ What: Looking for an existing saved cache before running your package manager.
 ↳ Command/Tool: restore-keys
 Use Case: When your exact lock file isn't found, but a slightly older cache can still save you 80% of download time.

7. Saving Storage Space
 ↳ What: GitHub automatically deletes caches that haven't been used in over 7 days to keep things tidy.
 ↳ Command/Tool: GitHub Actions Settings
 Use Case: When you want to clean up old clutter without manually managing storage.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always base your cache key on your lock file so it updates when dependencies change.
 ↳ Don't cache huge, unnecessary build folders that change on every single commit.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #GitHubActions #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-14/morning/github-actions-caching-speed-up-your-workflows-for-free-cheatsheet.pdf

---

*PDF: [github-actions-caching-speed-up-your-workflows-for-free-cheatsheet.pdf](github-actions-caching-speed-up-your-workflows-for-free-cheatsheet.pdf)*
