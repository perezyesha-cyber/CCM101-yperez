# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A two-tier architecture is an application design that separates the application and the database into two different tiers. In this laboratory, Nextcloud serves as the web application, while MariaDB stores the application's data.

## The Web/Application Tier

The web/application tier uses the Nextcloud container. It provides the user interface that users access through a web browser. It also handles HTTP requests and allows users to manage their files through the private cloud storage system.

## The Database Tier

The database tier uses the MariaDB container. It stores important application data, such as user account information and file metadata. It allows Nextcloud to save and retrieve the information it needs to work properly.

## Why Separate Them?

Separating the web application and database into two containers makes the system easier to manage, update, and troubleshoot. It also allows each container to operate independently and helps organize the application more efficiently. Docker Compose connects the containers so Nextcloud can communicate with MariaDB.
