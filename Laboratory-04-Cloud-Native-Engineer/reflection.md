# Mission Reflection

This laboratory helped me understand the difference between Virtual Machines and Docker containers. A Virtual Machine usually takes more time to start because it needs its own operating system. It also uses more computer resources. A Docker container can start faster because it shares the host operating system. In this activity, I was able to run an Nginx container in just a few commands.

The port mapping `-p 8080:80` is needed so I can access the web server from the host. The Nginx web server is running inside the container on port 80. Port 8080 is the port that I used from the host. Because of this mapping, I was able to use `curl http://localhost:8080` and see the Nginx welcome page.

When I use the `docker rm` command, the stopped container is removed from Docker. The container and its data are deleted. However, the Nginx image can still stay in Docker and can be used again to create another container.

Containerization can help developers and IT operations teams work better together. Developers can create an application and put it inside a container with its needed files. The operations team can then run the same container in another environment. This can make the deployment process easier and more consistent.

My GitHub portfolio is also improving because I am adding my laboratory activities and documenting what I learned. In this activity, I learned about Docker, Nginx, containers, and basic Docker commands. I also learned how to organize screenshots and Markdown files in GitHub. This activity gave me more experience in cloud computing and helped me understand how containers are used.
