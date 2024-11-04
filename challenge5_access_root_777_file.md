
# Purpose: Access file owned by root with 777 permission

Commands run:

`echo "CTF{permission_granted}" | sudo tee /root/everyone_can_access_me`

`sudo chmod 777 /root/everyone_can_access_me`

`sudo find / -type f -perm 777 2>/dev/null`

# Explanation:
Looking for the file with `-rwxrwxrwx` (777) permission. `find` command is used with the `-perm` flag to look for files with specific permissions. 

The `2>/dev/null` part helps suppress any "Permission Denied" errors in directories where you don’t have access.

The command `sudo tee /root/everyone_can_access_me` creates a file named `everyone_can_access_me` in the `/root` directory with elevated permissions (due to `sudo`). 

sudo: Runs the command as the superuser, which is required to write to the /root directory (normally restricted).

`tee` This command reads from standard input (or accepts content piped to it) and writes it to the specified file. If no input is provided, it doesn’t actually add content, but the file is still created if it doesn’t exist.

# Results:
`/root/everyone_can_access_me`

`CTF{permission_granted}`


