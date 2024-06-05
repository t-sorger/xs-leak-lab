# XS-Leaks Lab (XSLL)
Welcome to XS-Leaks Lab (XSLL) – a hands-on project exploring Cross-site Leaks (XS-Leaks). This project aims to introduce you to the topic while providing an interactive experience with selected XS-Leaks scenarios. For a deeper dive into the project, continue reading this README, and don't forget to explore the report available in this repository.

## XSLL Structure
XSLL comprises two Docker containers:
- **Attacker**: This container is designed to simulate an attacker attempting to exploit vulnerabilities and leak information from the victim.
- **Victim**: The victim container represents the entity under attack, serving as a practical environment to understand and mitigate XS-Leak risks.

## Installation
To get started, follow these steps:

1. **Download or Clone Repository**

2. **Configure Hosts File**: Modify your system's hosts file (`/etc/hosts`) to include the following entries:
```
127.0.0.1 	attacker.local
127.0.0.1 	victim.local
```
Alternatively, adjust the scripts to use `localhost` or `127.0.0.1`.

## Docker Container
For implementation, we utilize the official [NGINX Docker image](https://hub.docker.com/_/nginx) to set up the web servers within Docker containers. To manage these containers, use the provided scripts:
- **Start Docker Containers**:
```Bash
./setup.sh
```

- **Stop Docker Containers**:
```Bash
./destroy.sh
```

## Access Web Servers
After starting the Docker containers, you can access the web servers from your browser:
- [Attacker](http://attacker.local:31415/)
- [Victim](http://victim.local:27182/)

Explore these links to interact with the simulated environments and delve deeper into XS-Leak vulnerabilities.

## Browser Version Used for Testing
All vulnerabilities in this lab were tested using the following browser version:
- Brave
- Version 1.66.118 Chromium: 125.0.6422.147 (Official Build) (arm64)
