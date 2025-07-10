# 🚀 Linux Networking & Utility Commands

## 🌐 Networking Commands

| Command | Description |
|--------|-------------|
| `ping <website>` | Check if the connection to a website or IP is working. |
| `netstat` | View network connections and status. |
| `ss` | Newer alternative to `netstat` for displaying socket connections. |
| `ifconfig` | Display Ethernet interface details (deprecated, use `ip`). |
| `ip address show` | Show IP addresses and network interfaces. |
| `iwconfig` | Display wireless network interface details. |
| `traceroute <website>` | Show the path packets take to reach the destination. |
| `tracepath <website>` | Similar to `traceroute`, shows the IP path (no reply means buffering). |
| `mtr <website>` | Combines `ping` and `traceroute` for real-time path tracing. |
| `nslookup <website>` | Look up DNS records like IP addresses. |
| `dig <website>` | Query DNS servers for domain-related info (A, MX, etc.). |
| `whois <website>` | Get detailed domain registration and ownership info. |
| `arp` | View MAC address mappings (used in local networks). |
| `ifplugstatus` | Check if a network cable is plugged into a network interface. |

---

## 🛠️ Regularly Used Commands

| Command | Description |
|--------|-------------|
| `curl <API_URL>` | Make HTTP requests (commonly used to interact with APIs). |
| `curl <API_URL> \| jq` | Pretty-print JSON API responses using `jq`. |
| `wget <URL>` | Download files or webpages from the internet. |
| `sudo iptables -L` | List current firewall rules applied to the system. |
| `watch <command>` | Continuously run a command every few seconds (real-time updates). |
| `nmap -v <website>` | Scan a website or IP for open ports and services. |
| `route` | View the system's routing table (deprecated, use `ip route`). |

---

> 🧠 **Tip**: Use `man <command>` to learn more about any Linux command directly in the terminal.
