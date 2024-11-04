# Linux CTF Challenges (Fully Documented)
Working through Linux Command Line Capture The Flag (CTF) lab on Microsoft Azure

# Challenge 1: The Hidden File

Objective: Find a hidden file in the ctf_challenges directory and read its contents.

Skills tested:

Understanding of hidden files in Linux
Using ls with appropriate flags
Reading file contents
Hint: In Linux, files that start with a dot (.) are considered hidden. How can you list all files, including hidden ones?

# Challenge 2: The Secret File

Objective: Locate a file with the word "secret" in its name anywhere in the /home/ctf_user directory.

Skills tested:

Recursive file searching
Using grep or find commands
Hint: The find command can search for files based on their names. How can you use it to search for a file containing "secret" in its name?

# Challenge 3: The Largest Log

Objective: Find the largest file in the /var/log directory and retrieve the flag from it.

Skills tested:

Navigating directory structures
Sorting and filtering files based on size
Reading file contents
Hint: The du command can help you find file sizes. How can you combine it with sort to find the largest file?

# Challenge 4: The User Detective

Objective: Identify the user with UID 1001 and find the flag in their home directory.

Skills tested:

Understanding user management in Linux
Reading the /etc/passwd file or using id command
Navigating to other users' home directories
Hint: The /etc/passwd file contains information about user accounts. How can you search for a specific UID in this file?

# Challenge 5: The Permissive File

Objective: Locate the file owned by root with permissions 777 and read its contents.

Skills tested:

Understanding Linux file permissions
Using find command with permission parameters
Reading file contents as a non-root user
Hint: The find command can also search for files based on their permissions. What does 777 mean in terms of file permissions?

# Challenge 6: The Hidden Service

Objective: Find the process running on port 8080 and retrieve the flag from its command.

Skills tested:

Using network-related commands (netstat, ss, or lsof)
Understanding process information
Reading process details
Hint: The netstat or ss command can show you which processes are listening on which ports. How can you use these to find a process on a specific port?

# Challenge 7: The Encoded Secret

Objective: Decode the base64 encoded flag in the 'encoded_flag.txt' file.

Skills tested:

Understanding of base64 encoding
Using command-line decoding tools
Hint: Linux has a built-in command for base64 decoding. How can you use it to decode the contents of a file?
