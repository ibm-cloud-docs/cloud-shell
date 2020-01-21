---

copyright:
  years: 2020
lastupdated: "2020-01-21"

keywords: IBM Cloud Shell, troubleshooting, error, disconnect, connection lost, could not start cloud shell, bashrc

subcollection: cloud-shell

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:external: target="_blank" .external}
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}
{:support: data-reuse='support'}


# Troubleshooting for {{site.data.keyword.cloud-shell_notm}}
{: #troubleshooting}

Use these tips to help troubleshoot problems that you might run into when you use {{site.data.keyword.cloud-shell_full}}.
{: shortdesc}

Running into issues that you can't fix? We want to hear about it. [Submit feedback](/docs/cloud-shell?topic=cloud-shell-feedback) about {{site.data.keyword.cloud-shell_short}} through our UI or Slack channel.
{: tip}

## Why can't my sessions start?
{: #trouble-restart}
{: troubleshoot}

When you try to start {{site.data.keyword.cloud-shell_short}} or restart it after you were idle or your connection was lost, the following message is displayed:
{: tsSymptoms}

`Your session couldn't be started.`

Refresh your {{site.data.keyword.cloud-shell_short}} browser tab or window. If {{site.data.keyword.cloud-shell_short}} still can't start, try restarting from the {{site.data.keyword.cloud-shell_short}} menu. If you continue to see this issue, create a support case.
{: tsResolve}

## Why can't I work with my Kubernetes clusters from my session?
{: #trouble-kube}
{: troubleshoot}

You want to work with your {{site.data.keyword.containerlong}} clusters, but when you run a command such as `kubectl get pods`, the following error is displayed:
{: tsSymptoms}

```
$ kubectl get pods
The connection to the server localhost:8080 was refused - did you specify the right host or port?
```

The cluster isn't currently set as the context. As with your local development environment, the cluster context must be set for each individual session.
{:tsCauses}

Set the cluster as the context in your session as described in [Configuring the CLI to run `kubectl`](/docs/containers?topic=containers-cs_cli_install#cs_cli_configure).
{: tsResolve}

## What do I do if I changed my `.bashrc` file and my sessions don't work?
{: #trouble-bashrc}
{: troubleshoot}

You customized your {{site.data.keyword.cloud-shell_short}} sessions by editing the `.bashrc` file, and now your sessions don't open. As a result, you can't work in {{site.data.keyword.cloud-shell_short}}.
{: tsSymptoms}

Some code in your `.bashrc` file isn't working correctly, and it's interfering with your sessions' ability to initialize.
{:tsCauses}

If you're able to run commands from an existing open session, [download any files](/docs/cloud-shell?topic=cloud-shell-files) that you want to keep. Then, restart  {{site.data.keyword.cloud-shell_short}} by going to the {{site.data.keyword.cloud-shell_short}} menu and clicking **Restart**.
{: tsResolve}

## Why do I keep losing my connection to {{site.data.keyword.cloud-shell_short}}?
{: #trouble-connection}
{: troubleshoot}

You're working in {{site.data.keyword.cloud-shell_short}} when your session closes with the following message:
{: tsSymptoms}

`The connection to your session was lost.`

You might see this error for a few reasons:
{: tsCauses}
* Your internet connection was unstable.
* You reached the maximum capacity for your {{site.data.keyword.cloud-shell_short}} temporary storage.

If your connection was lost because of a temporary hiccup in your internet connection, refresh the browser window to reconnect. If you continue to be disconnected, restart {{site.data.keyword.cloud-shell_short}}. Restarting {{site.data.keyword.cloud-shell_notm}} removes all files in your workspace, so be sure to [download any files](/docs/cloud-shell?topic=cloud-shell-files) that you want to keep.
{: tsResolve}
