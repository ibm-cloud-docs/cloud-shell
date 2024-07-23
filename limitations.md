---

copyright:
  years: 2020, 2024
lastupdated: "2024-03-28"

keywords: Cloud Shell limitations, Cloud Shell known issues

subcollection: cloud-shell

---

{{site.data.keyword.attribute-definition-list}}

# Known issues and limitations
{: #issues-limitations}

{{site.data.keyword.cloud-shell_full}} includes the following known issues and limitations that might impact your experience.
{: shortdesc}

## Known issues
{: #known-issues}

* Your {{site.data.keyword.cloud-shell_short}} workspace includes 500 MB of temporary storage. If you use all of your storage space, your connection to {{site.data.keyword.cloud-shell_short}} is lost. To access {{site.data.keyword.cloud-shell_short}}, you must restart it, which removes all of your files.
* Adding files outside of your `/home/<user-name>` home directory can cause {{site.data.keyword.cloud-shell_short}} to close, particularly if the files are large.
* You can mount (or mount by using a volume switch) your home directory or subdirectories of your home directory to your Docker container. If you mount to another location, an error results. 

## Limitations
{: #limitations}

* {{site.data.keyword.cloud-shell_notm}} runs in the Dallas (`us-south`) and Frankfurt (`eu-de`) regions only. You can access resources in any region.
* Usage is limited to 50 hours of weekly use. For more information, see [Tracking your usage](/docs/cloud-shell?topic=cloud-shell-shell-ui#usage-limit).
* {{site.data.keyword.cloud-shell_notm}} does not support [trusted profiles](/docs/account?topic=account-create-trusted-profile&interface=ui). If you start {{site.data.keyword.cloud-shell_notm}} and see an `Internal Error`, ensure that you're not using the [IAM Trusted profiles](/iam/trusted-profiles){: external} feature to log in to your {{site.data.keyword.cloud_notm}} account.
