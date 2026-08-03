# Morning Post -- 2026-08-03

**Topic:** Cloud & DevOps Tips

---

Every cloud beginner has stared at AWS S3 and wondered where all their files actually go...
(with real examples you can use right now)

1. S3 Bucket
 ↳ What: A giant, unlimited storage folder in the cloud with a globally unique name.
 ↳ Command/Tool: aws s3 mb s3://my-first-bucket-12345
 Use Case: When your boss asks you to store 10,000 user profile pictures safely.

2. Uploading Files
 ↳ What: Moving a local file from your laptop up into your S3 bucket.
 ↳ Command/Tool: aws s3 cp photo.png s3://my-first-bucket-12345/
 Use Case: When you need to back up yesterday's database export before leaving work.

3. Public vs Private Access
 ↳ What: Controlling whether the whole world can view your file or just your app.
 ↳ Command/Tool: AWS Console -> Bucket -> Permissions -> Block public access
 Use Case: When you want to host a company logo so anyone on the web can see it.

4. S3 Lifecycle Policies
 ↳ What: Rules that automatically move old files to cheaper storage to save money.
 ↳ Command/Tool: AWS S3 Management Console -> Lifecycle rule creation
 Use Case: When the finance team complains about your cloud bill for storing logs from 2021.

5. Static Website Hosting
 ↳ What: Turning a simple S3 folder into a live website without managing servers.
 ↳ Command/Tool: aws s3 website s3://my-first-bucket-12345/ --index-document index.html
 Use Case: When you built a quick portfolio page and want to show it to friends.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always double-check your bucket permissions before uploading sensitive data.
 ↳ Avoid naming buckets with predictable names since S3 bucket names must be globally unique.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #AWSS3 #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-03/morning/aws-s3-explained-store-and-access-files-in-the-cloud-cheatsheet.pdf

---

*PDF: [aws-s3-explained-store-and-access-files-in-the-cloud-cheatsheet.pdf](aws-s3-explained-store-and-access-files-in-the-cloud-cheatsheet.pdf)*
