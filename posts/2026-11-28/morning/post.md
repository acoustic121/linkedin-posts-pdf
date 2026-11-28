# Morning Post -- 2026-11-28

**Topic:** Cloud & DevOps Tips

---

You don't need to rent a whole virtual machine just to run a 10-second script.
(with real examples you can use right now)

1. HTTP Trigger
 ↳ What: A function that runs whenever someone visits a specific web URL.
 ↳ Command/Tool: func new --template "HTTP trigger" --name MyHttpFunction
 Use Case: When your front-end team needs a quick API to fetch today's date.

2. Timer Trigger
 ↳ What: A function that runs automatically on a schedule, like an alarm clock.
 ↳ Command/Tool: func new --template "Timer trigger" --name RunEveryMorning
 Use Case: When your boss asks you to clear out old temp files every night at 12 AM.

3. Blob Storage Trigger
 ↳ What: A function that wakes up whenever a new file is uploaded to your storage.
 ↳ Command/Tool: func new --template "Blob trigger" --name ProcessNewImages
 Use Case: When a user uploads a profile picture and you need to resize it instantly.

4. Cosmos DB Trigger
 ↳ What: A function that reacts instantly whenever data is added or updated in your database.
 ↳ Command/Tool: func new --template "Cosmos DB trigger" --name LogNewUsers
 Use Case: When you want to send a welcome email the second a new user registers.

5. Azure Functions Core Tools
 ↳ What: A local command-line tool to run and test your functions on your own laptop before deploying.
 ↳ Command/Tool: func start
 Use Case: When you want to test your code without spending a single penny on the cloud.

6. Deploying to Azure
 ↳ What: Moving your locally tested function up to the actual live Azure cloud.
 ↳ Command/Tool: func azure functionapp publish MyCoolUniqueAppName
 Use Case: When your code works perfectly on your machine and it's time to share it with the world.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with the local emulator first so you don't worry about cloud bills.
 ↳ Never store database passwords directly in your code; use App Settings instead.

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-28/morning/azure-functions-run-code-on-demand-without-a-server-cheatsheet.pdf

---

*PDF: [azure-functions-run-code-on-demand-without-a-server-cheatsheet.pdf](azure-functions-run-code-on-demand-without-a-server-cheatsheet.pdf)*
