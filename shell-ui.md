---

copyright:
  years: 2020
lastupdated: "2020-04-10"

keywords: IBM Cloud Shell, cloud shell, terminal, shell session, usage limit, usage quota, restart, workspace, home directory

subcollection: cloud-shell

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:support: data-reuse='support'}

# Working in {{site.data.keyword.cloud-shell_short}}
{: #shell-ui}

{{site.data.keyword.cloud-shell_full}} contains a personal workspace and sessions where you can run commands. You can open up to five concurrent sessions, which operate independently so you can work with different resources, regions, and accounts at once.
{: shortdesc}

To open {{site.data.keyword.cloud-shell_notm}}, click the {{site.data.keyword.cloud-shell_notm}} icon ![{{site.data.keyword.cloud-shell_notm}} icon](../icons/terminal-cloud-shell.svg) in the {{site.data.keyword.cloud_notm}} console. A session starts and automatically logs you in with your current account through the {{site.data.keyword.cloud_notm}} CLI.

## Working with sessions
{: #shell-env}

A {{site.data.keyword.cloud-shell_short}} session is the terminal interface where you can run commands, scripts, and other tools. It's similar to the command prompt on your local machine, but it's preconfigured with the full {{site.data.keyword.cloud_notm}} CLI and numerous [plug-ins and tools](/docs/cloud-shell?topic=cloud-shell-plugins-tools) so that you can work in {{site.data.keyword.cloud_notm}} without having to install anything.

When you open a session, you start in your {{site.data.keyword.cloud-shell_short}} workspace's home directory, `/home/<user-name>`. Your home directory provides a temporary place for you to work with files in {{site.data.keyword.cloud-shell_short}}, and it's shared between all of your sessions. Because data in your home directory isn't persisted, any files that you add or change are removed after two hours of inactivity.

![A diagram that shows the workspace storage, which can be accessed in your home directory. The five sessions connect to the same workspace storage.](images/cloud-shell-env.svg "Sessions connect to your personal workspace storage."){: caption="Figure 1. Your personal workspace and sessions in Cloud Shell" caption-side="bottom"}

### Opening sessions
{: #multi-shell}
{: support}

To open a new session, click the Open icon ![Open a new session icon](../icons/add.svg). You can have up to five sessions open at one time. Each session maintains separate command histories, which are removed when you close the session. Because the workspace storage is shared between sessions, you can save a file to your home directory in one session, and then open the file in another session.

Each session automatically closes if it's not used for an hour. If you don't use {{site.data.keyword.cloud-shell_short}} for two hours - that is, another hour after the last session is closed - all files and data in your {{site.data.keyword.cloud-shell_short}} workspace are erased. If you need to step away from {{site.data.keyword.cloud-shell_short}}, be sure to download any files that you want to keep. For more information, see [Working with files](/docs/cloud-shell?topic=cloud-shell-files).
{: tip}

### Switching accounts
{: #switch-accounts}
{: support}

When you open a session, you're logged in with the {{site.data.keyword.cloud_notm}} CLI targeting the account and region that you were in when you opened {{site.data.keyword.cloud-shell_notm}}. This account and region are the default for every session, even if you changed them through the command line in another session. For example, say you run `ibmcloud login` to switch to a different account in a session. When you open a new session, it's logged in to the original account and not the one that you switched to previously.

To switch the default account for your sessions, close your {{site.data.keyword.cloud-shell_short}} environment, switch the account in the {{site.data.keyword.cloud_notm}} console menu bar, and then reopen {{site.data.keyword.cloud-shell_short}}.

## Changing locations
{: #change-location}

{{site.data.keyword.cloud-shell_short}} runs in the Dallas (`us-south`) and Frankfurt (`eu-de`) regions. Each {{site.data.keyword.cloud-shell_short}} location operates independently, which means that your workspace storage, sessions, and usage are separate. When you work in {{site.data.keyword.cloud-shell_short}}, the location that you're in determines the following aspects:

- Where your workspace data is stored, including any files that you upload and your user data, such as your session history and usage quota
- The default region that's targeted by the IBM Cloud CLI: `us-south` or `eu-de`

By default, the location that's closest to you geographically is selected when you open {{site.data.keyword.cloud-shell_short}} from the console. For example, if you're in California then {{site.data.keyword.cloud-shell_short}} opens to the Dallas region, but if you're in Paris it opens to the Frankfurt region.

To change to {{site.data.keyword.cloud-shell_short}} in a different location, find the current location in the {{site.data.keyword.cloud-shell_short}} menu bar, and click **Change**. Select the location that you want to switch to, and click **OK**.

If you change from the default location, {{site.data.keyword.cloud-shell_short}} remembers your location preferences by saving them as cookies in your browser. If you switch to a different browser or clear your browser cookies, {{site.data.keyword.cloud-shell_short}} will open in the default location.

## Restarting {{site.data.keyword.cloud-shell_short}}
{: #shell-restart}
{: support}

When you restart {{site.data.keyword.cloud-shell_short}}, any open sessions are closed and all of your files and data are removed. Before you restart, be sure that you download any files that you want to keep to your local system.

To restart, click the Menu icon ![More icon](../icons/actions-icon-vertical.svg), and select **Restart**.

## Tracking your usage
{: #usage-limit}

You can use {{site.data.keyword.cloud-shell_short}} for up to 30 hours within a week per region. Any time that you have at least one open session counts toward this usage quota, even if you aren't actively running commands. For example, if you're working in {{site.data.keyword.cloud-shell_short}} for 15 minutes and then leave your session open for a 30-minute lunch break, those 45 minutes are counted as usage. If you have three sessions open at the same time over an hour period, your usage is one hour because concurrent sessions don't count as additional usage. To minimize your usage, be sure to close sessions after you're done using them.

If you use all of your quota, your {{site.data.keyword.cloud-shell_short}} sessions are closed. Closing {{site.data.keyword.cloud-shell_short}} removes any data in your workspace, including your files and command history.

When you reach your usage quota, you get a notification that {{site.data.keyword.cloud-shell_short}} will close in 5 minutes. Use this time to complete any urgent tasks.
{: tip}

At any point, you can track your usage and check when your weekly quota resets. In the {{site.data.keyword.cloud-shell_short}} menu bar, click the Menu icon ![More icon](../icons/actions-icon-vertical.svg), and select **Usage quota**. You can view how many hours you used {{site.data.keyword.cloud-shell_short}} during the current weekly period and the date and time when it will reset.

The time that you used of the 30-hour usage quota resets back to 0 at the same time each week. Even after you used all of your quota, you can still use {{site.data.keyword.cloud-shell_notm}} for up to 5 minutes at a time to complete quick tasks, such as to run a few simple commands.

{{site.data.keyword.cloud-shell_notm}} is intended for {{site.data.keyword.cloud_notm}} administration and development purposes. It isn't intended to support long-running or compute-intensive scripts or programs or to process confidential data. Any usage outside of these guidelines might result in your access to {{site.data.keyword.cloud-shell_notm}} or {{site.data.keyword.cloud_notm}} being suspended. For more information, see the [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview/terms-of-use?topic=overview-terms).
{: note}
