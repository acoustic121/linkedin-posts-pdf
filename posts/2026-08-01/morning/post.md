# Morning Post -- 2026-08-01

**Topic:** Cloud & DevOps Tips

---

Ever typed the same 5 Linux commands every single morning before starting work?
(with real examples you can use right now)

1. Variables
 -> What: A box where you can store text or numbers to use later in your script.
 -> Command/Tool: MY_NAME="Aman"
 Use Case: When you need to save a server IP address so you don't have to type it ten times.

2. Echo
 -> What: A simple way to print messages to your screen so you know what your script is doing.
 -> Command/Tool: echo "Starting backup..."
 Use Case: When your script takes a minute to run and you want to see a friendly progress message.

3. If-Else Statements
 -> What: Making decisions in your code based on whether something is true or false.
 -> Command/Tool: if [ -d "logs" ]; then echo "Found"; fi
 Use Case: When your script needs to check if a folder exists before trying to save files inside it.

4. For Loops
 -> What: Telling your computer to repeat the same task over a list of items automatically.
 -> Command/Tool: for server in web1 web2; do ping -c 1 $server; done
 Use Case: When your boss asks you to check if all 50 company servers are online right now.

5. Comments
 -> What: Leaving notes in your code with a hashtag so you remember what it does next month.
 -> Command/Tool: # This line deletes old temp files
 Use Case: When you write a script today and look at it again six months later with zero memory.

6. Exit Status
 -> What: A secret number your computer gives back to tell you if your command worked or failed.
 -> Command/Tool: echo $?
 Use Case: When you want to stop your script immediately if a file download fails halfway through.

The best way to learn? Open a terminal and try these yourself.

My advice:
 -> Start small by turning a two-step manual task into a single script.
 -> Always double-check your file paths before running a delete command.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #BashScripting #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-auto-poster/raw/main/posts/2026-08-01/morning/post.pdf

---

*PDF: [post.pdf](post.pdf)*
