# Morning Post -- 2026-09-24

**Topic:** Cloud & DevOps Tips

---

Every developer has stared at a Docker container that crashes instantly and does not tell you why.
(with real examples you can use right now)

1. Check the exit clues
 ↳ What: See the numeric code that tells you if your app crashed or failed to start.
 ↳ Command/Tool: docker ps -a
 Use Case: When your app vanishes from the running list and you need to know if it even tried to start.

2. Read the final words
 ↳ What: Look at the error logs before the container gave up and died.
 ↳ Command/Tool: docker logs <container_id>
 Use Case: When your app crashes at 3am and you need to find the missing configuration file error.

3. Peek inside the box
 ↳ What: Open an interactive terminal inside the container to look around the file system.
 ↳ Command/Tool: docker run -it <image_name> sh
 Use Case: When you want to check if your code files actually made it inside the container.

4. Override the startup command
 ↳ What: Stop the app from auto-starting so you can troubleshoot it manually.
 ↳ Command/Tool: docker run -it --entrypoint sh <image_name>
 Use Case: When your default start script is broken and you need to test commands manually.

5. Inspect the blueprint
 ↳ What: View all the hidden settings, environment variables, and paths in your container setup.
 ↳ Command/Tool: docker inspect <container_id>
 Use Case: When you suspect you passed the wrong database password into your container.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always check the logs first before changing any code.
 ↳ Avoid guessing the error—let the container logs guide you.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Docker #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-24/morning/how-to-debug-a-docker-container-that-wont-start-cheatsheet.pdf

---

*PDF: [how-to-debug-a-docker-container-that-wont-start-cheatsheet.pdf](how-to-debug-a-docker-container-that-wont-start-cheatsheet.pdf)*
