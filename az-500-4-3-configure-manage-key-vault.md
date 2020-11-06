# 4.3. Configure and manage Key Vault

We've seen that the encryption services all use keys to encrypt and decrypt data, so how do we ensure that the keys themselves are secure? You may also have passwords, connection strings, or other sensitive pieces of information that you need to securely store.

Azure Key Vault is a cloud service that works as a secure secrets store. Key Vault allows you to create multiple secure containers, called vaults. These vaults are backed by hardware security modules (HSMs). Vaults help reduce the chances of accidental loss of security information by centralizing the storage of application secrets. Key Vaults also control and log the access to anything stored in them. Azure Key Vault can handle requesting and renewing Transport Layer Security (TLS) certificates, providing the features required for a robust certificate lifecycle management solution. Key Vault is designed to support any type of secret. These secrets could be passwords, database credentials, API keys, and certificates.

Because Azure AD identities can be granted access to use Azure Key Vault secrets, applications using managed identities for Azure services can automatically and seamlessly acquire the secrets they need.

Your organization can use Key Vault for the storage of all their sensitive application information, including the TLS certificates they use to secure communication between systems.

To create the vault:

```bash
az keyvault create \
    --resource-group learn-7036049c-ce86-4875-baeb-b6a6b8684285 \
    --location centralus \
    --name <your-unique-vault-name>
```

To add a secret:

```bash
az keyvault secret set \
    --name SecretPassword \
    --value reindeer_flotilla \
    --vault-name <your-unique-vault-name>
```

## Manage access to Key Vault

## Manage permissions to secrets, certificates, and keys

## Configure RBAC usage in Azure Key Vault

## Manage certificates

## Manage secrets

## Configure key rotation

## Backup and restore of Key Vault items
