# Purpose: Finding the process running on port 8080, and retrieve the flag from its command

Command used:

`sudo lsof -i :8080`

`sudo netstat -tuln | grep <port_number>`

`sudo ss -tuln | grep <port_number>`

`nc localhost 8080` or `curl http://localhost:8080` reveals the flag (information served on port 8080)


# Explanation:
Command 1 outputs details about any process using port 8080, including: Process ID, User running the process and Command name

In command 2 & 3 `-tuln` displays TCP (`-t`) and UDP (`-u`) listening (`-l`) ports without resolving names (`-n`).

`nc` (Netcat) is listening on port `8080`. Command 4 simulates a basic HTTP request to localhost on port 8080. If `nc` is serving any text or flag data, curl should display it in the terminal.


# Result:
`ss` command outputs;
`tcp   LISTEN 0      1            0.0.0.0:8080      0.0.0.0:* `


`lsof` command outputs;
`COMMAND   PID     USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
nc      10403 ctf_user    3u  IPv4 131014      0t0  TCP *:http-alt (LISTEN)`


`nc localhost 8080` command outputs;

`HTTP/1.1 200 OK`

`CTF{port_explorer}`


`curl http://localhost:8080` command outputs;

`CTF{port_explorer}`
