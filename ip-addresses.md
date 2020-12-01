---

copyright:
  years: 2020
lastupdated: "2020-11-30"

keywords: IBM Cloud Shell, cloud shell, cloud shell service, cloud shell ip addresses, cloud shell allowlist, cloud shell blocklist

subcollection: cloud-shell

---

{:external: target="_blank" .external}
{:shortdesc: .shortdesc}
{:table: .aria-labeledby="caption"}
{:tip: .tip}
{:important: .important}
{:note: .note}

# {{site.data.keyword.cloud-shell_notm}} session IP ranges
{: #cs-ip-ranges}

If you want to restrict access to {{site.data.keyword.cloud-shell_full}} from your service, you can allowlist specific IP addresses or ranges of IP addresses on your deployment.
{: shortdesc}

If you use an allowlist or blocklist to control connections in your environment, you can use the following IP information to allowlist access to {{site.data.keyword.cloud-shell_short}}. Ensure that you allowlist all of the subnet ranges for the entire region that your deployments reside in.

You can configure the allowed and blocked IP list in your target service's IP list settings for traffic that is going to or coming from {{site.data.keyword.cloud-shell_short}}.

You can use a {{site.data.keyword.cloud-shell_short}} session as a terminal to use SSH to log in to your [VSI](/docs/virtual-servers?topic=virtual-servers-about-virtual-servers). For example, if you use [IBM Security Group](/docs/security-groups?topic=security-groups-about-ibm-security-groups) to protect your VSI, you need to know the IP address range of {{site.data.keyword.cloud-shell_short}} in a particular region.

{{site.data.keyword.cloud-shell_short}} does not have privileged access to {{site.data.keyword.cloud_notm}} resources. It has the same access as the locally installed {{site.data.keyword.cloud_notm}} CLI or the {{site.data.keyword.cloud_notm}} console.
{: note}

## {{site.data.keyword.cloud-shell_short}} ingress IP ranges for us-south (Dallas)
{: #dallas-ip-range}

Data center location | Subnet
-- | --
Dallas 10 | 52.116.182.136/29
Dallas 10 | 169.48.166.216/29
Dallas 12 | 169.47.98.88/29
Dallas 12 | 169.48.219.200/29
Dallas 13 | 169.48.65.216/29
Dallas 13 | 169.48.74.80/29

## {{site.data.keyword.cloud-shell_short}} ingress IP ranges for eu-de (Frankfurt)
{: #frankfurt-ip-range}

Data center location | Subnet
-- | --
Frankfurt 2 | 158.177.215.136/29
Frankfurt 2 | 159.122.98.240/29
Frankfurt 4 | 161.156.129.96/29
Frankfurt 4 | 161.156.150.248/29
Frankfurt 5 | 149.81.102.232/29
Frankfurt 5 | 149.81.114.64/29

## {{site.data.keyword.cloud-shell_short}} ingress IP ranges for jp-tok (Tokyo)
{: #tokyo-ip-range}

Data center location | Subnet
-- | --
Tokyo 2 | 161.202.133.88/29
Tokyo 2 | 161.202.236.208/29
Tokyo 4 | 128.168.75.240/29
Tokyo 4 | 128.168.94.24/29
Tokyo 5 | 165.192.82.240/29
Tokyo 5 | 165.192.92.208/29
