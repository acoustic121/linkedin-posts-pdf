# Morning Post -- 2026-10-05

**Topic:** Cloud & DevOps Tips

---

Every developer has panicked after pushing a broken deployment to Kubernetes...
(with real examples you can use right now)

1. See Your History
 ↳ What: A command to view all the previous versions (revisions) of your app deployment.
 ↳ Command/Tool: helm history my-app
 Use Case: When your app crashes and you need to see which version was working before.

2. The 1-Second Rollback
 ↳ What: A command that instantly takes your application back to its previous working version.
 ↳ Command/Tool: helm rollback my-app 1
 Use Case: When your 3 AM deployment fails and you need to restore the site immediately.

3. The Safety Preview
 ↳ What: A way to test your deployment changes without actually applying them to the live cluster.
 ↳ Command/Tool: helm upgrade --install my-app ./charts/my-app --dry-run
 Use Case: When you want to make sure your configuration is correct before making live changes.

4. Check Current Status
 ↳ What: A quick way to see if your current application release is healthy or failed.
 ↳ Command/Tool: helm status my-app
 Use Case: When your boss asks, "Is the app deployment finished and running successfully?"

5. Find Your Deployments
 ↳ What: A command to list all the active applications managed by Helm in your namespace.
 ↳ Command/Tool: helm list
 Use Case: When you join a new project and want to see what applications are already running.

6. Inspect Config Settings
 ↳ What: A command to see exactly what settings and variables were used in your deployment.
 ↳ Command/Tool: helm get values my-app
 Use Case: When you need to check if you accidentally deployed with the wrong database URL.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always check your history before rolling back to make sure you target the correct version.
 ↳ Don't manually delete Kubernetes pods to "fix" a bad deployment—use Helm's rollback instead.

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-05/morning/helm-rollback-undo-a-bad-release-in-under-30-seconds-cheatsheet.pdf

---

*PDF: [helm-rollback-undo-a-bad-release-in-under-30-seconds-cheatsheet.pdf](helm-rollback-undo-a-bad-release-in-under-30-seconds-cheatsheet.pdf)*
