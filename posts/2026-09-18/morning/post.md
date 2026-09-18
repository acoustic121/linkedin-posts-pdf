# Morning Post -- 2026-09-18

**Topic:** Cloud & DevOps Tips

---

Every developer has built a Docker image that accidentally bloated to over 1GB...
(with real examples you can use right now)

1. Naming Build Stages
 ↳ What: Giving a temporary name to your compile stage so you can copy files from it later.
 ↳ Command/Tool: FROM node:18 AS builder
 Use Case: When you need heavy SDKs to build your application but don't want them in production.

2. Selective Copying
 ↳ What: Extracting only compiled binaries or dist folders into a fresh, clean container image.
 ↳ Command/Tool: COPY --from=builder /app/dist ./dist
 Use Case: When your app is compiled and you want to leave raw source code and build tools behind.

3. Lightweight Runtime Images
 ↳ What: Using tiny operating system bases like Alpine or Distroless for the final running container.
 ↳ Command/Tool: FROM node:18-alpine
 Use Case: When your cloud server disk space is tight and you want ultra-fast deployment speeds.

4. Production Dependency Filtering
 ↳ What: Installing only runtime packages while leaving behind heavy testing and linting tools.
 ↳ Command/Tool: npm ci --only=production
 Use Case: When security tools flag vulnerability alerts in dev tools you do not even use live.

5. Checking Image Footprint
 ↳ What: Comparing final container sizes in your terminal to see how much space you saved.
 ↳ Command/Tool: docker images
 Use Case: When your team lead asks how much smaller your newly optimized container actually is.

6. Cleaning Builder Cache
 ↳ What: Clearing out accumulated temporary layer data created during multi-stage image builds.
 ↳ Command/Tool: docker builder prune -f
 Use Case: When your laptop throws a low disk space warning after running builds all afternoon.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start simple by splitting your Dockerfile into just two stages: builder and runner.
 ↳ Avoid copying whole project directories into your final runtime stage by mistake.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Docker #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-18/morning/docker-multi-stage-builds-shrink-your-image-size-by-90-cheatsheet.pdf

---

*PDF: [docker-multi-stage-builds-shrink-your-image-size-by-90-cheatsheet.pdf](docker-multi-stage-builds-shrink-your-image-size-by-90-cheatsheet.pdf)*
