# Research: Types of Cloud Storage

## Comparison of Cloud Storage Types

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Stores data in fixed-size blocks that can be accessed separately. | Operating systems, virtual machine disks, and databases. | AWS EBS |
| File Storage | Stores data in files organized into folders and directories. | Shared files, documents, and team folders. | AWS EFS |
| Object Storage | Stores data as objects with unique identifiers and metadata in a flat structure. | Photos, videos, backups, and other unstructured data. | AWS S3 |

## Why Object Storage Is Best for User-Uploaded Images

Object Storage is the best choice for the client's photo-sharing application because it can store large amounts of images and other unstructured data. It can also scale as more users upload photos. Since the images are stored separately from the web server container, they can remain available even when the application container is restarted or replaced.
