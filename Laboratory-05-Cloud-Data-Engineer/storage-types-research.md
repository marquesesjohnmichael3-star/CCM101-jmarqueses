# Cloud Storage Comparison

| Storage Type | How It Stores Data | Common Use | Example |
|---|---|---|---|
| Block Storage | Divides information into blocks that can be managed independently. | Databases, virtual machines, and system disks. | Amazon EBS |
| File Storage | Keeps information as files arranged within directories. | Shared documents and files used by several systems. | Amazon EFS |
| Object Storage | Keeps files as objects together with metadata and an identifier. | Photos, videos, backups, and other unstructured information. | Amazon S3 |

## Why Object Storage?

For a photo-sharing application, object storage is practical because photos are unstructured files that can be stored as individual objects. Buckets also provide a simple way to organize large collections of uploaded files.
