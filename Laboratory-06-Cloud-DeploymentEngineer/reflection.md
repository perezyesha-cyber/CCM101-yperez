# Mission 6 Reflection: The Cloud Deployment Engineer

This laboratory activity helped me understand how Docker Compose can make cloud deployment easier. Instead of starting each container manually, I used a YAML configuration file to define the Nextcloud application and MariaDB database. With one command, I was able to start both services together. This method saves time and helps reduce mistakes during deployment.

I also learned that YAML indentation is very important. If I use the wrong number of spaces or press Tab instead of using spaces, the configuration file may produce an error. Docker Compose might not understand the file correctly, so I need to check the format and indentation carefully before deploying the application.

Environment variables, such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER`, provide the settings needed by the containers. They help Nextcloud connect to the correct database using the required credentials. I also learned that `MYSQL_HOST=database` allows the application to find the database service through the Docker Compose network. However, passwords written directly in a Compose file are suitable only for this practice environment and should be handled more securely in real projects.

Deploying Nextcloud in a few minutes was a good learning experience for me. I was able to see how a private cloud storage application works with a separate database. I also learned how to check the container status and stop the services after completing the activity.

Since Mission 1, my understanding of cloud computing has improved. I have learned more about cloud infrastructure, containers, storage, and application deployment. This mission taught me that cloud engineers can use Infrastructure as Code to make deployment more organized, repeatable, and efficient. I believe these skills will help me in future cloud computing activities and IT projects.
