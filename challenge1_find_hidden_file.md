# Purpose: Finding a hidden file in a directory.

Commands Used:
ls -a -l

find /path/to/directory -type f -name ".*"

# Explanation:
ls -a: Lists all files in a directory, including hidden ones.

ls -a -l: Lists all files in a directory, including hidden ones into a long list.

find /path/to/directory -type f -name ".*": Recursively finds hidden files across directories.


# Result:
CTF{hidden_files_revealed}
