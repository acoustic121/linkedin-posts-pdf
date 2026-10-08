# Morning Post -- 2026-10-08

**Topic:** Cloud & DevOps Tips

---

Choosing your first CI/CD tool feels like standing in a grocery store aisle with 50 brands of cereal.
(with real examples you can use right now)

1. Local GitHub Runner
 ↳ What: Run your GitHub Actions workflows locally on your laptop to test them instantly.
 ↳ Command/Tool: act
 Use Case: When you don't want to make 20 spam commit messages saying "fix pipeline error" just to test a change.

2. YAML Syntax Checker
 ↳ What: A quick validation tool to ensure your configuration files don't have spacing or formatting errors.
 ↳ Command/Tool: yamllint .github/workflows/main.yml
 Use Case: When your pipeline fails instantly because of an extra space you didn't notice.

3. GitLab CI Local Validator
 ↳ What: An API-based check to verify if your GitLab CI configuration is correct without running a real build.
 ↳ Command/Tool: curl --header "Content-Type: application/json" https://gitlab.com/api/v4/ci/lint
 Use Case: When you write a complex deployment flow and want to make sure GitLab understands it.

4. Docker-based Jenkins Runner
 ↳ What: Spin up a fresh, local Jenkins server in seconds without installing Java or configuring system settings.
 ↳ Command/Tool: docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts
 Use Case: When you want to practice building Jenkins pipelines safely without messing up your company's production server.

5. GitHub CLI Workflow Trigger
 ↳ What: A command-line utility to manually start a GitHub Actions workflow without pushing new code.
 ↳ Command/Tool: gh workflow run deploy.yml
 Use Case: When your manager asks you to redeploy the staging app right now without making any code changes.

6. Jenkins CLI Trigger
 ↳ What: A way to trigger Jenkins jobs directly from your terminal instead of clicking around the slow web UI.
 ↳ Command/Tool: java -jar jenkins-cli.jar -s http://localhost:8080/ build my-app-job
 Use Case: When you want to automate your development workflow by triggering a build directly from your local IDE.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with GitHub Actions because it requires zero installation and works directly with your GitHub repositories.
 ↳ Avoid writing massive shell scripts directly inside your YAML files; put them in a separate script file and run that instead.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #CICD #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-08/morning/jenkins-vs-gitlab-cicd-vs-github-actions-which-should-you-use-cheatsheet.pdf

---

*PDF: [jenkins-vs-gitlab-cicd-vs-github-actions-which-should-you-use-cheatsheet.pdf](jenkins-vs-gitlab-cicd-vs-github-actions-which-should-you-use-cheatsheet.pdf)*
