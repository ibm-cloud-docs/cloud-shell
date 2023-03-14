---

copyright:
  years: 2020, 2023
lastupdated: "2023-03-14"

keywords: Cloud Shell troubleshooting, cloud shell connection lost, could not start cloud shell, cloud shell bashrc, Cloud Shell hangs, Cloud Shell closes, Cloud Shell restarts

subcollection: cloud-shell

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Troubleshooting for {{site.data.keyword.cloud-shell_notm}}
{: #troubleshooting}

Use these tips to help troubleshoot problems that you might run into when you use {{site.data.keyword.cloud-shell_full}}.
{: shortdesc}

Running into issues that you can't fix? We want to hear about it. [Submit feedback](/docs/cloud-shell?topic=cloud-shell-feedback) about {{site.data.keyword.cloud-shell_short}} through our UI. Or come chat with the development team on [{{site.data.keyword.cloud_notm}} Dev Tools Slack](https://ic-devops-slack-invite.us-south.devops.cloud.ibm.com/){: external}. After you request your invitation, sign in and join the `#ask-your-question` channel.
{: tip}

## Why can't my sessions start?
{: #trouble-restart}
{: troubleshoot}

When you try to start {{site.data.keyword.cloud-shell_short}} or restart it after you were idle or your connection was lost, the following message is displayed:
{: tsSymptoms}

`Your session couldn't be started.` or `Session could not be started. Please wait for a few minutes, then restart the cloud shell and try again.`

Refresh your {{site.data.keyword.cloud-shell_short}} browser tab or window. If {{site.data.keyword.cloud-shell_short}} still can't start, try the following possible solutions:
{: tsResolve}

- Restart from the {{site.data.keyword.cloud-shell_short}} menu.
- Check if the IP address restriction is [defined for the account or the user](/docs/account?topic=account-ips). If the IP address restriction is defined, [add the {{site.data.keyword.cloud-shell_short}} ingress IP ranges](/docs/cloud-shell?topic=cloud-shell-cs-ip-ranges) to log in from the {{site.data.keyword.cloud-shell_short}} service. If the IP address restriction is not defined and you continue to see this issue, create a support case.
- Log out of {{site.data.keyword.cloud}}. Clear your browser cache and cookies to remove your preferences and then log in again and open {{site.data.keyword.cloud-shell_short}}.

## Why can't I work with my Kubernetes clusters from my session?
{: #trouble-kube}
{: troubleshoot}
{: support}

You want to work with your {{site.data.keyword.containerlong}} clusters, but when you run a command such as `kubectl get pods`, the following error is displayed:
{: tsSymptoms}

```text
$ kubectl get pods
The connection to the server localhost:8080 was refused - did you specify the correct host or port?
```

The cluster isn't currently set as the context. As with your local development environment, the cluster context must be set for each individual session.
{: tsCauses}

Set the cluster as the context in your session as described in [Configuring the CLI to run `kubectl`](/docs/containers?topic=containers-cs_cli_install#cs_cli_configure).
{: tsResolve}

## What do I do if I changed my `.bashrc` file and my sessions don't work?
{: #trouble-bashrc}
{: troubleshoot}
{: support}

You customized your {{site.data.keyword.cloud-shell_short}} sessions by editing the `.bashrc` file, and now your sessions don't open. As a result, you can't work in {{site.data.keyword.cloud-shell_short}}.
{: tsSymptoms}

Some code in your `.bashrc` file isn't working correctly, and it's interfering with your sessions' ability to initialize.
{: tsCauses}

If you're able to run commands from an existing open session, [download any files](/docs/cloud-shell?topic=cloud-shell-files) that you want to keep. Then, restart {{site.data.keyword.cloud-shell_short}} by going to the {{site.data.keyword.cloud-shell_short}} menu and clicking **Restart**.
{: tsResolve}

## Why do I keep losing my connection to {{site.data.keyword.cloud-shell_short}}?
{: #trouble-connection}
{: troubleshoot}
{: support}

You're working in {{site.data.keyword.cloud-shell_short}} when your session closes with the following message:
{: tsSymptoms}

`The connection to your session was lost.`

You might see this error for a few reasons:
{: tsCauses}

* Your internet connection was unstable.
* You reached the maximum capacity for your {{site.data.keyword.cloud-shell_short}} temporary storage.
* Rarely, the {{site.data.keyword.cloud-shell_short}} region you were working in is unavailable.

If your connection was lost because of a temporary hiccup in your internet connection, refresh the browser window to reconnect. If you continue to be disconnected, restart {{site.data.keyword.cloud-shell_short}}. Restarting {{site.data.keyword.cloud-shell_notm}} removes all files in your workspace, so be sure to [download any files](/docs/cloud-shell?topic=cloud-shell-files) that you want to keep.
{: tsResolve}

If a region is unavailable, restarting {{site.data.keyword.cloud-shell_short}} automatically loads it in an available region if you didn't change the {{site.data.keyword.cloud-shell_short}} location from the default. If you did manually change to a different location, clear your browser cache and cookies to remove your preferences, and then open {{site.data.keyword.cloud-shell_short}}.

## Why does {{site.data.keyword.cloud-shell_short}} hang, close, or restart?
{: #trouble-resource-use}
{: troubleshoot}
{: support}

You're working in {{site.data.keyword.cloud-shell_short}} when your session hangs or closes with no message.
{: tsSymptoms}

{{site.data.keyword.cloud-shell_short}} might hang, experience slow performance, or close with intensive resource usage. If too many resources are used, the {{site.data.keyword.cloud-shell_short}} environment might restart. When {{site.data.keyword.cloud-shell_short}} closes, any data in your workspace is deleted.
{: tsCauses}
