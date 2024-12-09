---

copyright:
  years: 2024
lastupdated: "2024-12-09"

keywords:

subcollection: cloud-shell

---




{{site.data.keyword.attribute-definition-list}}

# Service dependency map for IBM Cloud Shell
{: #service-dependencies}

If a service depends on other {{site.data.keyword.cloud_notm}} services, there can be impacts if any of the dependent services are having issues. The dependency severity indicates the impact to the service when the dependency is down.
{: shortdesc}

Critical
:   When the the dependency is down, the service is down.

Significant
:   When the dependency is down, the service features are impacted.

Medium
:   When the dependency is down, the service might be impacted and a workaround is possible.

Minimal
:   When the dependency is down, the main service features are not impacted.

The following table provides the dependency listing of this service following a standard deployment.


|Dependencies|Dependency impacts|Customer provided|Control or data plane|Location of dependency|
|:---|:---|:---|:---|:---|
|  [IBM Cloud Internet Services](/docs/internet-svcs?topic=internet-svcs-service-dependencies)  | Availability, Change management, Disaster recovery, Security compliance | No | Both |  Same region  |
|  [IBM Cloud Virtual Servers](/docs/classic-virtual-servers?topic=classic-virtual-servers-service-dependencies)  | Availability, Change management, Disaster recovery | No | Both |  Same region  |
|  [IBM Cloud Identity and Access Management](/docs/overview?topic=overview-service-dependencies)  | Availability, Change management, Security compliance | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  [IBM Cloud Kubernetes Service and Red Hat OpenShift on IBM Cloud - containers-kubernetes](/docs/containers-kubernetes?topic=containers-kubernetes-service-dependencies&interface=ui)  | Availability, Change management, Disaster recovery | No | Both |  Same region  |
|  [IBM Cloud Bare Metal](/docs/classic-bare-metal-servers?topic=classic-bare-metal-servers-service-dependencies)  | Availability, Change management, Disaster recovery | No | Both |  Same region  |
|  Akamai  | Availability, Change management, Disaster recovery | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  [IBM Cloud Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-service-dependencies)  | Availability, Change management, Disaster recovery, Security compliance | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  [IBM Cloud Databases - databases-for-etcd](/docs/databases-for-etcd?topic=databases-for-etcd-service-dependencies&interface=ui)  | Availability, Change management, Disaster recovery | No | Both |  Same region  |
|  [IBM Cloudant for IBM Cloud - cloudantnosqldb](/docs/cloudantnosqldb?topic=cloudantnosqldb-service-dependencies&interface=ui)  | Availability, Change management, Disaster recovery, Security compliance | No | Both |  Same region  |
|  [IBM Cloud Classic DNS Servers](/docs/classic-external-dns?topic=classic-external-dns-service-dependencies)  | Availability, Change management | No | Both |  Same data center  |
|  IBM Cloud Classic Infrastructure Resource Management  | Availability, Change management | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  IBM Cloud Public IP Address Management  | Availability, Change management | No | Both |  Same region  |
|  [IBM Cloud Console](/docs/overview?topic=overview-service-dependencies)  | Availability, Operations | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  [IBM Cloud Databases - databases-for-redis](/docs/databases-for-redis?topic=databases-for-redis-service-dependencies&interface=ui)  | Availability, Change management, Disaster recovery | No | Both |  Same region  |
{: row-headers}
{: caption="IBM Cloud Shell service dependency information - Critical dependencies" caption-side="top"}
{: tab-title="Critical dependencies"}
{: tab-group="service-dependency-data-for-cloudshell"}
{: class="comparison-tab-table"}
{: #critical-deps}
{: summary="Use the buttons for the dependency level to change the context of the table. This table has row and column headers. The row headers details about the dependency. The column headers identify the dependency. To understand the details about each dependency, navigate to the row to find the depedency that you need more information about interested in."}

|Dependencies|Dependency impacts|Customer provided|Control or data plane|Location of dependency|
|:---|:---|:---|:---|:---|
|  [IBM Cloud Container Registry](/docs/Registry?topic=Registry-service-dependencies)  | Availability, Change management, Disaster recovery, Security compliance | No | Both |  Same region  |
|  Synthetics  | Availability, Operations | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  [IBM Key Protect for IBM Cloud](/docs/key-protect?topic=key-protect-service-dependencies)  | Availability, Change management, Disaster recovery, Security compliance | No | Both |  Same region  |
|  [IBM Cloud Classic NTP Servers](/docs/classic-external-ntp?topic=classic-external-ntp-service-dependencies)  | Availability, Change management | No | Both |  Same data center  |
|  [IBM Cloud Activity Tracker event routing](/docs/atracker?topic=atracker-service-dependencies)  | Availability, Operations, Security compliance | No | Both |  Same region  |
|  [IBM Cloud Business Support Services](/docs/overview?topic=overview-service-dependencies)  | Availability | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  [IBM Cloud Global Resource Catalog](/docs/overview?topic=overview-service-dependencies)  | Availability, Change management | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  Let's Encrypt  | Availability, Change management, Security compliance | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  [IBM Log Analysis Log Routing](/docs/logs-router?topic=logs-router-service-dependencies)  | Availability, Operations, Security compliance | No | Both |  Same region  |
|  [IBM Cloud Metrics Routing](/docs/metrics-router?topic=metrics-router-service-dependencies)  | Availability, Operations | No | Both |  Same region  |
|  [IBM Cloud Monitoring](/docs/monitoring?topic=monitoring-service-dependencies)  | Availability, Operations | No | Both |  Same region  |
|  [IBM Cloud Secrets Manager](/docs/secrets-manager?topic=secrets-manager-service-dependencies)  | Availability, Change management, Disaster recovery, Security compliance | No | Both |  Same region  |
|  IBM Cloud Service Endpoints  | Availability, Change management, Disaster recovery | No | Both |  Same region  |
|  Segment  | Availability | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
{: row-headers}
{: caption="IBM Cloud Shell service dependency information - Significant dependencies" caption-side="top"}
{: tab-title="Significant dependencies"}
{: tab-group="service-dependency-data-for-cloudshell"}
{: class="comparison-tab-table"}
{: #significant-deps}
{: summary="Use the buttons for the dependency level to change the context of the table. This table has row and column headers. The row headers details about the dependency. The column headers identify the dependency. To understand the details about each dependency, navigate to the row to find the depedency that you need more information about interested in."}

|Dependencies|Dependency impacts|Customer provided|Control or data plane|Location of dependency|
|:---|:---|:---|:---|:---|
|  [IBM Cloud CLI ](/docs/cli?topic=cli-service-dependencies)  | Change management | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  TaaS Tekton Runners  | Change management, Security compliance | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
{: row-headers}
{: caption="IBM Cloud Shell service dependency information - Medium dependencies" caption-side="top"}
{: tab-title="Medium dependencies"}
{: tab-group="service-dependency-data-for-cloudshell"}
{: class="comparison-tab-table"}
{: #medium-deps}
{: summary="Use the buttons for the dependency level to change the context of the table. This table has row and column headers. The row headers details about the dependency. The column headers identify the dependency. To understand the details about each dependency, navigate to the row to find the depedency that you need more information about interested in."}

|Dependencies|Dependency impacts|Customer provided|Control or data plane|Location of dependency|
|:---|:---|:---|:---|:---|
|  Amplitude  | Operations | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  SOS Inventory Management  | Security compliance | No | Both |  ibm-intranet  |
|  SOS Compliance Reporting  | Security compliance | No | Both |  ibm-intranet  |
|  SOS SIEM  | Security compliance | No | Both |  ibm-intranet  |
|  SOS Tenable  | Security compliance | No | Both |  ibm-intranet  |
|  SOS Health-Check, Vulnerability Scanning and Patching  | Security compliance | No | Both |  ibm-intranet  |
|  [IBM Cloud Global Search and Tagging](/docs/overview?topic=overview-service-dependencies)  | Security compliance | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
|  [IBM Log Analysis & IBM Cloud Activity Tracker](/docs/cloud-logs?topic=cloud-logs-service-dependencies)  | Operations, Security compliance | No | Both |  Same region  |
|  OSS Platform  | Operations | No | Both |  [Global](https://cloud.ibm.com/docs/overview?topic=overview-zero-downtime#global-platform)  |
{: row-headers}
{: caption="IBM Cloud Shell service dependency information - Minimal dependencies" caption-side="top"}
{: tab-title="Minimal dependencies"}
{: tab-group="service-dependency-data-for-cloudshell"}
{: class="comparison-tab-table"}
{: #minimal-deps}
{: summary="Use the buttons for the dependency level to change the context of the table. This table has row and column headers. The row headers details about the dependency. The column headers identify the dependency. To understand the details about each dependency, navigate to the row to find the depedency that you need more information about interested in."}

This table can be used to answer the following questions:

- **What is the expected impact to the functions described?** Each severity tab in the table indicates the impact that your provisioned service might encounter if the dependency were to go offline. This means that the dependency high availability and disaster recovery influences the severity of the impact and therefore is used for general guidance to help you understand potential issues that might arise if the dependency was impacted by an incident.

   Services that are regional are not impacted by a severe outage of a single availability zone because of the failover that is built in to default to another zone. For these occurrences, there might be a slight performance impact, if any, while the system fails over to the other location. This also applies to global services where the impact is lowered even more as it can fail over to other regions if necessary. This reduces the frequency at which these items might have the impact that is shown.
   {: note}

- **What services does my service depend on?** The Dependencies column lists the services. These are the major service to service dependencies including major internal dependencies that might not be visible externally. If you select the dependency service, you are directed to more information about the dependencies of that service.

   Additional information is available only for the catalog services. Internal services do not have links to more information.
   {: note}

- **What function does the dependency impact?** Functions include access management, availability, change management, configuration management, customer responsibility, disaster recovery, instance control, none, operations or security compliance. If the dependency goes offline, these functions might be impacted. Definitions for each available values are as follows:

   access management
   :   Authentication, authorization and governance of the customer users access to the service and service instances.

   availability
   :   Availability of the service and service instances.

   change management
   :   Deployment, upgrade, patch, etc. of the service and service instances.

   configuration management
   :   Deployment, upgrade, patch, etc. of the service and service instances.

   customer responsibility
   :   Functions provides by customers to support specific service and service instances function. E.g. Key Protect instances provided by customer to support service BYOK encryption.

   disaster recovery
   :   Backup, recovery, restart of the service and service instances in case of disruption.

   instance control
   :   Creation, deletion, start, stop, etc. actions on lifecycle of the service instances.

   none
   :   No function impacted.

   operations
   :   Monitoring, troubleshooting, etc of the service and service instances.

   security compliance
   :   Vulnerability management and other security and compliance management of the service and service instances.

- **Where do dependency services need to be deployed with regard to my service?** In the Location of dependency column you can view if the dependency is located in the same region or deployed to a specific data center. You can use this data with the data in the Control or data plane column for a quick reference to identify if your data leaves the region or not in a standard setup.

   To find where your service can be deployed, see [Service and infrastructure availability by location](/docs/overview?topic=overview-services_region).

   The table shows a standard cloud deployment. If a special deployment is used like Fedramp or other region-bound deployment models, the data might differ from the details available in the table. Refer to the specific deployment that you are using for that information.
   {: note}

- **Where are the separate control plane and data plane located, if applicable?** In some cases, the dependency might have a separate control plane and data plane. In these cases, there are separate lines that show the location in relation to the deployed customer instance of the service where these will be provisioned. The lines might have different impacts and different functions. See the Control or data plane column to understand what possible impact this type of outage might have.

   Same region means that the dependent services are in the same region as the provisioned instance. Other values might show data center or region names if the service must be used from a specific region, a specific availability zone, or set of availability zones. If a service is tied to a specific region or site, and the region goes offline, the service might go offline as well. It is recommended that you go through the high availability and disaster recovery documentation of the dependency to determine if there are any steps that you should take to mitigate these types of risks.


For more information about the policies that are related to the services, you can refer to the following resources:

* [Service Level Agreement](https://www.ibm.com/support/customer/csol/terms/?id=i126-6605&lc=en){: external}
* [Shared responsibilities for using {{site.data.keyword.cloud_notm}} products](/docs/overview?topic=overview-shared-responsibilities)
* [Service and infrastructure availability by location](/docs/overview?topic=overview-services_region)
