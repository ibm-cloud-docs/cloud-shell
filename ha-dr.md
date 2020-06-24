---

copyright:
  years: 2020
lastupdated: "2020-06-23"

keywords: HA for Cloud Shell, DR for cloud shell, high availability for cloud shell, disaster recovery for cloud shell, failover for cloud shell

subcollection: cloud-shell

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}

# Understanding high availability and disaster recovery for {{site.data.keyword.cloud-shell_short}}
{: #ha-dr}

As an {{site.data.keyword.cloud}} platform service, {{site.data.keyword.cloud-shell_full}} follows the practices that are described in [How IBM Cloud ensures high availability and disaster recovery](/docs/overview?topic=overview-zero-downtime), with the exception that {{site.data.keyword.cloud-shell_notm}} is regionally available rather than globally available. Because {{site.data.keyword.cloud-shell_short}} is region-dependent, automated global failover isn't supported. You should always maintain a backup of your data outside of {{site.data.keyword.cloud-shell_short}}.
{: shortdesc}

{{site.data.keyword.cloud-shell_notm}} is available in the Dallas (`us-south`), Frankfurt (`eu-de`), and Tokyo (`jp-tok`) regions, and each location has three different data centers for redundancy. The data for each location is kept in the data centers near that location. If all the data centers in a location fail, {{site.data.keyword.cloud-shell_notm}} becomes unavailable in that location. When this happens, you can change to another location as described in [Changing locations](/docs/cloud-shell?topic=cloud-shell-shell-ui#change-location).

## Backing up your data
{: #data-backup}

Your {{site.data.keyword.cloud-shell_short}} workspace storage is temporary, and it's not intended to be used as the primary storage location for your files. Don't store business-critical or sensitive data in your workspace, and create a backup of your files outside of {{site.data.keyword.cloud-shell_notm}}. You're responsible for your data, and your backup can help you recover in case an outage or data loss occurs for any reason. For more information about how to transfer files to create a backup, see [Transferring multiple files](/docs/cloud-shell?topic=cloud-shell-files#transfer-many-files).
