---

copyright:
  years: 2020
lastupdated: "2020-01-21"

keywords: IBM Cloud Shell, frequently asked questions, faq, cloud shell type, cloud shell bash

subcollection: cloud-shell

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}


# FAQs for {{site.data.keyword.cloud-shell_notm}}
{: #faqs}

FAQs for {{site.data.keyword.cloud-shell_full}} include questions about {{site.data.keyword.cloud-shell_short}} sessions and its included tools and plug-ins. To find all FAQs for {{site.data.keyword.cloud}}, see our [FAQ library](https://{DomainName}/docs/faqs).
{: shortdesc}

## What type of shell is {{site.data.keyword.cloud-shell_short}}?
{: #what-shell-type}
{: faq}

{{site.data.keyword.cloud-shell_notm}} is an x86-64 Ubuntu Linux&trade; bash shell.

## What tools and plug-ins are included in {{site.data.keyword.cloud-shell_short}}?
{: #what-tools}
{: faq}

{{site.data.keyword.cloud-shell_notm}} includes all available {{site.data.keyword.cloud_notm}} CLI plug-ins and dozens of tools, packages, and runtimes. For the full list, see [Installed plug-ins and tools](/docs/cloud-shell?topic=cloud-shell-plugins-tools).

## How long can I use {{site.data.keyword.cloud-shell_short}}?
{: #what-usage-length}
{: faq}

You can use {{site.data.keyword.cloud-shell_short}} for up to 4 hours continuously or up to 30 hours within a single week. If you reach this limit, all {{site.data.keyword.cloud-shell_short}} sessions are closed, and any data in your workspace is deleted. If you reach your weekly limit, you can access {{site.data.keyword.cloud-shell_short}} only in 5-minute increments until the week resets.

## How can I audit {{site.data.keyword.cloud-shell_short}} usage?
{: #how-audit-logs}
{: faq}

{{site.data.keyword.cloud-shell_short}} generates {{site.data.keyword.at_full_notm}} events for your sessions and commands. You can analyze these events by using the {{site.data.keyword.at_short}} service. For more information, see [Activity Tracker events for {{site.data.keyword.cloud-shell_notm}}](/docs/cloud-shell?topic=cloud-shell-at_events).

## How can I delete my data in {{site.data.keyword.cloud-shell_short}}?
{: #how-delete-data}
{: faq}

Your data in {{site.data.keyword.cloud-shell_short}} is automatically deleted when {{site.data.keyword.cloud-shell_short}} is closed after inactivity or reaching the usage limits.

## How can I edit files in {{site.data.keyword.cloud-shell_short}}?
{: #how-edit-files}
{: faq}

{{site.data.keyword.cloud-shell_short}} includes two text editors, Vim (`vim`) and Nano (`nano`). You can use either of these editors to work with files in {{site.data.keyword.cloud-shell_short}}.

## How can I customize my {{site.data.keyword.cloud-shell_short}}?
{: #how-customize-shell}
{: faq}

As with any bash shell, you can modify the `.bashrc` file in your home directory to run commands or scripts every time a session starts. For example, you might set command aliases or environment variables that you often use. Because your home directory space is temporary, you need to edit the `.bashrc` file each time {{site.data.keyword.cloud-shell_short}} restarts.

Be careful when you edit these values because you can introduce errors that cause your sessions to not start. Don't change the `CLOUDSHELL`, `BLUEMIX_HOME`, `ACCOUNT_ID`, and `SESSION_NAME` environment variables, because they're required for your {{site.data.keyword.cloud-shell_short}} environment to work.

## How can I switch accounts in {{site.data.keyword.cloud-shell_short}}?
{: #faq-switch-accounts}
{: faq}

To switch the default account for all sessions, close {{site.data.keyword.cloud-shell_short}}, switch the account in the {{site.data.keyword.cloud_notm}} console menu bar, and then reopen {{site.data.keyword.cloud-shell_short}}.

