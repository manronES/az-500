# 3.2. Monitor security by using Azure Security Center

Azure Security Center is a free service, now enabled by default for all Azure subscriptions, that is tightly integrated with other Azure application level services, such as Azure Application Gateway and Azure Web Application Firewall. By analyzing logs from these services, Security Center can report on known vulnerabilities in real time, recommend responses to mitigate them, and even be configured to automatically execute playbooks in response to attacks.

## Evaluate vulnerability scans from Azure Security Center

## Configure Just in Time VM access by using Azure Security Center

Requirements:

* Azure Defender for servers.
* VM should be deployed by Azure Resource Manager, not classic deployment models.
* JIT does not support VMs protected by Azure Firewalls controlled by Azure Firewall Manager.

From Security Center, you can enable and configure the JIT VM access.

1. Open the Azure Defender dashboard and from the advanced protection area, select Just-in-time VM access. The **Just-in-time VM access** page opens with your VMs grouped into the following tabs:

* **Configured** - VMs that have been already been configured to support just-in-time VM access. For each VM, the configured tab shows:
  * the number of approved JIT requests in the last seven days
  * the last access date and time
  * the connection details configured
  * the last user
* **Not configured** - VMs without JIT enabled, but that can support JIT. We recommend that you enable JIT for these VMs.
* **Unsupported** - VMs without JIT enabled and which don't support the feature. Your VM might be in this tab for the following reasons:
  * Missing network security group (NSG) - JIT requires an NSG to be configured
  * Classic VM - JIT supports VMs that are deployed through Azure Resource Manager, not 'classic deployment'. Learn more about classic vs Azure Resource Manager deployment models.
  * Other - Your VM might be in this tab if the JIT solution is disabled in the security policy of the subscription or the resource group.

2. From the **Not configured** tab, mark the VMs to protect with JIT and select **Enable JIT on VMs**.

The JIT VM access page opens listing the ports that Security Center recommends protecting:

* 22 - SSH
* 3389 - RDP
* 5985 - WinRM
* 5986 - WinRM

To accept the default settings, select Save.

3. To customize the JIT options:

* Add custom ports with the Add button.
* Modify one of the default ports, by selecting it from the list.

For each port (custom and default) the Add port configuration pane offers the following options:

* Protocol- The protocol that is allowed on this port when a request is approved
* Allowed source IPs- The IP ranges that are allowed on this port when a request is approved
* Maximum request time- The maximum time window during which a specific port can be opened

  a. Set the port security to your needs.

  b. Select OK.

4. Select Save.

https://docs.microsoft.com/en-us/azure/security-center/just-in-time-explained

## Configure centralized policy management by using Azure Security Center

## Configure compliance policies and evaluate for compliance by using Azure Security Center
