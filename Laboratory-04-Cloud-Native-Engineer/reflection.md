# Mission Reflection

This laboratory helped me understand how containers can make application deployment faster and easier compared to traditional Virtual Machines. When using a Virtual Machine, an operating system needs to be installed and configured before applications can be deployed, which can take more time and system resources. In comparison, a Docker container can start in seconds because it uses the existing host operating system and only contains the application and its required dependencies.

The port mapping `-p 8080:80` is necessary because the Nginx web server is running inside the container on port 80, while port 8080 is used to access it from the host environment. This mapping allows a request sent to `localhost:8080` to reach the Nginx server running inside the container. During the activity, I used `curl http://localhost:8080` to verify that the Nginx welcome page was working.

When the `docker rm` command is used, the specified stopped container is permanently removed. This means the container itself and its writable container data are deleted. However, the Docker image used to create the container can still remain on the system.

Containerization can also improve collaboration between software developers and IT operations teams. Developers can package an application with its dependencies, while operations teams can run the same container in different environments. This supports a more consistent workflow and can make application deployment easier.

My GitHub portfolio is also evolving as I continue adding organized laboratory activities. Laboratory 04 adds practical experience with Docker, Nginx, containers, and technical documentation. By keeping the files and screenshots organized in the repository, I am building a portfolio that shows my progress and the cloud computing skills I have learned.
