---

copyright:
  years: 2020, 2021
lastupdated: "2021-12-30"

keywords: Cloud Shell preview web app, web preview in Cloud Shell, view port, port preview, app localhost

subcollection: cloud-shell

---

{:external: target="_blank" .external}
{:shortdesc: .shortdesc}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:pre: .pre}
{:screen: .screen}

# Previewing apps
{: #preview-apps}

You can preview apps that are running in {{site.data.keyword.cloud-shell_full}} just like you would if you were running them locally. The {{site.data.keyword.cloud-shell_short}} web preview makes your app UI or endpoint available at a URL that only you can access. This gives you a chance to view changes to your app before you deploy it to a publicly accessible location.
{: shortdesc}

## Before you begin
{: #preview-before-begin}

Enable **Web preview** in the {{site.data.keyword.cloud_notm}} console. For more information about how to enable web preview, see [Enabling or disabling Cloud Shell features for an account](/docs/account?topic=account-shell-settings#shell-features-enable).

## Web preview ports
{: #preview-ports}

You can preview an app by clicking the **Web preview** icon ![Web preview](../icons/view.svg) in the {{site.data.keyword.cloud-shell_short}} menu bar. Web preview is available for any app that listens to HTTP requests on the following ports:
* 3000
* 8080
* 8081
* 8082
* 8083
* 8084
* 9080

As with your local system, only one app can run on each port at any time. If you have multiple apps that are listening on the same port, it results in port conflicts.

## Previewing apps running directly in {{site.data.keyword.cloud-shell_short}}
{: #preview-app}

{{site.data.keyword.cloud-shell_short}} includes lots of [plug-ins, tools, and runtimes](/docs/cloud-shell?topic=cloud-shell-plugins-tools) that you can use to work with apps that you're developing. Because {{site.data.keyword.cloud-shell_short}} storage is temporary, the easiest way to work with an app is to first copy or clone it to your {{site.data.keyword.cloud-shell_short}} workspace, make any changes, and then preview it.

Currently, the {{site.data.keyword.dev_cli_notm}} CLI plug-in (`ibmcloud dev`) can't be used to build, test, or run apps in {{site.data.keyword.cloud-shell_short}}.
{: note}

The following example workflow shows how you can preview a [Node.js Express sample app](https://github.com/IBM/nodejs-express-app){: external} that's hosted in a GitHub repository.

1. In a {{site.data.keyword.cloud-shell_short}} session, clone your app source to your home directory.

    ```bash
    git clone https://github.com/IBM/nodejs-express-app.git
    ```
    {: pre}

    Then, change to the directory where your app was cloned.

    ```bash
    cd nodejs-express-app
    ```
    {: pre}

    At this point, you can make any changes to your app code, such as by using the `vim` text editor.
1. Start your app in {{site.data.keyword.cloud-shell_short}}.

   To start this Node.js sample app, you first need to download any project dependencies.
   ```bash
   npm install
   ```
   {: pre}

   Then, you can start the app so that it's running on a web server in {{site.data.keyword.cloud-shell_short}}.
   ```bash
   npm run start
   ```
   {: pre}

   After the app starts, note the port where your web server is listening. The port must be one of the [available ports](#preview-apps) to be able to preview it in {{site.data.keyword.cloud-shell_short}}. When this sample app starts, it outputs the following information, which shows that it's listening on port `3000`.

   ```text
   > nodejsexpressapp@1.0.0 start /home/my-user-name/nodejs-express-app
   > node server/server.js
   
   App UI available http://localhost:3000
   Swagger UI available http://localhost:3000/swagger/api-docs
   ```
   {: screen}

1. In the {{site.data.keyword.cloud-shell_short}} menu bar, click the **Web preview** icon ![Web preview](../icons/view.svg), and select the port where your server is listening. For the Node.js sample app, select 3000.

   Your web preview opens in a new browser window and shows the equivalent of `http://localhost:3000`. You should see the first screen of your app's UI.

   If you see a message that says there's nothing to preview in {{site.data.keyword.cloud-shell_short}}, the server where your app is running isn't listening on the selected port. Verify that your server is listening on the port that you're previewing, and refresh the preview page.
   {: tip}

Now that you're previewing your app, you can see any changes you make by restarting the app if needed and refreshing the page. Be sure to commit any changes back to your GitHub repo or otherwise download your changes because your workspace storage is temporary.

## Previewing apps running in a Kubernetes pod
{: #preview-kube-cluster}

You can also use {{site.data.keyword.cloud-shell_short}} to preview apps that are running in Kubernetes, such as a Prometheus dashboard or your typical web app. Because apps that are running in a pod in a Kubernetes cluster use an internal port, you need to expose the pod's port either by creating a service or setting up port forwarding.

If you create a service, you need to expose the service publicly, set up authentication to secure access, and set up an application load balancer (ALB) for the service. For more information, see [Connecting applications with services](https://kubernetes.io/docs/concepts/services-networking/connect-applications-service/){: external}.

If you're doing app development and testing, port forwarding is a simpler way to be able to quickly preview apps in your cluster. It requires much less up-front configuration, but you also have to reconfigure it whenever the pod restarts. The following steps walk you through setting up port forwarding and previewing an app that's running in a {{site.data.keyword.containerlong_notm}} cluster.

1. In a {{site.data.keyword.cloud-shell_short}} session, set the cluster where your app is running as the context. This enables you to use `kubectl` commands to work with your cluster.  For more information, see [Configuring the CLI to run `kubectl`](/docs/containers?topic=containers-cs_cli_install#cs_cli_configure).
1. Find the name of the pod where your app is running.

   ```bash
   kubectl get pods
   ```
   {: pre}

   The pod name is listed under the `NAME` column, for example `my-pod-123abc`.

   ```text
   NAME            READY   STATUS    RESTARTS   AGE
   my-pod-123abc   1/1     Running   0          9d
   ```
   {: screen}

1. Find the port in the pod that you want to expose by running the [`kubectl describe`](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#describe){: external} command on the pod.

   ```bash
   kubectl describe pod my-pod-123abc
   ```
   {: pre}

   Under the `Containers` section, the local port is listed as the `Port` value, such as `6000` in the following example.

   ```text
   Containers:
     cluster-agent:
     Container ID:   containerd://1234abcd5678efab90cde603e4ba6986fdaf26daae94c4f309
     Image:          us.icr.io/my-registry/my-image:0.5.0-dev.0.1234
     Image ID:       us.icr.io/my-registry/my-image@sha256:abc123def456abc789def012
     Port:           6000/TCP
     Host Port:      0/TCP
   ```
   {: screen}

1. Set up port forwarding by running the [`kubectl port-forward`](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#port-forward){: external} command. Be sure to select one of the [available ports](#preview-apps) for web preview in {{site.data.keyword.cloud-shell_short}}. 

   For example, the following command listens on port `8080` locally and forwards it to port `6000` within the pod.

   ```bash
   kubectl port-forward pod/my-pod-123abc 8080:6000
   ```
   {: pre}

   Now that port forwarding is set up, you can preview your app.
1. In the {{site.data.keyword.cloud-shell_short}} menu bar, click the **Web preview** icon ![Web preview](../icons/view.svg), and select the port that's being forwarded to your pod.

   Your web preview opens in a new browser window. You should see the first screen of your app's UI.

   If you see a message that says there's nothing to preview in {{site.data.keyword.cloud-shell_short}}, the server where your app is running isn't listening on the selected port. Verify that your server is listening on the pod's internal port and that you're forwarding the port that you're previewing to the correct internal port.
   {: tip}

## Previewing other endpoints on a port
{: #preview-endpoints}

After you open the web preview, you can view any other endpoints that your server is listening for on the same port. The web preview opens at a URL that's the equivalent to `http://localhost:<port>`. To view another endpoint, add the path to the web preview URL.

For example, the Node.js sample app outputs the following URLs:

```text
App UI available http://localhost:3000
Swagger UI available http://localhost:3000/swagger/api-docs
```
{: screen}

To view the Swagger UI, add `/swagger/api-docs` to the web preview URL: 

`https://p3000-abcd1234-ef56-a1b2-b122-a122560ba24f.dp3.us-south.shell.cloud.ibm.com/swagger/api-docs`
