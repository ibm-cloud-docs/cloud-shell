---

copyright:
  years: 2020, 2024
lastupdated: "2024-06-05"

keywords: getting started tutorial, IBM Cloud Shell, cloud shell, IBM Cloud cli, using IBM Cloud Shell, cloud shell access
content-type: tutorial
services:
account-plan: lite
completion-time: 30m
subcollection: cloud-shell

---

{{site.data.keyword.attribute-definition-list}}

# Getting started with {{site.data.keyword.cloud-shell_notm}}
{: #getting-started}
{: toc-content-type="tutorial"}
{: toc-services=""}
{: toc-completion-time="30m"}

In this getting started tutorial, you use {{site.data.keyword.cloud-shell_full}} to clone a sample Node.js app. {{site.data.keyword.cloud-shell_notm}} is a cloud-based shell workspace that you can access through your browser. It's preconfigured with the full [{{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cli-getting-started) and tons of plug-ins and tools that you can use to manage apps, resources, and infrastructure.
{: shortdesc}

New to {{site.data.keyword.cloud-shell_short}}? [Watch the demo video](https://www.youtube.com/watch?v=a8YHFyYfpVI){: external} to see how quickly you can start using it from the {{site.data.keyword.cloud_notm}} console.
{: tip}

## Before you begin
{: #prereqs}

* If you don't already have an {{site.data.keyword.cloud_notm}} account, [sign up for one](/registration/){: external} and log in.
* Note the following account access information that might affect your access to {{site.data.keyword.cloud-shell_short}} and its features:
   * An account administrator can grant specific users access to {{site.data.keyword.cloud-shell_short}} and its features, even if {{site.data.keyword.cloud-shell_short}} settings are disabled at the account level. For more information, see [Assigning access to {{site.data.keyword.cloud-shell_short}} and its features at a user level](/docs/account?topic=account-shell-settings#shell-access-user).
   * Account owners or users with {{site.data.keyword.cloud-shell_short}} administrator access can enable or disable {{site.data.keyword.cloud-shell_short}} features for an account. The available features in this release are **File upload and download** and **Web preview**. The feature settings apply only to the enabled {{site.data.keyword.cloud-shell_short}} locations. For more information, see [Enabling or disabling {{site.data.keyword.cloud-shell_short}} features for an account](/docs/account?topic=account-shell-settings#shell-features-enable).
   * For more information, see [IAM roles and actions](/docs/account?topic=account-iam-service-roles-actions#cloudshell-roles).

## Start a session in {{site.data.keyword.cloud-shell_notm}}
{: #open-shell}
{: step}

In the {{site.data.keyword.cloud_notm}} console, click the {{site.data.keyword.cloud-shell_notm}} icon ![{{site.data.keyword.cloud-shell_notm}} icon](../icons/terminal-cloud-shell.svg). A session starts and automatically logs you in through the {{site.data.keyword.cloud_notm}} CLI.

## Clone the Node.js sample app
{: #clone-app}
{: step}

Your {{site.data.keyword.cloud-shell_short}} session starts in the temporary home directory, `/home/<user-name>`. Clone the [Node.js Express sample app](https://github.com/IBM/nodejs-express-app){: external} to this directory and then change to the sample app directory by running the following commands.

```bash
git clone https://github.com/IBM/nodejs-express-app.git
```
{: pre}

```bash
cd nodejs-express-app
```
{: pre}

From your app directory, run the following command to view the new files.

```bash
ls
```
{: pre}

You can see that your `nodejs-express-app` directory contains all of the sample app files and folders.

```text
Dockerfile  Dockerfile-tools  LICENSE  README.md  package-lock.json
package.json  public  scripts  server  test
```
{: screen}

## Preview the app locally
{: #preview-app-locally}
{: step}

You can start it in {{site.data.keyword.cloud-shell_short}} and preview it locally.

1. First, download project dependencies for the Node.js sample app.

   ```bash
   npm install --only=prod
   ```
   {: pre}

1. Start the app.

   ```bash
   npm run start
   ```
   {: pre}

   When the app is running, it outputs the location where the app UI is available. For {{site.data.keyword.cloud-shell_short}}, you only need to note the port, which in this case is `3000` .

   ```text
   > nodejsexpressapp@1.0.0 start /home/my-user-name/nodejs-express-app
   > node server/server.js

   App UI available http://localhost:3000
   Swagger UI available http://localhost:3000/swagger/api-docs
   ```
   {: screen}

1. In the {{site.data.keyword.cloud-shell_short}} menu bar, click the **Web preview** icon ![Web preview](../icons/view.svg), and select port 3000.

   Your app preview opens in a new window. If you see the congratulations message, your app is running locally in {{site.data.keyword.cloud-shell_short}}!

1. Press `Control+C` to stop the app.

## Next steps
{: #next-steps}

From {{site.data.keyword.cloud-shell_short}}, you can quickly run commands on your {{site.data.keyword.cloud_notm}} account. For example:

* [Managing IAM access, API keys, service IDs, and access groups](/docs/cli?topic=cli-ibmcloud_commands_iam)
* [Viewing billing and usage information](/docs/cli?topic=cli-ibmcloud_billing)

In addition to the {{site.data.keyword.cloud_notm}} CLI, {{site.data.keyword.cloud-shell_short}} is preconfigured with all {{site.data.keyword.cloud_notm}} CLI plug-ins and many tools and runtimes to help you work in the cloud. For the full list, see [Installed plug-ins and tools](/docs/cloud-shell?topic=cloud-shell-plugins-tools).
