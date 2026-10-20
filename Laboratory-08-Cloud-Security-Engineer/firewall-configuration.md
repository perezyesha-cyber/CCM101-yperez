# 🛡️ FIREWALL CONFIGURATION REPORT

---

## 01 · 🔐 ALLOW SSH ACCESS

> **Security Rule:** Allow remote administration.

```bash
sudo ufw allow ssh
```

This command allows SSH connections through port 22 so administrators can remotely manage the server.

---

## 02 · 🧱 CONFIGURE THE DEFAULT DENY POLICY

> **Security Rule:** Block incoming traffic by default.

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

These commands block incoming traffic unless explicitly allowed and permit outgoing traffic from the server.

---

## 03 · 🌐 ALLOW PORT 8080

> **Security Rule:** Allow the required web application traffic.

```bash
sudo ufw allow 8080/tcp
```

This command allows incoming TCP traffic through port 8080 for the Nginx web application.

---

## 04 · ⚠️ SECURITY REMINDER

If I ran `sudo ufw enable` before `sudo ufw allow ssh`, incoming SSH connections could be blocked by the default deny policy, potentially preventing remote administration.

---

**CCM101 · CLOUD COMPUTING**  
Laboratory 08 — The Cloud Security Engineer
