
---

# CHECKPOINT 6 — Mission Reflection


This laboratory activity helped me understand how object storage works and how it can be used to manage a large amount of data. Object storage is better suited for storing millions of photos because it is designed to store files as objects and can handle large amounts of unstructured data. Unlike traditional block storage, object storage can organize files using metadata and buckets, making it easier to manage and access many photos. It is also scalable, which means more storage can be added as the amount of data increases.

Using Docker made the deployment of the MinIO storage server easier because I did not need to manually install and configure all the required components. I was able to use a Docker image and commands to create and run the MinIO container. Docker also made it easier to check if the server was running properly using commands such as `docker ps`.

A bucket is a container used in object storage to organize and store objects or files. In MinIO, a bucket can contain different files such as photos, documents, and other data. It provides a simple way to organize and manage stored objects.

Large enterprise companies can protect their object storage data from physical server crashes by using data replication, redundancy, backups, and multiple storage servers. These methods help ensure that copies of the data remain available even if one physical server fails.

Overall, this activity increased my confidence in navigating the Linux command line. I learned how to use Docker commands, pull an image, create and run a container, and check its status. Although I encountered some errors while deploying MinIO, solving them helped me better understand Docker, Linux commands, and cloud object storage.
