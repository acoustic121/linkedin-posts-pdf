# Morning Post -- 2026-09-29

**Topic:** Cloud & DevOps Tips

---

Remember the panic when code works locally but breaks on the server?
(with real examples you can use right now)

1. Jenkinsfile Setup
 ↳ What: A text file where you write down the steps to build and test your app automatically.
 ↳ Command/Tool: touch Jenkinsfile
 Use Case: When your team lead asks you to make the build process repeatable so anyone can run it.

2. Pipeline Block
 ↳ What: The main container that holds all the instructions for your automation.
 ↳ Command/Tool: pipeline { agent any }
 Use Case: When you need to tell Jenkins to run the job on any available computer.

3. Stages and Steps
 ↳ What: Breaking your work into clear chapters like building, testing, and deploying.
 ↳ Command/Tool: stage('Build') { steps { sh 'npm install' } }
 Use Case: When you want to see exactly which part of your app failed during an update.

4. Shell Commands in Jenkins
 ↳ What: Running normal terminal commands directly inside your automated pipeline.
 ↳ Command/Tool: sh 'npm test'
 Use Case: When you need to run your unit tests before letting the code go live.

5. Environment Variables
 ↳ What: Secret or dynamic settings like passwords or version numbers passed safely to your app.
 ↳ Command/Tool: environment { API_KEY = credentials('my-secret-key') }
 Use Case: When your app needs a secret database password without exposing it in the public code.

6. Post Actions
 ↳ What: What Jenkins should do after the build finishes, like sending a success message.
 ↳ Command/Tool: post { success { echo 'Deployment passed!' } }
 Use Case: When you want your team to get notified on Slack the moment a fix goes live.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with a tiny pipeline that just prints 'Hello World' before adding complex steps.
 ↳ Avoid hardcoding passwords directly inside your pipeline script.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Jenkins #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-29/morning/jenkins-pipelines-automate-your-builds-from-scratch-cheatsheet.pdf

---

*PDF: [jenkins-pipelines-automate-your-builds-from-scratch-cheatsheet.pdf](jenkins-pipelines-automate-your-builds-from-scratch-cheatsheet.pdf)*
