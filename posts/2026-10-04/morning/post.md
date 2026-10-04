# Morning Post -- 2026-10-04

**Topic:** Cloud & DevOps Tips

---

Every developer has copy-pasted code to production and prayed it works...
(with real examples you can use right now)

1. Pipeline Stages
 ↳ What: The big steps your code takes from your laptop to the live server.
 ↳ Command/Tool: stages: [build, test, deploy]
 Use Case: When you want to make sure tests pass before your app actually goes live.

2. The Build Job
 ↳ What: Compiles your code or downloads all the libraries your app needs to run.
 ↳ Command/Tool: npm install or pip install
 Use Case: When your app needs fresh dependencies to run properly on the server.

3. The Test Job
 ↳ What: Automatically runs your code checks to catch bugs before users see them.
 ↳ Command/Tool: pytest or npm test
 Use Case: When your boss asks you to prove the new feature actually works.

4. The Deploy Job
 ↳ What: Sends your tested code safely to your cloud server or hosting platform.
 ↳ Command/Tool: rsync or AWS CLI
 Use Case: When the app is finally ready and you want the whole world to see it.

5. Image Definition
 ↳ What: The pre-built operating system environment where your pipeline steps run.
 ↳ Command/Tool: image: node:18 or image: python:3.9
 Use Case: When you need a clean computer to build your app without messing up your local machine.

6. Artifacts
 ↳ What: Saved files from one step that you need to pass along to the next step.
 ↳ Command/Tool: artifacts: paths: [dist/]
 Use Case: When your build step creates a final folder that your deploy step needs to upload.

7. Variables
 ↳ What: Secret passwords or environment settings kept safe outside your code.
 ↳ Command/Tool: GitLab CI/CD Settings -> Variables
 Use Case: When you need to connect to a database without putting your password in public GitHub code.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with a tiny .gitlab-ci.yml file and add steps one by one.
 ↳ Never hardcode your database passwords directly inside the YAML file.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #GitLab #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-04/morning/gitlab-cicd-build-test-deploy-with-one-gitlab-ciyml-cheatsheet.pdf

---

*PDF: [gitlab-cicd-build-test-deploy-with-one-gitlab-ciyml-cheatsheet.pdf](gitlab-cicd-build-test-deploy-with-one-gitlab-ciyml-cheatsheet.pdf)*
