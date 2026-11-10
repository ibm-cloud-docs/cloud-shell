---

copyright:
  years: 2026
lastupdated: "2026-11-10"

keywords: Cloud Shell transition, Cloud Shell FAQ, IBM Paver Shell, Paver, Paver Shell FAQ, Cloud Shell to Paver

subcollection: cloud-shell

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQs for the transition from IBM Cloud Shell to IBM Paver Shell
{: #faqs-paver-transition}

Effective November 10, 2026, {{site.data.keyword.cloud-shell_notm}} will no longer be the default web shell experience on {{site.data.keyword.cloud_notm}}. [Paver Shell](https://paver.cloud.ibm.com){: external} is the recommended experience for managing infrastructure. With Paver, you can complete tasks, solve issues, optimize resources, and stay informed about what's happening in your environment. For more information, see [Using the {{site.data.keyword.IBM_notm}} Paver interactive shell](https://paver.ibm.com/docs/core-concepts/shell/){: external}.
{: important}



Frequently asked questions about the transition from {{site.data.keyword.cloud-shell_full}} to {{site.data.keyword.IBM_notm}} Paver Shell include questions about the timeline, access, workspace storage, and capabilities. To find all FAQs for {{site.data.keyword.cloud}}, see the [FAQ library](/docs/faqs).
{: shortdesc}

## What is changing with {{site.data.keyword.cloud-shell_notm}}?
{: #paver-faq-what-changing}
{: faq}

{{site.data.keyword.cloud-shell_notm}} is transitioning to {{site.data.keyword.IBM_notm}} Paver Shell, the next-generation shell experience in {{site.data.keyword.IBM_notm}} Paver for {{site.data.keyword.cloud_notm}}. {{site.data.keyword.IBM_notm}} Paver Shell retains the core browser-based terminal of {{site.data.keyword.cloud-shell_notm}} and adds AI-assisted interactions.

## Why is {{site.data.keyword.IBM_notm}} transitioning from {{site.data.keyword.cloud-shell_notm}} to {{site.data.keyword.IBM_notm}} Paver Shell?
{: #paver-faq-why-transition}
{: faq}

{{site.data.keyword.IBM_notm}} is evolving {{site.data.keyword.cloud-shell_notm}} into a more intelligent, AI-driven experience for cloud operations. {{site.data.keyword.IBM_notm}} Paver Shell is designed to retain familiar terminal workflows while adding natural-language interactions, cloud resource context, and AI-assisted command execution.

## What is {{site.data.keyword.IBM_notm}} Paver Shell, and what can I do with it?
{: #paver-faq-what-is-paver-shell}
{: faq}

{{site.data.keyword.IBM_notm}} Paver Shell combines a browser-based terminal and command-line tools with a chat-based, AI-assisted experience. It supports direct command-line interface (CLI) commands and natural-language requests to work with {{site.data.keyword.cloud_notm}} resources. It also provides capabilities such as multiple concurrent sessions and more flexible terminal usage.

## Is {{site.data.keyword.IBM_notm}} Paver Shell the recommended shell experience for infrastructure operations?
{: #paver-faq-recommended-shell}
{: faq}

Yes. {{site.data.keyword.IBM_notm}} Paver Shell is the recommended shell experience for infrastructure operations while {{site.data.keyword.cloud_notm}} transitions from the existing {{site.data.keyword.cloud-shell_notm}} experience.

## What is the transition timeline for {{site.data.keyword.cloud-shell_notm}}?
{: #paver-faq-timeline}
{: faq}

{{site.data.keyword.cloud-shell_notm}} remains available until March 31, 2027. After this date, {{site.data.keyword.IBM_notm}} Paver Shell replaces {{site.data.keyword.cloud-shell_notm}}.

## How do I access {{site.data.keyword.IBM_notm}} Paver Shell, and can I continue using {{site.data.keyword.cloud-shell_notm}} during the transition?
{: #paver-faq-access}
{: faq}

Click the {{site.data.keyword.cloud-shell_notm}} icon in the {{site.data.keyword.cloud_notm}} console. A transition dialog opens, where you can choose between {{site.data.keyword.IBM_notm}} Paver Shell and {{site.data.keyword.cloud-shell_notm}}. To access {{site.data.keyword.IBM_notm}} Paver Shell, select **Try Paver**. To continue using the existing experience, select {{site.data.keyword.cloud-shell_notm}}. The dialog opens each time that you click the {{site.data.keyword.cloud-shell_notm}} icon during the transition period.

## Will there be any service interruption during the transition?
{: #paver-faq-service-interruption}
{: faq}

No service interruption is planned as part of the transition. {{site.data.keyword.cloud-shell_notm}} remains available until March 31, 2027.

## What happens to files stored in my existing {{site.data.keyword.cloud-shell_notm}} workspace?
{: #paver-faq-existing-files}
{: faq}

{{site.data.keyword.cloud-shell_notm}} provides 500 MB of temporary workspace storage. Files and data are removed after one hour of inactivity or when the usage quota is reached. Download any files that you need to keep before they are removed.

## Do I need to migrate my existing {{site.data.keyword.cloud-shell_notm}} environment to {{site.data.keyword.IBM_notm}} Paver Shell?
{: #paver-faq-migrate-environment}
{: faq}

No. A separate workspace migration is not required. {{site.data.keyword.cloud-shell_notm}} workspace storage is temporary, and files and data are removed automatically. For more information, see [What happens to files stored in my existing {{site.data.keyword.cloud-shell_notm}} workspace?](#paver-faq-existing-files). Download any files that you need to retain before they are deleted.

## Will my existing {{site.data.keyword.cloud_notm}} CLI commands and tools be available in {{site.data.keyword.IBM_notm}} Paver Shell?
{: #paver-faq-cli-tools}
{: faq}

{{site.data.keyword.IBM_notm}} Paver Shell is designed to retain the core terminal and CLI capabilities of {{site.data.keyword.cloud-shell_notm}}, including the {{site.data.keyword.cloud_notm}} CLI and Linux tools. It also adds chat-based, AI-assisted interactions.

## What happens after the transition from {{site.data.keyword.cloud-shell_notm}} to {{site.data.keyword.IBM_notm}} Paver Shell?
{: #paver-faq-after-transition}
{: faq}

After March 31, 2027, the {{site.data.keyword.IBM_notm}} Paver icon replaces the {{site.data.keyword.cloud-shell_notm}} icon in the {{site.data.keyword.cloud_notm}} console. The Paver icon opens {{site.data.keyword.IBM_notm}} Paver Shell.

## Can I use chat and terminal together in {{site.data.keyword.IBM_notm}} Paver?
{: #paver-faq-chat-terminal}
{: faq}

Yes. In {{site.data.keyword.IBM_notm}} Paver, you can work through chat, a terminal, or both. Chat and terminal share context, so you can work across both interfaces within the same environment.

## What types of infrastructure operations can {{site.data.keyword.IBM_notm}} Paver assist with?
{: #paver-faq-infrastructure-operations}
{: faq}

{{site.data.keyword.IBM_notm}} Paver provides AI-assisted guidance for infrastructure troubleshooting, deployment, migration, and day-to-day operations. It also supports guided workflows and automated operational assistance to help you complete infrastructure-related tasks.

## What safeguards are available when I perform actions in {{site.data.keyword.IBM_notm}} Paver?
{: #paver-faq-safeguards}
{: faq}

{{site.data.keyword.IBM_notm}} Paver includes built-in guardrails that can explain actions and support approval-based workflows. These guardrails help you understand operations and work through appropriate approval processes.

## Can I store files and artifacts in {{site.data.keyword.IBM_notm}} Paver?
{: #paver-faq-store-files}
{: faq}

{{site.data.keyword.IBM_notm}} Paver provides a managed workspace that supports storing and working with files and artifacts within the Paver environment.
