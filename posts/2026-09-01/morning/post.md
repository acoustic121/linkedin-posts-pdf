# Morning Post -- 2026-09-01

**Topic:** Cloud & DevOps Tips

---

Ever pushed code to production at 2 PM and broken the app for thousands of active users?
(with real examples you can use right now)

1. Rolling Update
 ↳ What: Replaces old instances of your app with new ones step-by-step so your site stays up.
 ↳ Command/Tool: kubectl set image deployment/myapp myapp=myapp:v2
 Use Case: When your boss asks you to update the app without kicking off active users.

2. Readiness Probes
 ↳ What: Tells your server to wait until the app is fully booted before sending user traffic.
 ↳ Command/Tool: readinessProbe: httpGet: { path: /health, port: 8080 }
 Use Case: When your app crashes at 3am because traffic hit it before the database connected.

3. Blue-Green Deployment
 ↳ What: Runs two identical environments so you can switch 100% of traffic to new code instantly.
 ↳ Command/Tool: sudo nginx -s reload
 Use Case: When you need an instant 1-second rollback plan just in case the release fails.

4. Canary Release
 ↳ What: Sends 5% of real user traffic to new code first to test if it breaks.
 ↳ Command/Tool: kubectl argo rollouts promote my-app
 Use Case: When you want to test a risky new feature on a tiny audience first.

5. Graceful Shutdown
 ↳ What: Gives your app time to finish active user requests before closing down completely.
 ↳ Command/Tool: process.on('SIGTERM', () => server.close())
 Use Case: When users lose their filled shopping cart because the app restarted abruptly.

6. Database Expansion Migration
 ↳ What: Adding database columns as optional first so old and new code run together seamlessly.
 ↳ Command/Tool: ALTER TABLE users ADD COLUMN age INT DEFAULT NULL;
 Use Case: When your running app breaks because someone renamed a database column live.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always set readiness probes so traffic never hits an app while it is still booting.
 ↳ Never delete or rename database columns in the exact same release as new app code.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #ZeroDowntime #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-01/morning/how-to-deploy-code-without-downtime-zero-downtime-deploys-cheatsheet.pdf

---

*PDF: [how-to-deploy-code-without-downtime-zero-downtime-deploys-cheatsheet.pdf](how-to-deploy-code-without-downtime-zero-downtime-deploys-cheatsheet.pdf)*
