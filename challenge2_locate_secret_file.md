# Purpose: Locate a file with "secret" in its name using grep.

# Commands Used:

ls /home/ctf_user | grep "secret"

find /path/to/directory -type f | grep "secret"

find /home/ctf_user -type f -name "*secret*"

# Explanation:
The first command lists files in the specified directory and filters for those containing "secret".

The second command finds all files recursively and filters for those containing "secret".

The third command searches recursively for files that contain the term "secret" in their names within the specified directory.

# Result:
CTF{grep_is_your_friend}
