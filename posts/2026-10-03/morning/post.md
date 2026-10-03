# Morning Post -- 2026-10-03

**Topic:** Cloud & DevOps Tips

---

Deploying code without running database migrations first usually breaks everything in production.
(with real examples you can use right now)

1. Pre-install Hook
 ↳ What: Runs a Kubernetes Job before your application pods are created.
 ↳ Command/Tool: helm.sh/hook: pre-install
 Use Case: When you need to set up database schemas before your app starts up.

2. Post-install Hook
 ↳ What: Runs a task right after your application successfully installs.
 ↳ Command/Tool: helm.sh/hook: post-install
 Use Case: When your team wants a Slack notification as soon as a new app goes live.

3. Pre-upgrade Hook
 ↳ What: Triggers a job before Helm updates an existing app release.
 ↳ Command/Tool: helm.sh/hook: pre-upgrade
 Use Case: When your boss asks you to back up the database right before updating the software.

4. Post-upgrade Hook
 ↳ What: Runs a script immediately after a successful application upgrade.
 ↳ Command/Tool: helm.sh/hook: post-upgrade
 Use Case: When you need to clear the Redis cache right after deploying new code.

5. Hook Weight
 ↳ What: Sets the exact execution order when you have multiple hooks running together.
 ↳ Command/Tool: helm.sh/hook-weight: "-5"
 Use Case: When you must run a network check before running your database migration script.

6. Hook Delete Policy
 ↳ What: Automatically cleans up temporary hook pods so they do not clutter your cluster.
 ↳ Command/Tool: helm.sh/hook-delete-policy: hook-succeeded
 Use Case: When your cluster gets messy because completed job pods stick around forever.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always test hooks locally with minikube or kind before running them in production.
 ↳ Don't forget to add a delete policy, or completed hook pods will stack up forever.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-03/morning/helm-hooks-run-jobs-before-and-after-a-kubernetes-deploy-cheatsheet.pdf

---

*PDF: [helm-hooks-run-jobs-before-and-after-a-kubernetes-deploy-cheatsheet.pdf](helm-hooks-run-jobs-before-and-after-a-kubernetes-deploy-cheatsheet.pdf)*
