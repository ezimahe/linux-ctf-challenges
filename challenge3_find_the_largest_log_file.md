# Purpose: Finding the largetst log file in a directory

Commands Used:

`cd /path/to/your/directory`

`find . -type f -exec du -h {} + | sort -rh | head -n 1`

Other:

`find /path/to/directory -type f -name "*part_of_filename*" -exec du -h {} + | sort -rh | head -n 1` #Search specific name

`find /path/to/directory -type f -name "*.log" -exec du -h {} + | sort -rh | head -n 1` #Search specific extension


# Explanation:
`find . -type f`: This finds all files in the current directory and its subdirectories.

`-exec du -h {}`: This executes the du command on each file found, which returns the disk usage in human-readable format.

`sort -rh`: This sorts the output in reverse order based on size.

`head -n 1`: This outputs only the largest file.

# Result:
`CTF{size_matters_in_linux}`
