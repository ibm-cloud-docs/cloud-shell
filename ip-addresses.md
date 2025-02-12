---

copyright:
  years: 2020, 2025
lastupdated: "2025-02-12"

keywords: IBM Cloud Shell, cloudshell, CloudShell, cloud shell, cloud shell service, cloud shell ip addresses, cloud shell allowlist, cloud shell blocklist

subcollection: cloud-shell

---

{{site.data.keyword.attribute-definition-list}}

# {{site.data.keyword.cloud-shell_notm}} session IP ranges
{: #cs-ip-ranges}

If you want to restrict access to {{site.data.keyword.cloud-shell_full}} from your service, you can allowlist specific IP addresses or ranges of IP addresses on your deployment.
{: shortdesc}

If you use an allowlist or blocklist to control connections in your environment, you can use the following IP information to allowlist access to {{site.data.keyword.cloud-shell_short}}. Ensure that you allowlist all of the subnet ranges for the entire region where your deployments are.

You can configure the allowed and blocked IP list in your target service's IP list settings for traffic that is going to or coming from {{site.data.keyword.cloud-shell_short}}.

You can use a {{site.data.keyword.cloud-shell_short}} session as a terminal to use SSH to log in to your [VSI](/docs/virtual-servers?topic=virtual-servers-about-virtual-servers). For example, if you use [IBM Security Group](/docs/security-groups?topic=security-groups-about-ibm-security-groups) to protect your VSI, you need to know the IP address range of {{site.data.keyword.cloud-shell_short}} in a particular region.

{{site.data.keyword.cloud-shell_short}} does not have privileged access to {{site.data.keyword.cloud_notm}} resources. It has the same access as the locally installed {{site.data.keyword.cloud_notm}} CLI or the {{site.data.keyword.cloud_notm}} console.
{: note}


## Current ingress IP ranges
{: #current-ranges}

Tables 1 - 3 list the IP ranges for each region.


### {{site.data.keyword.cloud-shell_short}} ingress IP ranges for Dallas (us-south)
{: #dallas-ip-range}

Data center location | Subnet
-- | --
| Dallas 10 | 169.46.9.208/28 \n 169.46.97.32/27 \n 10.177.94.192/26 |
| Dallas 12 | 169.48.197.32/28 \n 169.48.231.32/27 \n 10.185.217.192/26 |
| Dallas 13 |	67.228.112.80/28 \n 67.228.231.192/27 \n 10.37.169.128/26 |
{: caption="Cloud Shell ingress IP ranges for Dallas (us-south) caption-side="bottom"}

### {{site.data.keyword.cloud-shell_short}} ingress IP ranges for Frankfurt (eu-de)
{: #frankfurt-ip-range}

Data center location | Subnet
-- | --
| Frankfurt 2 | 169.50.22.224/27 \n 10.134.69.192/26 |
| Frankfurt 4 | 161.156.184.160/28 \n 161.156.185.160/27 \n 10.240.247.0/26 |
| Frankfurt 5 | 149.81.65.224/28 \n 149.81.112.128/27 \n 10.123.216.64/26 |
{: caption="Cloud Shell ingress IP ranges for Frankfurt (eu-de)" caption-side="bottom"}
