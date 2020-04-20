---

copyright:
  years: 2020
lastupdated: "2020-04-18"

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

