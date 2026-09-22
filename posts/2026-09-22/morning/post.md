# Morning Post -- 2026-09-22

**Topic:** Cloud & DevOps Tips

---

Ever wondered why your Docker builds take 5 minutes for a tiny code change?
(with real examples you can use right now)

1. Layer Caching
 ↳ What: Docker skips rebuilding unchanged steps by saving previous build results as cached layers.
 ↳ Command/Tool: docker build -t my-app .
 Use Case: When you fix a single typo in your code and want an instant build.

2. Copying Dependencies First
 ↳ What: Moving package files before source code so Docker caches your heavy dependency downloads.
 ↳ Command/Tool: COPY package*.json ./
 Use Case: When npm install takes 5 minutes every single time you edit a file.

3. Combining RUN Commands
 ↳ What: Joining commands with && so temporary installation files do not get saved into layers.
 ↳ Command/Tool: RUN apt-get update && apt-get install -y curl
 Use Case: When you want to install tools and clean up temporary files in one step.

4. Using .dockerignore
 ↳ What: A text file that stops large local files from being sent to Docker during builds.
 ↳ Command/Tool: echo "node_modules" > .dockerignore
 Use Case: When your build is slow because it is sending gigabytes of local junk to Docker.

5. Multi-Stage Builds
 ↳ What: Using multiple FROM lines to drop build tools and keep only final app binaries.
 ↳ Command/Tool: FROM golang:1.21 AS builder
 Use Case: When your manager asks why a simple Go app image is 1GB instead of 20MB.

6. Slim Base Images
 ↳ What: Starting your Dockerfile with lightweight OS distributions instead of full heavy Linux versions.
 ↳ Command/Tool: FROM python:3.11-slim
 Use Case: When you need your app container to download fast during a 3am deployment fix.

7. Inspecting Image Layers
 ↳ What: Viewing every layer and its file size to see which command made your image huge.
 ↳ Command/Tool: docker history my-app:latest
 Use Case: When your build size suddenly explodes and you need to find out why.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Order your Dockerfile steps from least-changed (installing packages) to most-changed (copying source code).
 ↳ Never copy your whole directory before running your package manager install command.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Docker #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-22/morning/docker-image-layers-why-your-builds-are-slow-and-how-to-fix-cheatsheet.pdf

---

*PDF: [docker-image-layers-why-your-builds-are-slow-and-how-to-fix-cheatsheet.pdf](docker-image-layers-why-your-builds-are-slow-and-how-to-fix-cheatsheet.pdf)*
