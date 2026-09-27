# Mission Reflection

Object storage is useful for a photo-sharing system because images are unstructured data and can be stored as separate objects. Instead of treating every photo like part of a traditional disk, the storage system can organize the files inside buckets. This makes the storage model appropriate for applications that may receive a large number of images.

Docker simplified the MinIO setup because the server could be launched from an existing container image. The required ports, administrator account, and console settings could be supplied when the container was started. This avoided having to perform a long manual installation process.

A bucket is a logical container for objects in an object storage system. In this activity, `client-photos` was used as the bucket where the sample uploaded file was stored.

Enterprise systems can protect stored information by maintaining backups and copies of data in different locations. Replication can also help maintain another copy when a storage server or physical machine becomes unavailable. These approaches can help reduce the effect of hardware failures.

Working through this activity increased my familiarity with the Linux command line. I was able to use commands for Docker, create directories and files, check running containers, and manage a Git repository. The activity also helped me understand how a containerized service can provide a practical cloud storage environment.
