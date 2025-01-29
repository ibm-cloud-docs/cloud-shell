---

copyright:
  years: 2020, 2025
lastupdated: "2025-01-29"

keywords: cloud shell plug-ins, cloud shell runtimes, cloud shell tools, cloud shell utilities, cli plugins, ibm cloud cli

subcollection: cloud-shell

---

{{site.data.keyword.attribute-definition-list}}

# Installed plug-ins and tools
{: #plugins-tools}

In addition to the full {{site.data.keyword.cloud}} CLI, {{site.data.keyword.cloud-shell_full}} includes preinstalled CLI plug-ins, packages, tools, and runtimes so that you can instantly start working on the command line.
{: shortdesc}

For more information about the {{site.data.keyword.cloud-shell_notm}} CLI plug-ins, see [Extending IBM Cloud CLI with plug-ins](/docs/cli?topic=cli-plug-ins).

## {{site.data.keyword.cloud_notm}} CLI plug-ins
{: #installed-plugins}

{{site.data.keyword.cloud-shell_notm}} includes all {{site.data.keyword.cloud_notm}} CLI plug-ins, including but not limited to:

* [{{site.data.keyword.at_full_notm}} CLI plug-in](/docs/cli?topic=cli-activity-tracker-cli) (`ibmcloud atracker`)
* [{{site.data.keyword.iae_full_notm}} CLI plug-in](/docs/cli?topic=cli-CLI_analytics_engine) (`ibmcloud ae`)
* [{{site.data.keyword.appconfig_notm}} CLI plug-in](/docs/app-configuration-cli-plugin?topic=app-configuration-cli-plugin-app-configuration-cli) (`ibmcloud ac`)
* [{{site.data.keyword.cloud_notm}} Catalogs management CLI plug-in](/docs/cli?topic=cli-manage-catalogs-plugin) (`ibmcloud catalog`)
* [{{site.data.keyword.IBM_notm}} Context-based restrictions CLI plug-in](/docs/cli?topic=cli-cbr-plugin) (`ibmcloud cbr`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.databases-for}} CLI plug-in](/docs/cli?topic=cli-cdb-reference) (`ibmcloud cdb`)
* [{{site.data.keyword.cloudant_short_notm}} CLI plug-in](/docs/cli?topic=cli-cloudant-cli) (`ibmcloud cloudant`)
* [{{site.data.keyword.codeenginefull_notm}} CLI plug-in](/docs/cli?topic=cli-cli) (`ibmcloud ce`)
* [{{site.data.keyword.IBM_notm}} Code Risk Analyzer CLI plug-in](/docs/cli?topic=cli-cra-cli-plugin) (`ibmcloud cra`)
* [{{site.data.keyword.registrylong_notm}} CLI plug-in](/docs/cli?topic=cli-manage-catalogs-plugin) (`ibmcloud cr`)
* [{{site.data.keyword.cloud_notm}} {{site.data.keyword.DRA_short}} CLI plug-in](/docs/cli?topic=cli-CLI_devops-insights) (`ibmcloud doi`)
* [{{site.data.keyword.IBM_notm}} Direct Link CLI plug-in](/docs/cli?topic=cli-dl-cli) (`ibmcloud dl`)
* [{{site.data.keyword.en_full_notm}} CLI plug-in](/docs/cli?topic=cli-event-notifications-cli) (`ibmcloud event-notifications`)
* [{{site.data.keyword.dns_full_notm}} CLI plug-in](/docs/cli?topic=cli-dns-services-cli-commands) (`ibmcloud dns`)
* [{{site.data.keyword.cloud_notm}} {{site.data.keyword.ihsdbaas_full}} CLI plug-in](/docs/cli?topic=cli-dbaas_cli_plugin) (`ibmcloud dbaas`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.hscrypto}} CLI plug-in](/docs/cli?topic=cli-hpcs-cli-plugin) (`ibmcloud tke`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.hscrypto}} Certificate manager CLI plug-in](/docs/cli?topic=cli-hpcs-cli-plugin#cert-manager-cli-plugin) (`ibmcloud hpcs-cert-mgr`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.hpvs}} CLI plug-in](/docs/cli?topic=cli-hpvs_cli_plugin) (`ibmcloud hpvs`)
* [{{site.data.keyword.cis_full_notm}} CLI plug-in](/docs/cli?topic=cli-cis-cli) (`ibmcloud cis`)
* [{{site.data.keyword.containerlong_notm}} CLI plug-in](/docs/cli?topic=cli-kubernetes-service-cli) (`ibmcloud ks`)
* [{{site.data.keyword.monitoringlong_notm}} (ibmcloud monitoring) CLI plug-in](/docs/cli?topic=cli-monitor-cli) (`ibmcloud monitoring`)
* [{{site.data.keyword.cos_full_notm}} CLI plug-in](/docs/cli?topic=cli-ic-cos-cli) (`ibmcloud cos`)
* [{{site.data.keyword.IBM_notm}} Power Systems Virtual Server CLI plug-in](/docs/power-iaas-cli-plugin?topic=power-iaas-cli-plugin-power-iaas-cli-reference) (`ibmcloud pi`)
* [{{site.data.keyword.pag_full_notm}} CLI plug-in](/docs/privileged-access-gateway?topic=privileged-access-gateway-pag-cli-commands) (`ibmcloud gateway`)
* [{{site.data.keyword.satellitelong_notm}} CLI plug-in](/docs/satellite?topic=satellite-satellite-cli-reference) [(`ibmcloud sat`](/docs/satellite?topic=satellite-icsat_map))
* [{{site.data.keyword.bplong_notm}} CLI plug-in](/docs/cli?topic=cli-manage-catalogs-plugin) (`ibmcloud schematics`)
* [{{site.data.keyword.secrets-manager_full_notm}} CLI plug-in](/docs/secrets-manager?topic=secrets-manager-secrets-manager-cli) (`ibmcloud secrets-manager`)
* [{{site.data.keyword.tg_full_notm}} CLI plug-in](/docs/cli?topic=cli-transit-gateway-cli) (`ibmcloud tg`)
* [{{site.data.keyword.vpc_full}} CLI plug-in](/docs/cli?topic=cli-vpc-reference) (`ibmcloud is`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.messagehub}} CLI plug-in](/docs/EventStreams?topic=EventStreams-cli_reference) (`ibmcloud es`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.keymanagementserviceshort}} CLI plug-in](/docs/cli?topic=cli-key-protect-cli-reference) (`ibmcloud kp`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSysShort}} CLI plug-in](/docs/cli?topic=cli-power-iaas-cli-reference) (`ibmcloud pi`)
* [{{site.data.keyword.vpc_short}} CLI plug-in](/docs/cli?topic=cli-vpc-reference) (`ibmcloud vpc-infrastructure`)
* [{{site.data.keyword.IBM_notm}} {{site.data.keyword.dv_short}} CLI plug-in](/docs/watson-query-cli-plugin?topic=watson-query-cli-plugin-CLI-name) (`ibmcloud watson-query`)

The {{site.data.keyword.cloud_notm}} CLI and plug-ins are regularly updated to the latest available versions. For the full list of installed plug-ins and their versions, run `ibmcloud plugin list` in {{site.data.keyword.cloud-shell_short}}.
{: tip}

## Tools
{: #installed-tools}

   - Apache Ant (`ant`)
   - Apache Maven (`maven`)
   - Bazaar version control system (`bzr`)
   - Calico CLI (`calicoctl`)
   - cURL (`curl`)
   - Docker (`docker`)
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
   - Simple Python Version Management (`pyenv`)

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
