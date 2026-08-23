# Morning Post -- 2026-08-23

**Topic:** Cloud & DevOps Tips

---

Ever destroyed a Docker container and panicked when your database disappeared?
(with real examples you can use right now)

1. Named Volumes
 ↳ What: A dedicated, safe storage space managed directly by Docker outside any container lifecycle.
 ↳ Command/Tool: docker volume create db_data
 Use Case: When you need a permanent home for database files before starting your backend.

2. Mounting Volumes to Containers
 ↳ What: Attaching your permanent volume to a specific folder inside a running container.
 ↳ Command/Tool: docker run -d -v db_data:/var/lib/mysql mysql:8.0
 Use Case: When you want your MySQL database data to stay safe even if the container crashes at 3am.

3. Bind Mounts (Local Directory Sync)
 ↳ What: Linking a folder on your laptop directly into a container for live updates.
 ↳ Command/Tool: docker run -v $(pwd)/src:/app/src -p 3000:3000 node:alpine
 Use Case: When your boss asks you to fix code bugs instantly without rebuilding the image.

4. Inspecting Volume Storage Path
 ↳ What: Finding out the exact physical location on your host machine where Docker stores data.
 ↳ Command/Tool: docker volume inspect db_data
 Use Case: When a senior engineer asks where your app's persistent files are physically stored.

5. Listing All Active Volumes
 ↳ What: Displaying every storage volume currently existing on your system.
 ↳ Command/Tool: docker volume ls
 Use Case: When you want to check if old project files are secretly hogging space.

6. Cleaning Unused Volumes
 ↳ What: Deleting all orphaned volumes that aren't attached to any container.
 ↳ Command/Tool: docker volume prune
 Use Case: When your laptop runs out of disk space and you need a quick spring cleaning.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always give your volumes custom names instead of relying on anonymous random hashes.
 ↳ Don't assume stopping or deleting a container automatically deletes its mounted volume.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Docker #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-23/morning/docker-volumes-explained-where-does-your-data-go-cheatsheet.pdf

---

*PDF: [docker-volumes-explained-where-does-your-data-go-cheatsheet.pdf](docker-volumes-explained-where-does-your-data-go-cheatsheet.pdf)*
