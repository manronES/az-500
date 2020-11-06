# 4.1. Configure security for storage

## Configure access control for storage accounts

## Configure key management for storage accounts

## Configure Azure AD authentication for Azure Storage

## Configure Azure AD Domain Services authentication for Azure Files

## Create and manage Shared Access Signatures (SAS)

## Create a shared access policy for a blob or blob container

## Configure Storage Service Encryption

Azure Storage Service Encryption (SSE) for data at rest helps you protect your data to meet your organizational security and compliance commitments. With this feature, the Azure storage platform automatically encrypts your data with 256-bit Advanced Encryption Standard (AES) encryption before persisting it to disk and decrypts the data during retrieval. This handling of encryption, encryption at rest, decryption, and key management in Storage Service Encryption is transparent to applications using the services - you don't need to add any code or turn on any features.

You can use Microsoft-managed encryption keys with SSE, or you can use your own encryption keys by selecting the option in the Azure portal.

SSE automatically encrypts data in:

* All Azure Storage services including Azure Managed Disks, Azure Blob storage, Azure Files, Azure Queue storage, and Azure Table storage
* Both performance tiers (Standard and Premium)
* Both deployment models (Resource Manager and classic)

For your organization, SSE means that whenever they are using services that support storage service encryption, their data is encrypted on the physical medium of storage. In the highly unlikely event that access to the physical disk is obtained, data will be unreadable since it has been encrypted as written to the physical disk.
