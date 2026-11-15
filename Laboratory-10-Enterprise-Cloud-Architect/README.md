# Laboratory 10 – The Enterprise Cloud Architect

## Mission Overview

This project is the final laboratory activity for CCM101 – Cloud Computing. It focuses on designing, deploying, securing, and managing a private cloud infrastructure using Ubuntu Server, Docker, and Docker Compose.

Our group developed an infrastructure that includes several services for database management, source code hosting, password management, DNS filtering, and reverse proxy configuration.

## Objectives

- Design a cloud infrastructure architecture.
- Deploy multiple services using Docker Compose.
- Use persistent volumes to store application data.
- Apply security configurations to protect the server.
- Create an automation script for maintenance tasks.
- Prepare documentation for deployment and system maintenance.

## Project Components

| Component | Description |
|---|---|
| PostgreSQL | Database management |
| Gitea | Self-hosted Git repository management |
| Vaultwarden | Password management |
| Pi-hole | DNS filtering and internal DNS resolution |
| Nginx | Reverse proxy and HTTPS configuration |
| Docker Compose | Container and service management |

## Project Files

| File | Description |
|---|---|
| `README.md` | Project overview and description |
| `architecture-diagram.png` | Visual representation of the infrastructure |
| `docker-compose.yml` | Configuration for the application services |
| `automation-script.sh` | Script for automated maintenance tasks |
| `operational-manual.md` | Instructions for operating and maintaining the system |
| `final-reflection.md` | Reflection on the learning experience |

## Security and Automation

Our project incorporates security and automation concepts through firewall configuration, controlled service access, persistent storage, and a Bash automation script.

The automation script is designed to back up PostgreSQL databases, remove old backup files, generate SSL/TLS certificates, and reload Nginx. A scheduled Cron job is intended to execute the script automatically.

## Learning Outcomes

This activity helped us apply concepts related to Linux administration, virtualization, containerization, networking, persistent storage, security, and automation.

## Conclusion

This project demonstrates how different cloud technologies can work together to provide a private cloud infrastructure. It also highlights the importance of teamwork, security, data protection, automation, and proper documentation in managing cloud services.
