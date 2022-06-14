---

copyright:
  years: 2020, 2022
lastupdated: "2022-06-03"

keywords: Cloud Shell limitations, Cloud Shell known issues

subcollection: cloud-shell

---

{:shortdesc: .shortdesc}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:important: .important}
{:note: .note}

# Known issues and limitations
{: #issues-limitations}

{{site.data.keyword.cloud-shell_full}} includes the following known issues and limitations that might impact your experience.
{: shortdesc}

## Known issues
{: #known-issues}

* Your {{site.data.keyword.cloud-shell_short}} workspace includes 500 MB of temporary storage. If you use all of your storage space, your connection to {{site.data.keyword.cloud-shell_short}} is lost. To access {{site.data.keyword.cloud-shell_short}}, you must restart it, which removes all of your files.
* Adding files outside of your `/home/<user-name>` home directory can cause {{site.data.keyword.cloud-shell_short}} to close, particularly if the files are large.
* You can use the {{site.data.keyword.cloud_notm}} CLI {{site.data.keyword.dev_cli_short}} (`ibmcloud dev`) commands to work with cloud-based resources such as pipelines and toolchains. However, it can't be used to work locally, such as to build, test, or run apps.

## Limitations
{: #limitations}

* {{site.data.keyword.cloud-shell_notm}} runs in the Dallas (`us-south`), Frankfurt (`eu-de`), and Tokyo (`jp-tok`) regions only. You can access resources in any region.
* Usage is limited to 50 hours of weekly use. For more information, see [Tracking your usage](/docs/cloud-shell?topic=cloud-shell-shell-ui#usage-limit).
* {{site.data.keyword.cloud-shell_notm}} does not support [trusted profiles](/docs/account?topic=account-create-trusted-profile&interface=ui). If you launch {{site.data.keyword.cloud-shell_notm}} and see an `Internal Error`, ensure that you're not using the [IAM Trusted profiles](/iam/trusted-profiles){: external} feature to log in to your {{site.data.keyword.cloud_notm}} account.
