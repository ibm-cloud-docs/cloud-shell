---

copyright:
  years: 2020
lastupdated: "2020-06-24"

keywords: IBM Cloud Shell, Cloud Shell, release notes, changes, updates, image version

subcollection: cloud-shell

---

{:external: target="_blank" .external}
{:shortdesc: .shortdesc}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:important: .important}
{:note: .note}

# Release notes
{: #release-notes-image}

Use these release notes to learn about the latest changes to {{site.data.keyword.cloud-shell_full}}.
{: shortdesc}

The {{site.data.keyword.cloud_notm}} CLI and plug-ins are regularly updated to the latest available versions.
{: tip}

## 24 June 2020
{: #24-06-2020}

{{site.data.keyword.cloud-shell_notm}} is now generally available (GA)! With this release, {{site.data.keyword.cloud-shell_short}} includes the following updates:
* Increased service level availability to 99.99% and hardened disaster recovery plan to meet {{site.data.keyword.cloud_notm}} requirements. For more information, see [Understanding high availability and disaster recovery for {{site.data.keyword.cloud-shell_short}}](/docs/cloud-shell?topic=cloud-shell-ha-dr).
* Added support for inputting and viewing double-byte characters on the command line in your sessions. This enables you to work in national languages such as Japanese, Simplified Chinese, or Traditional Chinese.
* Added support for the Tokyo (`jp-tok`) region.
* Added cookie preferences so you can choose which cookies {{site.data.keyword.cloud-shell_short}} saves. {{site.data.keyword.cloud-shell_short}} relies on personalization cookies to remember your region preferences.
* Added a link to these release notes from the About {{site.data.keyword.cloud-shell_notm}} window, so you can find them even more easily in the future.
* Updated the {{site.data.keyword.cloud-shell_short}} server image to version 0.7.1, which includes the following changes:
   * Updated the Istio CLI (`istioctl`) to 1.5.4.
   * Added auto-complete for Red Hat OpenShift CLI (`oc`).
   * Added the Cloud Foundry CLI installed in the {{site.data.keyword.cloud_notm}} CLI context (`ibmcloud cf`).

## 15 May 2020
{: #15-05-2020}

Updated the {{site.data.keyword.cloud-shell_short}} server image to version 0.6.6:
* Updated Red Hat&reg; OpenShift CLI (`oc`) to 4.3.
* Updated the {{site.data.keyword.cloud_notm}} CLI and all plug-ins to the latest versions.
* Removed Netcat networking utility (`netcat`).

## 18 April 2020
{: #18-04-2020}

* Added the ability to preview web apps that you access through {{site.data.keyword.cloud-shell_short}}. For more information, see [Previewing apps](/docs/cloud-shell?topic=cloud-shell-preview-apps).
* Added support for running {{site.data.keyword.cloud-shell_short}} in the Frankfurt (`eu-de`) region. Each region runs independently, so your workspace, sessions, and usage are completely separate. For more information, see [Changing locations](/docs/cloud-shell?topic=cloud-shell-shell-ui#change-location).
* Extended the time after which inactive sessions are closed from 30 minutes to an hour.
* Extended the time after which workspace data is removed due to inactivity from an 30 minutes to an hour after there are no open sessions.
* Removed the 4-hour continuous usage limit. You can now use {{site.data.keyword.cloud-shell_short}} for any length of time up to the weekly usage quota.
* Updated the {{site.data.keyword.cloud-shell_short}} server image to version 0.6.3, which includes the following changes:
   * Added GNU Automake (`automake`).
   * Added GNU Compiler Collection (`gcc`, `gcov`, and `gcov-tool`).
   * Downgraded the Istio CLI (`istioctl`) from 1.5 to 1.4.
   * Updated the {{site.data.keyword.cloud_notm}} CLI and all plug-ins to the latest versions.


## 16 February 2020
{: #image-0-4-37}

Updated the {{site.data.keyword.cloud-shell_short}} server image to version 0.4.37. Changes to this image affect the tools and other capabilities that are available in each session.

* Enabled auto-completion for the {{site.data.keyword.cloud_notm}} CLI.
* Added the community `kn` Knative CLI and removed the third-party `knctl` Knative CLI.
* Added the {{site.data.keyword.ibmwatson_notm}} CLI plug-in (`ibmcloud watson`).
* Updated {{site.data.keyword.cloud_notm}} CLI plug-ins to the latest versions.
* Updated the Istio CLI (`istoctl`) to version 1.4.4.

