# osTicket Helpdesk Lab (Debian 12)

## Overview
This project documents the deployment of **osTicket**, an open-source ticketing system, on **Debian 12 (Bookworm)** as part of a personal home lab. The goal of this lab is to simulate a real-world IT helpdesk environment and demonstrate skills relevant to desktop support, NOC, and junior system administration roles.

This repository represents **Phase 1** of a multi-phase lab build. The system is currently deployed as a standalone service and will later be integrated with Active Directory for centralized authentication.

---

## Objectives
- Deploy a functional helpdesk ticketing system on Linux
- Configure and secure a LAMP-style stack
- Practice structured troubleshooting and log analysis
- Document decisions, issues, and resolutions
- Build a realistic, resume-ready home lab project

---

## Environment
- **OS:** Debian GNU/Linux 12 (Bookworm)
- **Platform:** VirtualBox
- **Web Server:** Apache 2
- **Database:** MariaDB
- **PHP:** PHP 8.2
- **Application:** osTicket v1.18.x

---

## Features (Phase 1)
- Web-based user ticket submission portal
- Agent and admin dashboard
- Department and help topic configuration
- Ticket creation, assignment, response, and closure
- Local database backend (MariaDB)

---

## Architecture
- Single Debian VM
- Apache serving osTicket via PHP
- MariaDB running locally on the same host
- Standalone deployment (no directory services yet)

A network diagram and architecture overview will be added in future updates.

---

## Installation Summary
High-level installation steps:
1. Installed Debian 12 (Bookworm) with minimal configuration
2. Installed Apache, PHP, MariaDB, and required PHP extensions
3. Secured MariaDB using built-in hardening tools
4. Created a dedicated database and user for osTicket
5. Deployed osTicket to Apache web root
6. Completed web-based installer
7. Performed post-install cleanup and permission hardening

Detailed step-by-step instructions are documented in `docs/installation.md`.

---

## Troubleshooting Highlights
During deployment, several real-world issues were encountered and resolved, including:
- PHP extension compatibility issues
- Missing IMAP dependency
- HTTP 500 Internal Server Errors
- Database authentication failures
- File permission and ownership issues

These problems were diagnosed using system logs (Apache error logs, PHP module checks) and resolved methodically. Full details are documented in `docs/troubleshooting.md`.

---

## Validation
The deployment was validated by:
- Logging into the admin and agent dashboards
- Creating test tickets from the user portal
- Responding to and closing tickets as an agent
- Verifying service stability and configuration persistence

---

## Future Plans (Phase 2)
Planned enhancements include:
- Active Directory / LDAP integration
- Centralized user authentication
- Role-based access using domain groups
- Email (SMTP) integration for ticket notifications
- HTTPS configuration (TLS)
- Backup and recovery considerations

Future work will be documented as additional phases in this repository.

---

## Author
Created as part of a personal home lab project focused on IT support and infrastructure fundamentals.
