# ALX System Engineering & DevOps

A project covering shell scripting, Linux administration, networking, web infrastructure, and production operations.

## Overview

This project includes 27 tasks that build practical DevOps and systems engineering skills on Ubuntu. The project begins with Bash shell fundamentals—navigation, permissions, redirection, and variable expansion—then advances through control flow, process management, and regular expressions. The Middle task folders introduce networking concepts, Puppet configuration management, SSH hardening, and Nginx web server deployment. The final section covers load balancing, HTTPS/SSL, firewall rules, MySQL administration, Python REST API clients, web stack debugging, monitoring, and incident postmortems.

Each task folder is a self-contained directory of numbered tasks with checker-compatible scripts, configuration files, and Puppet manifests. Tasks increase in complexity from single-line shell commands to multi-server deployments, API integrations, and production troubleshooting scenarios.

## Skills covered


- Navigate and administer a Linux filesystem using Bash, permissions, and I/O redirection
- Write shell scripts with loops, conditionals, argument parsing, and signal handling
- Apply regular expressions for pattern matching and text extraction
- Describe the OSI model, TCP/UDP, IP/MAC addressing, and common network diagnostics
- Manage server configuration with Puppet manifests and idempotent resource declarations
- Set up SSH key-based authentication and harden remote access with Puppet
- Deploy and tune Nginx web servers, custom error pages, redirects, and domain setup
- Debug broken web stacks across multiple debugging project iterations
- Set up HAProxy load balancers and custom HTTP response headers
- Terminate SSL with HAProxy and redirect HTTP traffic to HTTPS
- Write the full request lifecycle from browser input to server response
- Set up UFW firewall rules and port forwarding for secure network access
- Manage MySQL databases, users, and replication concepts
- Consume and export REST API data with Python (`requests`, CSV, JSON)
- Build advanced API scripts for pagination, recursion, and subscriber counting
- Monitor web infrastructure and write structured incident postmortems
- Tune application server limits with Puppet for production readiness

## Tech Stack

| Category | Technologies |
|----------|-------------|
| Shell | Bash, POSIX utilities, `awk`, `sed` |
| Languages | Bash, Ruby (regex tasks), Python 3 |
| Configuration | Puppet, Nginx, HAProxy |
| Networking | TCP/UDP, DNS, SSH, SSL/TLS, UFW |
| Databases | MySQL |
| Web/API | Nginx, REST APIs, JSON, CSV export |
| Debugging | `strace`, `curl`, system logs, process inspection |
| Runtime | Ubuntu 20.04+ |

## Project Structure

| Module | Directory | Focus |
|--------|-----------|-------|
| 0x00 | `0x00-shell_basics` | Navigation, listing, moving, and manipulating files |
| 0x01 | `0x01-shell_permissions` | Users, groups, ownership, and permission bits |
| 0x02 | `0x02-shell_redirections` | Pipes, redirects, `find`, and filters |
| 0x03 | `0x03-shell_variables_expansions` | Variables, aliases, arithmetic, and expansions |
| 0x04 | `0x04-loops_conditions_and_parsing` | `for`/`while`/`until`, FizzBuzz, RSA key handling |
| 0x05 | `0x05-processes_and_signals` | Process listing, background jobs, signals, PID management |
| 0x06 | `0x06-regular_expressions` | Ruby regex patterns, repetition tokens, phone numbers |
| 0x07 | `0x07-networking_basics` | OSI model, network types, MAC/IP, TCP/UDP, `ping` |
| 0x08 | `0x08-networking_basics_2` | Localhost IP, attached IPs, listening ports |
| 0x0A | `0x0A-configuration_management` | Puppet: files, packages, and command execution |
| 0x0B | `0x0B-ssh` | SSH keys, config, and Puppet-managed SSH hardening |
| 0x0C | `0x0C-web_server` | Nginx install, file transfer, redirects, 404 pages, Puppet |
| 0x0D | `0x0D-web_stack_debugging_0` | First web stack debugging: serving pages |
| 0x0E | `0x0E-web_stack_debugging_1` | Nginx port debugging and short fixes |
| 0x0F | `0x0F-load_balancer` | HAProxy install, custom headers, Puppet automation |
| 0x10 | `0x10-https_ssl` | SSL termination, HTTPS redirects, HAProxy SSL |
| 0x11 | `0x11-what_happens_when_your_type_google_com_in_your_browser_and_press_enter` | Browser request lifecycle blog, diagram, contribution |
| 0x12 | `0x12-web_stack_debugging_2` | User context, Nginx process ownership, quick fixes |
| 0x13 | `0x13-firewall` | UFW rules and port forwarding |
| 0x14 | `0x14-mysql` | MySQL setup, users, databases, and queries |
| 0x15 | `0x15-api` | Python API data gathering, CSV/JSON export |
| 0x16 | `0x16-api_advanced` | Subscribers, top posts, recursive Reddit queries, counting |
| 0x17 | `0x17-web_stack_debugging_3` | `strace`-assisted debugging with Puppet |
| 0x18 | `0x18-webstack_monitoring` | Web stack monitoring setup and practices |
| 0x19 | `0x19-postmortem` | Incident postmortem documentation |
| 0x1A | `0x1A-application_server` | Application server configuration |
| 0x1B | `0x1B-web_stack_debugging_4` | Advanced limits tuning with Puppet |

## Key Implementations

- **Shell scripting foundation (`0x00`–`0x05`)** — Progressive Bash tasks from basic navigation through process signals, including FizzBuzz, superstitious number loops, and background process control
- **Puppet configuration management (`0x0A`, `0x0B`, `0x0C`, `0x0F`, `0x1B`)** — Idempotent manifests for file creation, package installation, Nginx deployment, HAProxy headers, SSH config, and resource limits
- **Web server deployment (`0x0C`, `0x0F`, `0x10`)** — Nginx installation, custom 404 pages, domain setup, HAProxy load balancing, SSL termination, and HTTP-to-HTTPS redirection
- **Web stack debugging series (`0x0D`–`0x0E`, `0x12`, `0x17`, `0x1B`)** — Iterative troubleshooting of broken stacks: port conflicts, user permissions, process ownership, and `strace` analysis
- **Networking and security (`0x07`–`0x08`, `0x13`)** — OSI/TCP-UDP fundamentals, localhost diagnostics, UFW firewall rules, and port forwarding
- **MySQL administration (`0x14`)** — Database and user management scripts for server-side data storage
- **Python API clients (`0x15`–`0x16`)** — REST data collection with `requests`, CSV/JSON export, pagination, recursive fetching, and aggregate counting
- **Production operations (`0x18`–`0x19`)** — Monitoring practices and structured postmortem writing for real-world incident response

## Getting Started

### Prerequisites

- Ubuntu 20.04+ (local or VM)
- Git
- Bash 4+
- Python 3.8+ (modules `0x15` onward)
- Puppet (modules `0x0A` onward)
- Nginx, HAProxy, MySQL as required per module

### Setup

```bash
git clone <repository-url>
cd alx-system_engineering-devops
chmod +x **/*.sh 2>/dev/null
```

### Running Tasks

Shell tasks are executed directly or via checker `main` files:

```bash
./0x00-shell_basics/0-current_working_directory
./0x05-processes_and_signals/0-what-is-my-pid
```

Puppet manifests are applied with the Puppet agent:

```bash
puppet apply 0x0A-configuration_management/0-create_a_file.pp
puppet apply 0x0C-web_server/7-puppet_install_nginx_web_server.pp
```

Python API tasks:

```bash
python3 0x15-api/0-gather_data_from_an_API.py
python3 0x16-api_advanced/0-main.py
python3 0x16-api_advanced/100-count.py
```

MySQL scripts (module `0x14`) are run against a local MySQL instance with appropriate credentials.

## Curriculum Context

This project covers DevOps and systems engineering in the ALX Software Engineering curriculum. It runs alongside or after foundational Git and shell exposure from the pre-course and zero-day task folders, and complements the C programming project with the operational skills needed to deploy and maintain web applications in production.

| Previous | Next |
|----------|------|
| `alx-zero_day` — Git workflow and first C/Bash tasks on Ubuntu | `alx-higher_level_programming` — Python, SQL, and JavaScript web development |

Related work:

- `alx-low_level_programming` — C fundamentals that underpin systems programming concepts used in debugging and server administration
- `alx-backend` / `alx-backend-python` — Backend specialization building on the web stack and API skills developed here
