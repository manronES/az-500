# 4.2. Configure security for databases

## Enable database authentication

## Enable database auditing

## Configure Azure SQL Database Advanced Threat Protection

## Implement database encryption

Transparent data encryption (TDE) helps protect Azure SQL Database and Azure Data Warehouse against the threat of malicious activity. It performs real-time encryption and decryption of the database, associated backups, and transaction log files at rest without requiring changes to the application. By default, TDE is enabled for all newly deployed Azure SQL Databases.

TDE encrypts the storage of an entire database by using a symmetric key called the database encryption key. By default, Azure provides a unique encryption key per logical SQL Server and handles all the details. Bring-your-own-key is also supported with keys stored in Azure Key Vault.

Since TDE is enabled by default, your organization can be confident they have the proper protections in place for data stored in their databases.

## Implement Azure SQL Database Always Encrypted

For their on-premises Microsoft SQL Server databases, your organization has turned on the SQL Server Always Encrypted feature. Always Encrypted is designed to protect sensitive data, such as client personal information or financial data. This feature protects column data at rest and in transit by having the client application handle the encryption and decryption outside the SQL Server database through an installed driver. This allows your organization to minimize exposure of data as the database never works with unencrypted data. The Always Encrypted client driver performs the actual encryption and decryption processes, rewriting the T-SQL queries as necessary to encrypt data passed to the DB and decrypt the results, while keeping these operations transparent to the application.

>>> Just for on-premises databases?
