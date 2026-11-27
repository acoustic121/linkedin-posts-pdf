# Morning Post -- 2026-11-27

**Topic:** Cloud & DevOps Tips

---

Remember the last time you spent three hours configuring an Ubuntu server just to run a simple Node.js app?
(with real examples you can use right now)

1. App Service Plan
 ↳ What: The invisible virtual machine infrastructure that gives your web app CPU and memory.
 ↳ Command/Tool: az appservice plan create --name myPlan --resource-group myRG --sku B1
 Use Case: When your boss asks you to host three websites without paying for three separate servers.

2. Web App Creation
 ↳ What: The actual container where your code lives and runs on a public URL.
 ↳ Command/Tool: az webapp create --name myCoolApp --resource-group myRG --plan myPlan
 Use Case: When you built a cool project over the weekend and want to share the live link with friends in 60 seconds.

3. Git Deployment
 ↳ What: Pushing your code straight from your laptop to the cloud without messing with FTP or servers.
 ↳ Command/Tool: az webapp up --name myCoolApp --resource-group myRG --html
 Use Case: When you just fixed a tiny typo in your HTML file and want it live on the internet immediately.

4. Environment Variables
 ↳ What: Secret settings like database passwords that you keep out of your code files.
 ↳ Command/Tool: az webapp config appsettings set --name myCoolApp --resource-group myRG --settings DATABASE_URL=my_secret
 Use Case: When your app needs to talk to a database without you accidentally leaking passwords on GitHub.

5. Live Streaming Logs
 ↳ What: Watching your app's live terminal output in real-time to catch bugs.
 ↳ Command/Tool: az webapp log tail --name myCoolApp --resource-group myRG
 Use Case: When users report a 500 error at 3 AM and you need to see the exact crash message instantly.

6. Automatic Scaling
 ↳ What: Letting Azure automatically add more server power when too many people visit your site.
 ↳ Command/Tool: az monitor autoscale create --resource-group myRG --resource myPlan
 Use Case: When your startup gets featured on Product Hunt and traffic suddenly spikes by 10,000%.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always start with the cheapest 'Free' or 'Basic' pricing tier while learning.
 ↳ Never hardcode database passwords directly into your source code.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-27/morning/azure-app-service-deploy-web-apps-without-managing-servers-cheatsheet.pdf

---

*PDF: [azure-app-service-deploy-web-apps-without-managing-servers-cheatsheet.pdf](azure-app-service-deploy-web-apps-without-managing-servers-cheatsheet.pdf)*
