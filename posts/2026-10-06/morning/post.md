# Morning Post -- 2026-10-06

**Topic:** Cloud & DevOps Tips

---

Ever had code that worked perfectly on your Mac, but crashed instantly on your teammate's Windows laptop?
(with real examples you can use right now)

1. The Matrix Strategy
 ↳ What: A feature that lets you run the same test suite across different operating systems and versions at the same time.
 ↳ Command/Tool: strategy: matrix
 Use Case: When you want to verify your app works on Ubuntu, macOS, and Windows without writing three separate workflows.

2. OS Runner Selection
 ↳ What: Choosing the virtual machines provided by GitHub to run your tests on.
 ↳ Command/Tool: runs-on: ${{ matrix.os }}
 Use Case: When your boss asks you to prove that the new update doesn't break on Windows servers.

3. Node/Language Version Matrix
 ↳ What: Testing your code against multiple versions of programming languages simultaneously.
 ↳ Command/Tool: node-version: [18, 20, 22]
 Use Case: When you want to upgrade your app to Node 22 but need to make sure it doesn't break for users still on Node 18.

4. Excluding Specific Combinations
 ↳ What: Skipping certain setups that you know don't work or aren't needed to save build time and money.
 ↳ Command/Tool: exclude:
 Use Case: When you want to test macOS with Node 20 and 22, but need to skip testing Node 18 on macOS because it's not supported.

5. Including Extra Variables
 ↳ What: Adding custom configurations or unique settings to a specific runner in your matrix.
 ↳ Command/Tool: include:
 Use Case: When you need to add an experimental flag only for the Ubuntu-latest and Node 22 combination.

6. Max Parallel Jobs
 ↳ What: Limiting how many tests run at the exact same time to avoid hitting GitHub's free-tier limits.
 ↳ Command/Tool: max-parallel: 2
 Use Case: When your team's build queue gets clogged because too many OS tests are running all at once.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start small with just two operating systems before adding complex language versions.
 ↳ Avoid running huge matrix tests on every single tiny commit to keep your build times fast.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #GitHubActions #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-06/morning/github-actions-matrix-builds-test-on-multiple-os-at-once-cheatsheet.pdf

---

*PDF: [github-actions-matrix-builds-test-on-multiple-os-at-once-cheatsheet.pdf](github-actions-matrix-builds-test-on-multiple-os-at-once-cheatsheet.pdf)*
