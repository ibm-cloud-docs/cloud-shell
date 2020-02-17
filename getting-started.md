---

copyright:
  years: 2020
lastupdated: "2020-02-17"

keywords: getting started tutorial, IBM Cloud Shell, cloud shell, cli, shell

subcollection: cloud-shell

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# Getting started with {{site.data.keyword.cloud-shell_notm}}
{: #getting-started}

In this getting started tutorial, you use {{site.data.keyword.cloud-shell_full}} to clone a sample Node.js app and deploy it to Cloud Foundry on {{site.data.keyword.cloud}}. {{site.data.keyword.cloud-shell_notm}} is a cloud-based shell workspace that you can access through your browser. It's preconfigured with the full {{site.data.keyword.cloud_notm}} CLI and tons of plug-ins and tools that you can use to manage apps, resources, and infrastructure. This tutorial takes about 5 minutes to complete.
{: shortdesc}

New to {{site.data.keyword.cloud-shell_short}}? [Watch the demo video](https://www.youtube.com/watch?v=a8YHFyYfpVI){: external} to see how quickly you can start using it from the {{site.data.keyword.cloud_notm}} console.
{: tip}

## Before you begin
{: #prereqs}
If you don't already have an {{site.data.keyword.cloud_notm}} account, [sign up for one](https://cloud.ibm.com/registration/) and log in. And that's it - because {{site.data.keyword.cloud-shell_notm}} is instantly accessible from the console, no other installation is needed.

## Step 1. Start a session in {{site.data.keyword.cloud-shell_notm}}
{: #open-shell}

In the console menu bar, click the {{site.data.keyword.cloud-shell_notm}} icon ![{{site.data.keyword.cloud-shell_notm}} icon](../icons/terminal-cloud-shell.svg). A session starts and automatically logs you in through the {{site.data.keyword.cloud_notm}} CLI.

## Step 2. Clone the Node.js sample app
{: #clone-app}

Your {{site.data.keyword.cloud-shell_short}} session starts in the temporary home directory, `/home/<user-name>`. Clone the [Hello World sample app](https://github.com/IBM-Cloud/node-helloworld){: external} to this directory and then change to the sample app directory by running the following commands.

```bash
git clone https://github.com/IBM-Cloud/node-helloworld.git
```
{: pre}

```bash
cd node-helloworld
```
{: pre}

From your app directory, run the following command to view the new files.

```bash
ls -R
```
{: pre}

You can see that your `node-helloworld` directory contains all of the sample app files.

```
.:
LICENSE  Procfile  README.md  manifest.yml  package.json  public  server.js

./public:
index.html  styles.css
```
{: screen}

## Step 3. Target a Cloud Foundry org and space
{: #target-cf}

Because you're deploying the sample app to Cloud Foundry, you need to target a Cloud Foundry org and space. The org and space help to organize your Cloud Foundry services and apps.

Run the following command to interactively target a Cloud Foundry instance and select an org and space. If you have only a single org or space, it's automatically selected for you.

```bash
ibmcloud target --cf
```
{: pre}

## Step 4. Deploy your app
{: #deploy-app}

Build and deploy your app in Cloud Foundry by running the following command.

```bash
ibmcloud cf push node-helloworld
```
{: pre}

As the command runs, it creates your app, downloads any dependencies, and then deploys it. When the app starts, details about the app, such as its URL, memory usage, and status, are displayed.

To view your running app, copy the `routes` URL and paste it in your browser.

```
name:              node-helloworld
requested state:   started
routes:            node-helloworld.us-south.cf.appdomain.cloud
last uploaded:     Wed 01 Jan 12:34:56 UTC 2020
stack:             cflinuxfs3
buildpacks:        sdk-for-nodejs

type:            web
instances:       1/1
memory usage:    128M
start command:   node server
     state     since                  cpu    memory      disk      details
#0   running   2020-01-01T12:34:56Z   0.0%   0 of 128M   0 of 1G
```
{: screen}

## Next steps
{: #next-steps}

<!-- Now that you're familiar with deploying a basic Cloud Foundry app, try an in-depth tutorial for [creating apps by using the CLI](/docs/cli?topic=creating-apps-create-deploy-app-cli) that deploys an app in a DevOps pipeline. -->

From {{site.data.keyword.cloud-shell_short}}, you can quickly run commands on your {{site.data.keyword.cloud_notm}} account. For example:

* [Managing accounts, users, and Cloud Foundry orgs](/docs/cli?topic=cloud-cli-ibmcloud_commands_account)
* [Managing IAM access, API keys, service IDs, and access groups](/docs/cli?topic=cloud-cli-ibmcloud_commands_iam)
* [Viewing usage for accounts, orgs, resource groups, and resources](/docs/cli?topic=cloud-cli-ibmcloud_billing)

In addition to the {{site.data.keyword.cloud_notm}} CLI, {{site.data.keyword.cloud-shell_short}} is preconfigured with all {{site.data.keyword.cloud_notm}} CLI plug-ins and many tools and runtimes to help you work in the cloud. For the full list, see [Installed plug-ins and tools](/docs/cloud-shell?topic=cloud-shell-plugins-tools).
