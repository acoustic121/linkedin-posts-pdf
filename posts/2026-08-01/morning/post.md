# Morning Post -- 2026-08-01

**Topic:** Cloud & DevOps Tips

---

Every beginner has written a Dockerfile that took 10 minutes to build.
(with real examples you can use right now)

1. Use Official Base Images
 ↳ What: Start your Dockerfile with a trusted, pre-made image instead of building an operating system from scratch.
 ↳ Command/Tool: FROM node:18-alpine
 Use Case: When your boss asks you to containerize the new web app before the afternoon demo.

2. Order Your Instructions Wisely
 ↳ What: Place commands that change less often at the top so Docker can reuse its saved cache.
 ↳ Command/Tool: COPY package.json . && RUN npm install
 Use Case: When you want your code builds to finish in seconds instead of coffee-break lengths.

3. Clean Up Package Caches
 ↳ What: Delete temporary installation files in the same step you create them to keep your image size tiny.
 ↳ Command/Tool: RUN apt-get update && apt-get install -y curl && rm -rf /var/lib/apt/lists/*
 Use Case: When your container image is so huge that uploading it to the cloud takes forever.

4. Set a Working Directory
 ↳ What: Create and move into a specific folder inside your container so your files don't scatter everywhere.
 ↳ Command/Tool: WORKDIR /app
 Use Case: When you are copying project files and want them neatly organized in one place.

5. Run as a Non-Root User
 ↳ What: Switch away from the super-admin user so hackers cannot easily take over your host machine.
 ↳ Command/Tool: USER node
 Use Case: When security scans fail because your app is running with dangerous root permissions.

6. Use .dockerignore Files
 ↳ What: Tell Docker which local folders and files to ignore so they never get copied into your image.
 ↳ Command/Tool: echo "node_modules" > .dockerignore
 Use Case: When your local node_modules folder accidentally gets copied and bloats your build.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Keep your Dockerfiles simple and read them from top to bottom like a recipe.
 ↳ Avoid putting your database passwords directly inside the Dockerfile text.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Docker #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-01/morning/dockerfile-best-practices-for-beginners-cheatsheet.pdf

---

*PDF: [dockerfile-best-practices-for-beginners-cheatsheet.pdf](dockerfile-best-practices-for-beginners-cheatsheet.pdf)*
