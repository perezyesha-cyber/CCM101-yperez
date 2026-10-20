# 🛡️ MISSION REFLECTION
---

In this laboratory activity, I learned the importance of securing a server using a firewall. A host-based firewall helps protect a server by controlling incoming and outgoing network traffic. Even if someone gets past the network security, the firewall can still block connections that are not allowed. This gives the server an additional layer of protection against possible attacks.

I also learned that managing open network ports is important because attackers can use them to access a server. If too many ports are open, the server becomes more exposed to security risks. In this activity, I allowed port 22 for SSH and port 8080 for the Nginx web application. I learned that only the necessary ports should be allowed to reduce the server's attack surface.

In a real company, leaving MySQL port 3306 open to the public internet is dangerous because attackers might try to access the database and steal important information. They could also change or delete data if they successfully gain access. That is why database access should only be allowed for trusted servers and authorized users.

This activity changed my understanding of server security because I realized that setting up a server is easy, but protecting it requires more attention. Even a small mistake in the firewall configuration can create security problems. I also learned that SSH should be allowed before enabling the firewall to avoid blocking remote access.

Having eight completed missions in my GitHub portfolio makes me feel that I have learned more about cloud computing. Each activity helped me practice different commands and understand how cloud services work. This mission also improved my knowledge of Linux, Docker, and firewall configuration. Overall, I learned that securing a server is an important responsibility and should always be part of deploying an application.

---

**CCM101 · CLOUD COMPUTING**  
Laboratory 08 — The Cloud Security Engineer
