---

copyright:
  years: 2020, 2022
lastupdated: "2022-04-14"

keywords: Cloud Shell release notes, Cloud Shell changes, Cloud Shell updates

subcollection: cloud-shell

---

{{site.data.keyword.attribute-definition-list}}

# Release notes
{: #release-notes-image}

Use the release notes to learn about the latest changes to {{site.data.keyword.cloud-shell_full}}.
{: shortdesc}

The {{site.data.keyword.cloud_notm}} CLI and plug-ins are regularly updated to the most recent available versions. These updates are not usually detailed in these release notes.
{: tip}

## 14 April 2022
{: #14-04-2022}

Helm version 3 is now the default version. When you run `helm` on {{site.data.keyword.cloud-shell_short}}, Helm version 3 is the version that runs. To run Helm version 2, type `helm2`. The `helm3` alias is also available if you use Helm version 3 in your scripts.

## 18 December 2020
{: #18-12-2020}

* Account owners or users with {{site.data.keyword.cloud-shell_short}} administrator access can enable or disable {{site.data.keyword.cloud-shell_short}} features for an account. The available features in this release are **File upload and download** and **Web preview**. The feature settings apply only to the enabled {{site.data.keyword.cloud-shell_short}} locations. For more information, see [Enabling or disabling {{site.data.keyword.cloud-shell_short}} features for an account](/docs/account?topic=account-shell-settings#shell-features-enable).
* An account administrator can grant specific users access to {{site.data.keyword.cloud-shell_short}} and its features, even if {{site.data.keyword.cloud-shell_short}} settings are disabled at the account level. For more information, see [Assigning access to {{site.data.keyword.cloud-shell_short}} and its features at a user level](/docs/account?topic=account-shell-settings#shell-access-user).
* The following new service roles are available:
   * Cloud Operator
   * Cloud Developer
   * File Manager

   For more information, see [IAM roles and actions](/docs/account?topic=account-iam-service-roles-actions#ibm-cloud-shell).
* {{site.data.keyword.cloud-shell_notm}} now uses a Red Hat&trade; Linux&trade; bash shell instead of a x86-64 Ubuntu Linux&trade; bash shell.

## 18 September 2020
{: #18-09-2020}

* Account owners or users with {{site.data.keyword.cloud-shell_short}} administrator access can manage {{site.data.keyword.cloud-shell_short}} settings from the {{site.data.keyword.cloud_notm}} console. For more information, see the following topics:
   - [Updating {{site.data.keyword.cloud-shell_short}} settings](/docs/account?topic=account-shell-settings)
   - [Actions and roles for account management services](/docs/account?topic=account-account-services#shell-service-account-management)
* The following tools are new with this {{site.data.keyword.cloud-shell_short}} update:
   - Terraform version switch (`tfswitch`) version 0.8.832
   - Tekton CLI (`tkn`) version 0.12.0
* The following tools are updated with this {{site.data.keyword.cloud-shell_short}} update:
   - `kn` upgrade to 0.14.0
   - The {{site.data.keyword.cloud_notm}} CLI (`ibmcloud`) is upgraded to version 1.2.1, and the CLI plug-ins are upgraded to the most recent versions

## 12 August 2020
{: #12-08-2020}

* Increased the weekly usage quota from 30 hours to 50 hours so you have more time to use {{site.data.keyword.cloud-shell_short}} each week. For more information about the usage quota, see [Tracking your usage](/docs/cloud-shell?topic=cloud-shell-shell-ui#usage-limit).
* Changed {{site.data.keyword.cloud-shell_short}} to have separate workspaces for each account. Previously, workspaces in each region were set at the user level, which meant that your workspace was shared across all of your accounts. For more information about workspaces, see [Your {{site.data.keyword.cloud-shell_short}} workspace](/docs/cloud-shell?topic=cloud-shell-shell-ui#shell-workspace).
* Moved the cookie preferences from the in-page button to the **Privacy** option in the {{site.data.keyword.cloud-shell_short}} menu.
* Updated the {{site.data.keyword.cloud-shell_short}} server image to version 1.0.1, which includes the following changes:
   * Added the Operator SDK (`operator-sdk`) for managing Kubernetes applications at version 0.19.0.
   * Added the Mercurial source content management tool (`hg`) at version 4.4.1.
   * Added the Bazaar version control system and CLI (`bzr`) at version 2.7.0.
   * Updated the Python runtime from version 3.5 to 3.6.
   * Updated the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform to 1.8.1

## 24 June 2020
{: #24-06-2020}

{{site.data.keyword.cloud-shell_notm}} is now generally available (GA)! With this release, {{site.data.keyword.cloud-shell_short}} includes the following updates:
* Increased service level availability to 99.99% and hardened disaster recovery plan to meet {{site.data.keyword.cloud_notm}} requirements. For more information, see [Understanding high availability and disaster recovery for {{site.data.keyword.cloud-shell_short}}](/docs/cloud-shell?topic=cloud-shell-ha-dr).
* Added support for inputting and viewing double-byte characters on the command line in your sessions. This enables you to work in national languages such as Japanese, Simplified Chinese, or Traditional Chinese.
* Added support for the Tokyo (`jp-tok`) region.
* Added cookie preferences so you can choose which cookies {{site.data.keyword.cloud-shell_short}} saves. {{site.data.keyword.cloud-shell_short}} relies on personalization cookies to remember your region preferences.
* Added a link to these release notes from the About {{site.data.keyword.cloud-shell_notm}} window, so you can find them even more easily in the future.
* Updated the {{site.data.keyword.cloud-shell_short}} server image to version 0.7.1, which includes the following changes:
   * Updated the ISTIO CLI (`istioctl`) to 1.5.4.
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
* Added support for running {{site.data.keyword.cloud-shell_short}} in the Frankfurt (`eu-de`) region. Each region runs independently, so your workspace, sessions, and usage are separate. For more information, see [Changing locations](/docs/cloud-shell?topic=cloud-shell-shell-ui#change-location).
* Extended the time after which inactive sessions are closed from 30 minutes to an hour.
* Extended the time after which workspace data is removed due to inactivity from 30 minutes to an hour after there are no open sessions.
* Removed the 4-hour continuous usage limit. You can now use {{site.data.keyword.cloud-shell_short}} for any length of time up to the weekly usage quota.
* Updated the {{site.data.keyword.cloud-shell_short}} server image to version 0.6.3, which includes the following changes:
   * Added GNU Automake (`automake`).
   * Added GNU Compiler Collection (`gcc`, `gcov`, and `gcov-tool`).
   * Downgraded the ISTIO CLI (`istioctl`) from 1.5 to 1.4.
   * Updated the {{site.data.keyword.cloud_notm}} CLI and all plug-ins to the most recent versions.


## 16 February 2020
{: #image-0-4-37}

Updated the {{site.data.keyword.cloud-shell_short}} server image to version 0.4.37. Changes to this image affect the tools and other capabilities that are available in each session.

* Enabled auto-completion for the {{site.data.keyword.cloud_notm}} CLI.
* Added the community `kn` Knative CLI and removed the third-party `knctl` Knative CLI.
* Added the {{site.data.keyword.ibmwatson_notm}} CLI plug-in (`ibmcloud watson`).
* Updated {{site.data.keyword.cloud_notm}} CLI plug-ins to the most recent versions.
* Updated the ISTIO CLI (`istoctl`) to version 1.4.4.
