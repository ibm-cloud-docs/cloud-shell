---

copyright:
  years: 2020, 2025
lastupdated: "2025-04-11"

keywords: HA for Cloud Shell, DR for cloud shell, high availability for cloud shell, disaster recovery for cloud shell, failover for cloud shell

subcollection: cloud-shell

---

{{site.data.keyword.attribute-definition-list}}

# Understanding high availability and disaster recovery for {{site.data.keyword.cloud-shell_short}}
{: #ha-dr}

As an {{site.data.keyword.cloud}} platform service, {{site.data.keyword.cloud-shell_full}} follows the practices that are described in [How {{site.data.keyword.cloud_notm}} prepares for disaster recovery](/docs/resiliency?topic=resiliency-ha-redundancy). One exception is that {{site.data.keyword.cloud-shell_notm}} is regionally available rather than globally available. Because {{site.data.keyword.cloud-shell_short}} is region-dependent, automated global failover isn't supported. Always maintain a backup of your data outside of {{site.data.keyword.cloud-shell_short}}.
{: shortdesc}

{{site.data.keyword.cloud-shell_notm}} is available in the Dallas (`us-south`) and Frankfurt (`eu-de`) regions, and each location has three different data centers for redundancy. The data for each location is kept in the data centers near that location. If all the data centers in a location or region fail, {{site.data.keyword.cloud-shell_notm}} becomes unavailable in that location or region. If this issue happens, you can change to another location or region as described in [Changing locations](/docs/cloud-shell?topic=cloud-shell-shell-ui#change-location).

For more information, see [How {{site.data.keyword.cloud_notm}} ensures high availability and redundancy](/docs/resiliency?topic=resiliency-ha-redundancy).

## Backing up your data
{: #data-backup}

Your {{site.data.keyword.cloud-shell_short}} workspace storage is temporary, and it is not to be used as the primary storage location for your files. Don't store business-critical or sensitive data in your workspace, and create a backup of your files outside of {{site.data.keyword.cloud-shell_notm}}. You're responsible for your data, and your backup can help you recover in case an outage or data loss occurs for any reason. For more information about how to transfer files to create a backup, see [Transferring multiple files](/docs/cloud-shell?topic=cloud-shell-files#transfer-many-files).

## What to do if a region is not available
{: #data-unavailable}

If a region is not available, {{site.data.keyword.cloud-shell_short}} indicates that the current region or location is not available. You must manually restore the files and data from a previous backup before you can access them.  


To select an available region and manually restore your data and files, complete these steps:

1. In {{site.data.keyword.cloud-shell_short}}, find the current location in the {{site.data.keyword.cloud-shell_short}} menu bar, and click **Change**.
2. Select the location that you want to switch to, and click **OK**. For more information, see [Changing locations](/docs/cloud-shell?topic=cloud-shell-shell-ui#change-location).
3. Upload the previously backed-up files and data into the new region or location. For more information, see [Uploading files](/docs/cloud-shell?topic=cloud-shell-files#upload-file).
