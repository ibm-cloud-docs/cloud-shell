---

copyright:
  years: 2020, 2022
lastupdated: "2022-12-14"

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

## Current ingress IP ranges
{: #current-ranges}

Tables 1 - 3 list the current ingress IP ranges. On 20 January 2023, the IP address list will change. For more information on the new ranges, see [New ingress IP ranges](#new-ranges).

So that existing access is maintained, you must add the new IP ranges to your allowlists as soon as possible. You can remove the old IP ranges from the allowlists after the 20 January 2023.
{: note}

### {{site.data.keyword.cloud-shell_short}} ingress IP ranges for us-south (Dallas)
{: #dallas-ip-range}

Data center location | Subnet
-- | --
| Dallas 10 | 169.60.247.192/28 |
| Dallas 10 | 169.60.247.224/28 |
| Dallas 10 | 169.60.247.240/28 |
| Dallas 12 | 169.61.132.64/28 |
| Dallas 12 | 169.61.132.96/28 |
| Dallas 12 | 169.61.132.112/28 |
| Dallas 13 | 169.61.41.64/28 |
| Dallas 13 | 169.61.41.80/28 |
| Dallas 13 | 169.61.41.96/28 |
| Dallas 13 | 169.61.41.112/28 |
{: caption="Table 1. Cloud Shell ingress IP ranges for us-south (Dallas)" caption-side="bottom"}

### {{site.data.keyword.cloud-shell_short}} ingress IP ranges for eu-de (Frankfurt)
{: #frankfurt-ip-range}

Data center location | Subnet
-- | --
| Frankfurt 2 | 159.122.96.216/29 |
| Frankfurt 2 | 169.50.53.0/28 |
| Frankfurt 4 | 161.156.77.128/27 |
| Frankfurt 4 | 161.156.157.192/27 |
| Frankfurt 4 | 161.156.157.224/27 |
| Frankfurt 5 | 149.81.73.160/27 |
{: caption="Table 2. Cloud Shell ingress IP ranges for eu-de (Frankfurt)" caption-side="bottom"}

### {{site.data.keyword.cloud-shell_short}} ingress IP ranges for jp-tok (Tokyo)
{: #tokyo-ip-range}

Data center location | Subnet
-- | --
| Tokyo 2 | 161.202.235.192/27 |
| Tokyo 4 | 128.168.68.192/27 |
| Tokyo 5 | 165.192.70.32/27 |
{: caption="Table 3. Cloud Shell ingress IP ranges for jp-tok (Tokyo)" caption-side="bottom"}


## New ingress IP ranges
{: #new-ranges}

On 20 January 2023, the Cloud Shell ingress IPs for all regions (Dallas, Frankfurt, and Tokyo) will change. Tables 4 - 6 show the new IP ranges for each region.

So that existing access is maintained, you must add the new IP ranges to your allowlists as soon as possible. You can remove the old IP ranges from the allowlists after the 20 January 2023.
{: note}

### New {{site.data.keyword.cloud-shell_short}} ingress IP ranges for us-south (Dallas)
{: #dallas-ip-new-range}

Data center location | Subnet
-- | --
| Dallas 10 | 169.46.9.208/28 |
| Dallas 12 | 169.48.197.32/28 |
| Dallas 13 |	67.228.112.80/28 |
{: caption="Table 4. New Cloud Shell ingress IP ranges for us-south (Dallas)" caption-side="bottom"}

### New {{site.data.keyword.cloud-shell_short}} ingress IP ranges for eu-de (Frankfurt)
{: #frankfurt-ip-new-range}

Data center location | Subnet
-- | --
| Frankfurt 2 | 159.122.93.208/28 |
| Frankfurt 4 | 161.156.184.160/28 |
| Frankfurt 5 | 149.81.65.224/28 |
{: caption="Table 5. New Cloud Shell ingress IP ranges for eu-de (Frankfurt)" caption-side="bottom"}

### New {{site.data.keyword.cloud-shell_short}} ingress IP ranges for jp-tok (Tokyo)
{: #tokyo-ip-new-range}

Data center location | Subnet
-- | --
| Tokyo 2 | 169.56.48.176/28 |
| Tokyo 4 | 128.168.66.240/28 |
| Tokyo 5 | 165.192.108.208/28 |
{: caption="Table 6. New Cloud Shell ingress IP ranges for jp-tok (Tokyo)" caption-side="bottom"}
