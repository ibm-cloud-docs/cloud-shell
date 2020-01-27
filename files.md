---

copyright:
  years: 2020
lastupdated: "2020-01-24"

keywords: IBM Cloud Shell, upload file in cloud shell, download file in cloud shell, add file, add project to cloud shell, file storage, persistence, import file, export file

subcollection: cloud-shell

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:pre: .pre}

# Working with files
{: #files}

Your {{site.data.keyword.cloud-shell_full}} workspace includes a home directory where you can temporarily work with files in your {{site.data.keyword.cloud-shell_short}} sessions. You can upload or download files one at a time to your workspace through the UI, or use command-line tools to work with many files at once.
{: shortdesc}

## Temporary workspace storage
{: #file-persistence}

Your {{site.data.keyword.cloud-shell_notm}} workspace includes 500 MB of temporary secure storage that you can access through your personal home directory, `/home/<user-name>`. This storage space is provided at the user level rather than the account level. This means that only you can access your storage, and you can access it from any of your accounts. No one else in your accounts can access your workspace storage.

Your workspace storage is shared across all of your sessions, so you can work with the same files in different session tabs. The storage persists only while your workspace is active. If you're idle in {{site.data.keyword.cloud-shell_short}} for over an hour, your files and data are removed. Similarly, if you reach a usage limit or you restart {{site.data.keyword.cloud-shell_short}}, {{site.data.keyword.cloud-shell_short}} closes and removes your data. If you make any changes to files that you want to keep, be sure to download the files at the end of your session.

There is a known issue where your connection to {{site.data.keyword.cloud-shell_short}} is lost if your reach the temporary storage limit. If this happens, the only way to fix the connection is to restart {{site.data.keyword.cloud-shell_short}}, which removes all of your files. While working in {{site.data.keyword.cloud-shell_notm}}, avoid uploading large files and remove any unused files by using standard Linux&trade; commands, such as `rm`.
{: important}

### Backing up your data
{: #data-backup}

Your workspace storage is temporary, and it's not intended to be used as the primary storage location for your files. Don't store business-critical or sensitive data in your workspace, and create a backup of your files outside of {{site.data.keyword.cloud-shell_notm}}. You're responsible for your data, and your backup can help you recover in case an outage or data loss occurs for any reason. For more information about how to transfer files to create a backup, see [Transferring multiple files](#transfer-many-files).

## Uploading files
{: #upload-file}

You can upload a file to the root level of your home directory. Only a single file can be uploaded at a time.

1. In the {{site.data.keyword.cloud-shell_notm}} menu bar, click the Upload icon ![Upload icon](../icons/upload.svg).
1. Select the file that you want to upload, and click **Open**.

Your file is uploaded in your home directory, for example `/home/<user-name>/myFile.txt`. You can move or otherwise work with your files by running standard Linux&trade; commands. For example, you can move a `myFile.txt` file that you uploaded to a `myFolder` subdirectory by running the following command.

```bash
mv myFile.txt ./myFolder/
```
{: pre}

Although you can move files, be sure to keep all files in your workspace under your home directory, `/home/<user-name>`. If you move files outside of this directory, it can cause {{site.data.keyword.cloud-shell_short}} to close, which removes your data.
{: tip}

## Downloading files
{: #download-files}

You can download a file from your workspace to your local system. Only a single file can be downloaded at a time.

1. Find the path to the file from the command line by using standard Linux commands.

   For example, you can list all files and subdirectories within your current directory.

   ```bash
   ls -R
   ```
   {: pre}

   Or, you can search for a file name. The following command searches for files with `myFile` in the name.

   ```bash
   find -iname *myFile*
   ```
   {: pre}

1. In the {{site.data.keyword.cloud-shell_notm}} menu bar, click the Download icon ![Download icon](../icons/download.svg).
1. Enter the path to the file in your home directory, such as `/myFolder/myFile.txt`. Click **Continue**.

   Don't include the home directory root `/home/<user-name>` in the file path. File paths are case-sensitive.
   {: tip}

1. Follow your browser prompt to open or save the file to your computer.


## Transferring multiple files
{: #transfer-many-files}

Using the {{site.data.keyword.cloud-shell_short}} UI, you can upload or download only a single file at a time. If you need to transfer many files, it might take a long time to move all of them individually. Instead, use these strategies to efficiently move files between your workspace and another file system.

### Create archives to move files
{: #files-archive}

Before you move files, combine the files into an archive file such as a `.tar`, `.tar.gz`, or `.zip` so that you can move them all at once.

For example, to upload a folder of {{site.data.keyword.cloud_notm}} administration scripts, you might compress them into a `myScripts.zip` file and upload them to {{site.data.keyword.cloud-shell_short}}. In your {{site.data.keyword.cloud-shell_short}} session, you can then run `unzip myScripts.zip` to extract the files.

You can do the same thing in reverse when you want to download files. For example, say you want to back up your entire {{site.data.keyword.cloud-shell_short}} workspace. From your home directory, run `tar -cvf myTar.tar *` to create a `.tar` file (Mac or Linux) or run `zip -r myZip.zip *` to create a `.zip` file (Mac or Windows). Then, download the archive file from {{site.data.keyword.cloud-shell_short}} and extract it on your local system.

### Work from a Git repo
{: #files-clone-git}

For projects in Git repositories, use the {{site.data.keyword.cloud-shell_short}} UI to upload an SSH key so that you can connect to your Git repo. Keep a local copy of your SSH key as a backup. Then, run `git clone` to clone all of the repo's files to your {{site.data.keyword.cloud-shell_short}} workspace. As a bonus, when you commit and push your changes to your Git repo, your changes are automatically backed up to a file system that's outside of {{site.data.keyword.cloud-shell_short}}.
