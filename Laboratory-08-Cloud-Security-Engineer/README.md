# 🛡️ LABORATORY 08 — THE CLOUD SECURITY ENGINEER

## 01 · 🎯 MISSION OVERVIEW

This laboratory activity is about securing a server using the UFW firewall. I deployed an Nginx web server using Docker and configured firewall rules to allow SSH and web application traffic. I also tested the application and checked the firewall status to make sure the configuration was working.

---

## 02 · 📌 OBJECTIVES

- Understand the Principle of Least Privilege and attack surface.
- Learn how to configure a firewall using UFW.
- Apply the Default Deny policy to block incoming traffic by default.
- Allow SSH access and web application traffic on port 8080.
- Test the web application using the `curl` command.
- Document the commands and results in GitHub.

---

## 03 · 💻 COMMANDS EXECUTED

### 🔹 Deploy and Test the Web Application

```bash
docker run -d --name secure-web-app -p 8080:80 nginx
curl http://localhost:8080
```

### 🔹 Configure the Firewall

```bash
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
```

### 🔹 Allow the Application Port

```bash
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl http://localhost:8080
```

---

## 04 · 🧠 SKILLS LEARNED

- Deploying a web server using Docker.
- Testing a web application using `curl`.
- Configuring and checking UFW firewall rules.
- Managing network ports to improve server security.
- Understanding the importance of SSH access and the Default Deny policy.
- Writing technical documentation using Markdown.

---
<p align="center">
  <b>CCM101 · CLOUD COMPUTING</b><br/>
  <sub>Laboratory 08 — The Cloud Security Engineer</sub>
</p>



