# Morning Post -- 2026-10-16

**Topic:** Cloud & DevOps Tips

---

Tired of paying GitHub for extra pipeline minutes or waiting in long build queues?
(with real examples you can use right now)

1. Download Runner Package
 ↳ What: Downloads the official GitHub runner software onto your personal cloud server.
 ↳ Command/Tool: curl -o runner.tar.gz -L https://github.com/actions/runner/releases/download/v2.314.0/actions-runner-linux-x64-2.314.0.tar.gz
 Use Case: When you want to set up a private EC2 instance as your personal build machine.

2. Extract Runner Files
 ↳ What: Unpacks the downloaded runner package so it is ready for configuration.
 ↳ Command/Tool: tar xzf ./runner.tar.gz
 Use Case: When preparing the installation files in your server terminal.

3. Configure Runner Connection
 ↳ What: Connects your local server to your GitHub repository using a secure token.
 ↳ Command/Tool: ./config.sh --url https://github.com/user/repo --token YOUR_GITHUB_TOKEN
 Use Case: When your team needs your cloud server to listen for incoming GitHub code changes.

4. Install Background Service
 ↳ What: Keeps the runner process active continuously in the background even after system reboots.
 ↳ Command/Tool: sudo ./svc.sh install && sudo ./svc.sh start
 Use Case: When your server reboots at midnight and you still need builds to work the next morning.

5. Target Custom Server in Workflow
 ↳ What: Directs your GitHub pipeline to run on your server instead of GitHub cloud machines.
 ↳ Command/Tool: runs-on: self-hosted
 Use Case: When your app deployment needs direct access to databases in your private cloud network.

6. Route Jobs with Custom Labels
 ↳ What: Sends specific heavy tasks to high-performance servers using tags.
 ↳ Command/Tool: runs-on: [self-hosted, linux, high-ram]
 Use Case: When your boss asks you to run a massive data process on a high-memory server.

7. Check Runner Status
 ↳ What: Verifies if your runner service is actively running and waiting for jobs.
 ↳ Command/Tool: sudo ./svc.sh status
 Use Case: When a build gets stuck and you need to see if your server agent is offline.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by testing self-hosted runners on a personal practice repository before using them in real work apps.
 ↳ Never attach self-hosted runners to public repositories, as open-source pull requests can execute unsafe code on your server.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #GitHubActions #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-16/morning/github-actions-self-hosted-runners-run-pipelines-on-your-server-cheatsheet.pdf

---

*PDF: [github-actions-self-hosted-runners-run-pipelines-on-your-server-cheatsheet.pdf](github-actions-self-hosted-runners-run-pipelines-on-your-server-cheatsheet.pdf)*
