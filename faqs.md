---

copyright:
  years: 2020, 2025
lastupdated: "2025-03-19"

keywords: Cloud Shell frequently asked questions, Cloud Shell faq, cloud shell type, cloud shell bash

subcollection: cloud-shell

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQs for {{site.data.keyword.cloud-shell_notm}}
{: #faqs}

FAQs for {{site.data.keyword.cloud-shell_full}} include questions about {{site.data.keyword.cloud-shell_short}} sessions and its included tools and plug-ins. To find all FAQs for {{site.data.keyword.cloud}}, see the [FAQ library](/docs/faqs).
{: shortdesc}

## What type of shell does {{site.data.keyword.cloud-shell_short}} use?
{: #what-shell-type}
{: faq}

{{site.data.keyword.cloud-shell_notm}} uses a Red Hat&reg; Linux&reg; bash shell.

## What tools and plug-ins are included in {{site.data.keyword.cloud-shell_short}}?
{: #what-tools}
{: faq}
{: support}

{{site.data.keyword.cloud-shell_notm}} includes all available {{site.data.keyword.cloud_notm}} CLI plug-ins and dozens of tools, packages, and runtimes. For the full list, see [Installed plug-ins and tools](/docs/cloud-shell?topic=cloud-shell-plugins-tools).

## What browsers does {{site.data.keyword.cloud-shell_short}} support?
{: #what-browsers}
{: faq}
{: support}

To work in {{site.data.keyword.cloud-shell_short}}, you need to use one of the {{site.data.keyword.cloud_notm}} supported browsers. For more information, see [What are the {{site.data.keyword.cloud_notm}} prerequisites?](/docs/overview?topic=overview-prereqs-platform) If you use a browser that is not supported, you might see blank screens or other display problems when you use {{site.data.keyword.cloud-shell_short}}.

## How do I copy and paste text in {{site.data.keyword.cloud-shell_short}}?
{: #how-copy-paste}
{: faq}
{: support}

To copy text in {{site.data.keyword.cloud-shell_short}}, select the text that you want to copy, and then do one of the following actions:

* In your browser menu, click **Edit**, and then click **Copy** or **Paste**.
* For macOS, use the keyboard shortcuts Cmd+C and Cmd+V.
* For Linux&reg;, use Ctrl+Insert for copy and Shift+Insert for paste.
* For Windows&reg;, use Ctrl+Insert for copy and either Shift+Insert or Ctrl+Shift+V for paste.
* Select text and then right-click to use the menu, and select **Copy** or **Paste**.

Firefox and Internet Explorer might not support clipboard permissions properly.

## How long can I use {{site.data.keyword.cloud-shell_short}}?
{: #what-usage-length}
{: faq}
{: support}

You can use {{site.data.keyword.cloud-shell_short}} for up to 50 hours within a single week. If you reach this limit, all {{site.data.keyword.cloud-shell_short}} sessions are closed, and any data in your workspace is deleted. But don't worry, you can still access {{site.data.keyword.cloud-shell_short}} only in 5-minute increments until the week resets.

## How can I audit {{site.data.keyword.cloud-shell_short}} usage?
{: #how-audit-logs}
{: faq}

{{site.data.keyword.cloud-shell_short}} generates {{site.data.keyword.at_full_notm}} events for your sessions and commands. You can analyze these events by using the {{site.data.keyword.at_short}} service. For more information, see [Activity Tracker events for {{site.data.keyword.cloud-shell_notm}}](/docs/cloud-shell?topic=cloud-shell-at_events).

## How can I delete my data in {{site.data.keyword.cloud-shell_short}}?
{: #how-delete-data}
{: faq}
{: support}

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

## Can I use trusted profiles with {{site.data.keyword.cloud-shell_short}}?
{: #faq-use-trusted-profiles}
{: faq}

A [trusted profile](/docs/account?topic=account-create-trusted-profile&interface=ui) can be used to create and access a {{site.data.keyword.cloud-shell_short}} session, along with regular account access. When you use a trusted profile, you access the account that is associated with that profile.

## How can I switch account or trusted profile in {{site.data.keyword.cloud-shell_short}}?
{: #faq-switch-accounts}
{: faq}

To switch between an account and a [trusted profile](/docs/account?topic=account-create-trusted-profile&interface=ui), follow these steps:
- In the {{site.data.keyword.cloud_notm}} console, select the required account or trusted profile.
- Return to the existing {{site.data.keyword.cloud-shell_short}} browser tab. The session will automatically reload with the selected account or trusted profile. (or)
- In the {{site.data.keyword.cloud_notm}} console, click the ![{{site.data.keyword.cloud-shell_short}}](image-2.png) icon in the {{site.data.keyword.cloud_notm}} console. A new browser tab opens with the chosen account or trusted profile.

## Can I use `sudo` to run commands?
{: #faq-sudo}
{: faq}

{{site.data.keyword.cloud-shell_short}} is a restricted shell, so `sudo` isn't supported in {{site.data.keyword.cloud-shell_short}}.

## How do I manage access and locations for {{site.data.keyword.cloud-shell_short}}?
{: #faq-shell-access}

Account owners or {{site.data.keyword.cloud-shell_short}} administrators can control whether users in an account can access {{site.data.keyword.cloud-shell_short}}, and they can select the location for storing user session data. For more information, see the following topics:

* [Updating {{site.data.keyword.cloud-shell_short}} settings](/docs/account?topic=account-shell-settings)
* [Actions and roles for account management services](/docs/account?topic=account-account-services#shell-service-account-management)
