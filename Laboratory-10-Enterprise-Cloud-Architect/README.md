# Laboratory 10 – The Enterprise Cloud Architect

## 1. Mission Overview

This project is the final laboratory activity for CCM101 – Cloud Computing. Its main goal is to design, deploy, secure, automate, and document a private cloud infrastructure using the knowledge gained from the previous laboratory activities.

For this mission, I developed a containerized infrastructure using Ubuntu Server, Docker, and Docker Compose. The infrastructure includes PostgreSQL, Gitea, Vaultwarden, Pi-hole, and Nginx. These services provide database management, source code hosting, password management, DNS filtering, and reverse proxy functionality.

The project also includes persistent storage, firewall configuration, an automation script, and an operational manual. These components are intended to help maintain application data, improve security, and simplify server maintenance.

## 2. Project Objectives

The objectives of this project are:

- Design a cloud infrastructure architecture and network topology.
- Configure an Ubuntu Server virtual machine.
- Deploy multiple services using Docker Compose.
- Connect application services to a PostgreSQL database.
- Configure persistent volumes for data storage.
- Use Nginx as a reverse proxy for the hosted services.
- Configure Pi-hole for DNS filtering and internal name resolution.
- Apply firewall rules to restrict unnecessary network access.
- Create a Bash script for database backups and maintenance tasks.
- Schedule automated operations using Cron.
- Document the deployment and maintenance procedures.

## 3. Infrastructure Architecture

The infrastructure runs on an Ubuntu Server virtual machine hosted by a physical computer through a hypervisor.

Docker Compose manages five primary services connected through a dedicated bridge network named `cloudnova-network`.

### Architecture Components

| Component | Function |
|---|---|
| Ubuntu Server | Hosts the Docker environment and cloud services. |
| Docker Engine | Runs the application containers. |
| Docker Compose | Defines and manages the services, networks, and volumes. |
| PostgreSQL | Provides database storage for the applications. |
| Gitea | Provides self-hosted Git repository management. |
| Vaultwarden | Provides password and secure information management. |
| Pi-hole | Provides DNS filtering and internal DNS resolution. |
| Nginx | Handles reverse proxy requests and HTTPS configuration. |
| UFW | Controls incoming network connections at the host level. |
| Bash Script | Performs database backup, backup cleanup, and certificate-related operations. |
| Cron | Schedules the automation script to run at a configured time. |

Refer to `architecture-diagram.png` for the visual representation of the infrastructure.

## 4. Docker Services

The `docker-compose.yml` file defines the following services.

### PostgreSQL

PostgreSQL is the database service used by Gitea and Vaultwarden. It stores application-related information and uses the `postgres_data` volume for persistent database storage.

### Gitea

Gitea is a self-hosted Git service that allows users to create repositories and manage source code. It connects to PostgreSQL through the internal Docker network.

Its application data is stored using the `gitea_data` volume.

### Vaultwarden

Vaultwarden provides a self-hosted password management service for authorized users. Its configuration disables public account registration by setting `SIGNUPS_ALLOWED=false`.

Its application data is stored using the `vaultwarden_data` volume.

### Pi-hole

Pi-hole provides DNS filtering and can be configured to resolve internal domain names for the hosted services.

Its configuration exposes DNS on ports 53/TCP and 53/UDP, while the web interface is mapped to host port 8081. Its data is stored using the `pihole_data` and `dnsmasq_data` volumes.

### Nginx

Nginx serves as the reverse proxy for the infrastructure. It is configured to listen on ports 80 and 443 and uses a custom configuration file named `nginx.conf`.

The certificate directory is mounted as read-only inside the container. The intended configuration allows services to be accessed through their assigned internal domain names.

## 5. Persistent Storage

The infrastructure defines five named Docker volumes:

- `postgres_data`
- `gitea_data`
- `vaultwarden_data`
- `pihole_data`
- `dnsmasq_data`

These volumes are intended to preserve important application data when containers are restarted or recreated.

Persistent volumes do not replace backups. Important data should also be backed up regularly and tested for successful recovery.

## 6. Network Configuration

All five services are connected to the `cloudnova-network` bridge network.

The Docker Compose configuration publishes the following host ports:

| Port | Protocol | Purpose |
|---|---|---|
| 53 | TCP | DNS service |
| 53 | UDP | DNS service |
| 80 | TCP | HTTP and reverse proxy access |
| 443 | TCP | HTTPS access |
| 8081 | TCP | Pi-hole web interface |

SSH must also be allowed through the host firewall for remote administration.

Only the ports required by the actual deployment should be accessible. Database ports should remain private and should not be published directly to the host unless there is a specific requirement.

## 7. Security Configuration

The infrastructure is designed to use UFW for host-level firewall protection.

The intended firewall policy follows these principles:

- Set the default incoming policy to deny.
- Allow SSH for remote administration.
- Allow only the application ports required for the deployment.
- Keep PostgreSQL accessible through the internal Docker network.
- Disable public Vaultwarden registration.
- Use HTTPS through Nginx.
- Restrict access to administrative interfaces.
- Avoid storing passwords or other sensitive credentials in public repositories.

The host firewall and Docker networking must be tested together because published Docker ports may affect how traffic is handled. Firewall rules alone should not be assumed to block all access to published container ports.

## 8. Automation and Backup

The project includes `automation-script.sh`, which is designed to perform several operational tasks.

Its intended functions are:

1. Create a backup directory if it does not exist.
2. Export PostgreSQL databases using `pg_dumpall`.
3. Save the database export as a timestamped SQL file.
4. Delete SQL backup files older than 30 days.
5. Generate a self-signed SSL/TLS certificate.
6. Reload the Nginx configuration.

The script is intended to run automatically through a Cron job.

Before relying on it, the administrator must verify that the script is executable, the target directory exists, the required containers are running, and the backup and certificate operations complete successfully.

The script also needs to be tested to ensure that certificate renewal does not interrupt HTTPS access and that database backups can be restored.

## 9. Project Files

| File | Description |
|---|---|
| `README.md` | Provides an overview of the infrastructure and its components. |
| `architecture-diagram.png` | Shows the planned infrastructure architecture. |
| `docker-compose.yml` | Defines the five services, their configuration, persistent volumes, and network. |
| `automation-script.sh` | Contains the automated database backup and maintenance operations. |
| `operational-manual.md` | Provides deployment, administration, and maintenance instructions. |
| `final-reflection.md` | Describes my learning experience throughout the course. |

## 10. Expected Outcomes

The project is intended to demonstrate the following capabilities:

- Deploy multiple containerized services using Docker Compose.
- Connect applications to a PostgreSQL database.
- Preserve application data using persistent volumes.
- Route application requests through Nginx.
- Configure internal DNS resolution using Pi-hole.
- Restrict unnecessary network access through firewall configuration.
- Automate database backup and maintenance operations.
- Document the infrastructure for future administration.

Each capability must be verified through actual deployment and testing.

## 11. Skills Learned

Through this activity, I applied my knowledge of Linux administration, virtualization, Docker, Docker Compose, networking, persistent storage, database management, firewall configuration, reverse proxies, Bash scripting, and technical documentation.

I also learned that a cloud infrastructure requires proper planning, security testing, backup verification, and regular maintenance.

## 12. Conclusion

Laboratory Activity 10 allowed me to combine different cloud computing technologies into one infrastructure project. By designing a multi-service environment and preparing its configuration and documentation, I gained a better understanding of how applications, databases, networks, and automation work together.

This project also taught me that building a cloud environment involves more than making applications run. Security, data protection, automation, and documentation are important parts of maintaining a reliable system.
