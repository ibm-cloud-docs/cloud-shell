---

copyright:
  years: 2020, 2022
lastupdated: "2022-02-16"

keywords: cloud shell plug-ins, cloud shell runtimes, cloud shell tools, cloud shell utilities, cli plugins, ibm cloud cli

subcollection: cloud-shell

---

{:shortdesc: .shortdesc}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:important: .important}
{:note: .note}

# Installed plug-ins and tools
{: #plugins-tools}

In addition to the full {{site.data.keyword.cloud}} CLI, {{site.data.keyword.cloud-shell_full}} includes preinstalled CLI plug-ins, packages, tools, and runtimes so that you can instantly get working on the command line.
{: shortdesc}

For more information about the {{site.data.keyword.cloud-shell_notm}} CLI plugins, see [Installing the tools and plug-ins manually](/docs/cli?topic=cli-install-devtools-manually) and [Extending IBM Cloud CLI with plug-ins](/docs/cli?topic=cli-plug-ins).

## {{site.data.keyword.cloud_notm}} CLI plug-ins
{: #installed-plugins}

{{site.data.keyword.cloud-shell_notm}} includes all {{site.data.keyword.cloud_notm}} CLI plug-ins, including but not limited to:

* [{{site.data.keyword.iae_full_notm}} CLI plug-in](/docs/cli?topic=analytics-engine-cli-plugin-CLI_analytics_engine) (`ibmcloud ae`)
* [{{site.data.keyword.cloud_notm}} Catalogs Management CLI plug-in](/docs/cli?topic=cli-manage-catalogs-plugin) ([`ibmcloud catalog`](/docs/cli?topic=cli-ibmcloud_catalog))
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.databases-for}} CLI plug-in](/docs/cli?topic=databases-cli-plugin-cdb-reference) (`ibmcloud cdb`)
* [{{site.data.keyword.codeenginefull_notm}} CLI plug-in](/docs/codeengine?topic=codeengine-cli) (`ibmcloud ce`)
* [{{site.data.keyword.registrylong_notm}} CLI plug-in](/docs/cli?topic=container-registry-cli-plugin-containerregcli) (`ibmcloud cr`)
* [{{site.data.keyword.cloud_notm}} {{site.data.keyword.DRA_short}} CLI plug-in](/docs/cli?topic=devops-insights-cli-plugin-CLI_devops-insights) (`ibmcloud doi`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.openwhisk_short}} CLI plug-in](/docs/cli?topic=cloud-functions-cli-plugin-functions-cli) (`ibmcloud fn`)
* [{{site.data.keyword.cloud_notm}} {{site.data.keyword.ihsdbaas_full}} CLI plug-in](/docs/cli?topic=dbaas-cli-plugin-dbaas_cli_plugin) (`ibmcloud dbaas`)
* [{{site.data.keyword.cis_full_notm}} CLI plug-in](/docs/cli?topic=cis-cli-plugin-cis-cli) (`ibmcloud cis`)
* [{{site.data.keyword.containerlong_notm}} CLI plug-in](/docs/cli?topic=containers-kubernetes-service-cli) (`ibmcloud ks`)
* [{{site.data.keyword.cos_full_notm}} CLI plug-in](/docs/cli?topic=cloud-object-storage-cli-plugin-ic-cos-cli) (`ibmcloud cos`)
* [{{site.data.keyword.satellitelong_notm}} CLI plug-in](/docs/cli?topic=satellite-satellite-cli-reference) [(`ibmcloud sat`](/docs/satellite?topic=satellite-icsat_map))
* [{{site.data.keyword.bplong_notm}} plug-in](/docs/cli?topic=schematics-cli-plugin-schematics-cli-reference) (`ibmcloud schematics`)
* [{{site.data.keyword.tg_full_notm}} CLI plug-in](/docs/cli?topic=tg-cli-plugin-transit-gateway-cli) (`ibmcloud tg`)
* [{{site.data.keyword.vpc_full}} CLI plug-in](/docs/cli?topic=vpc-infrastructure-cli-plugin-vpc-reference) (`ibmcloud is`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.messagehub}} CLI plug-in](/docs/EventStreams?topic=EventStreams-cli_reference) (`ibmcloud es`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.keymanagementserviceshort}} CLI plug-in](/docs/cli?topic=key-protect-cli-plugin-key-protect-cli-reference) (`ibmcloud kp`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSysShort}} CLI plug-in](/docs/cli?topic=power-iaas-cli-plugin-power-iaas-cli-reference) (`ibmcloud pi`)

The {{site.data.keyword.cloud_notm}} CLI and plug-ins are regularly updated to the latest available versions. For the full list of installed plug-ins and their versions, run `ibmcloud plugin list` in {{site.data.keyword.cloud-shell_short}}.
{: tip}

## Tools
{: #installed-tools}

   - Apache Ant (`ant`)
   - Apache Maven (`maven`)
   - Bazaar version control system (`bzr`)
   - Calico CLI (`calicoctl`)
   - cURL (`curl`)
   - etcd CLI (`etcdctl`)
   - FIGlet text banner generator (`figlet`)
   - Git CLI (`git`)
   - GNU Automake (`automake`)
   - GNU Compiler Collection (`gcc`, `gcov`, `gcov-tool`)
   - GNU Wget (`wget`)
   - Gradle CLI (`gradle`)
   - Helm CLI (`helm`)
   - Istio CLI (`istioctl`)
   - jq JSON processor (`jq`)
   - Knative CLI (`kn`)
   - Kubernetes CLI (`kubectl`)
   - Kubetail Kubernetes log aggregator (`kubetail`)
   - Mercurial source content management tool (`hg`)
   - Nano text editor (`nano`) and colors for `nano`
   - nodemon Node.js development monitoring utility (`nodemon`)
   - NPM Package Manager (`npm`)
   - Node Version Manager (`nvm`)
   - Operator SDK (`operator-sdk`)
   - PostgeSQL client (`psql`)
   - Red Hat&reg; OpenShift CLI (`oc`)
   - Red Hat OpenShift Do CLI (`odo`)
   - Redis CLI (`redis-cli`)
   - SoftLayer CLI (`slcli`)
   - Terraform CLI (`terraform`) and {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform  (`ibmcloud terraform`)
   - tmux terminal multiplexer (`tmux`)
   - UnZip extraction utility (`unzip`)
   - Vim text editor (`vim`)
   - XZ Utils (`xz`, `xzcat`, `xzcmp`, `xzdiff`, `xzegrep`, `xzfgrep`, `xzgrep`, `xzless`, `xzmore`)
   - Yarn package manager (`yarn`)
   - yq YAML processor (`yq`)
   - Zip archive utility (`zip`)

## Packages and libraries
{: #installed-packages}

   - `apt-transport-https`
   - `bash-completion`
   - `build-essential`
   - `ca-certificates`
   - `cron`
   - `dnsutils`
   - `gettext`
   - `inetutils-ping`
   - `libevent-dev`
   - `libncurses5-dev`
   - `locales`
   - `musl`
   - `net-tools`
   - `pkg-config`
   - `powerline-shell`
   - Python `requests`
   - `python-virtualenv`
   - `python-setuptools`
   - `python-pip`
   - `python3-pip`
   - `ruby-dev`
   - `silversearcher-ag`
   - `software-properties-common`
   - `zlib1g-dev`

## Programming language runtimes
{: #installed-runtimes}

   - Java&trade; (OpenJDK)
   - Python
   - Ruby
   - Go
   - Node.JS
