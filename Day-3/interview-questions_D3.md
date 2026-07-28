# Day 3 Interview Questions & Answers
 
```
1. Difference between ps and top?
 
ps gives a one-time snapshot of running processes at that exact
moment. top gives a live, continuously updating view of processes
along with CPU and memory usage. In short — ps is a static picture,
top is a real-time dashboard.
```
 
```
2. How do you terminate a running process in Linux?
 
We use the kill command with the process ID, like kill 1234. This
sends a termination signal to the process asking it to stop
gracefully.
 
Follow-up — kill vs kill -9:
kill sends a polite termination signal (SIGTERM), giving the process
a chance to close cleanly and save its state. kill -9 sends SIGKILL,
which force-stops the process immediately, without any cleanup. We
use kill -9 only when a process is stuck and not responding to a
normal kill.
```
 
```
3. Purpose of jobs, bg, and fg?
 
jobs shows all background and suspended processes in the current
terminal session. bg resumes a paused process in the background so
we can continue using the terminal. fg brings a background process
back to the foreground when we need to interact with it directly.
We use these when running long tasks — like a backup script —
without blocking our terminal.
```
 
```
4. Difference between cp and mv? Real-world example.
 
cp copies a file, keeping the original in place — useful when we
back up a config file before editing, like cp config.yaml
config.yaml.bak. mv moves or renames a file, removing it from the
original location — useful when we move a deployment script into
the correct directory, like mv deploy.sh /opt/scripts/.
```
 
```
5. Find a file named config.yaml in current directory?
 
We use: find . -name config.yaml
Here, "." means search starting from the current directory, "-name"
specifies the exact filename we're looking for, and it searches
through all subdirectories recursively.
```
 
```
6. Purpose of ping? What does 100% packet loss mean?
 
ping checks if a remote host or server is reachable over the network
by sending small data packets and waiting for a reply. 100% packet
loss means none of our packets got a response — indicating the host
is down, unreachable, or blocked by a firewall.
```
 
```
7. What does ip addr show?
 
ip addr shows network interface details. Three key pieces of info:
1) IP address assigned to each interface, 2) whether the interface
is UP or DOWN, and 3) the MAC address of the network card.
```
 
```
8. What is curl used for? Production example.
 
curl is used to send HTTP requests directly from the terminal — to
test APIs, download files, or check if a server is responding. In
production, a DevOps engineer might use curl to health-check an API
endpoint after deployment, like curl -I https://myapp.com/health.
```
 
```
9. What does ss -tuln show? What is LISTEN state?
 
ss -tuln shows active network ports and sockets — t for TCP, u for
UDP, l for listening ports, and n shows numeric addresses instead of
resolving names. LISTEN state means the port is open and actively
waiting for incoming connections, like a web server ready to accept
traffic.
```
 
```
10. Purpose of dig? Why useful for DNS troubleshooting?
 
dig queries DNS servers to check how a domain name resolves to an IP
address. It's useful for troubleshooting because it shows the exact
DNS response, including which server answered and how long
resolution took — helping us confirm if a DNS issue is causing a
website outage.
```
 
```
Bonus Scenario: "Website is not opening" — troubleshooting order
 
I'd troubleshoot step-by-step, from basic connectivity to deeper
issues:
 
1. ping <domain> — check if the server is reachable at all.
2. dig <domain> — confirm DNS is resolving the domain correctly.
3. curl -I <domain> — check if the web server is actually responding
   with a valid HTTP status.
4. ss -tuln — verify if the web server's port (like 80 or 443) is
   open and listening.
 
This order makes sense because we move from network-level checks to
DNS, then to the application layer — isolating the issue quickly
instead of guessing.
```