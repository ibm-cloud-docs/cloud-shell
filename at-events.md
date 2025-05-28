---

copyright:
  years: 2020, 2025
lastupdated: "2025-05-28"

keywords: cloud shell activity tracker events, cloud shell event, audit Cloud Shell commands, Cloud Shell logs

subcollection: cloud-shell

---

{{site.data.keyword.attribute-definition-list}}

# Activity tracking events for {{site.data.keyword.cloud-shell_notm}}
{: #at_events}



{{site.data.keyword.cloud_notm}} services, such as {{site.data.keyword.cloud-shell_notm}}, generate activity tracking events. 
{: shortdesc}

Activity tracking events report on activities that change the state of a service in {{site.data.keyword.cloud_notm}}. You can use the events to investigate abnormal activity and critical actions and to comply with regulatory audit requirements.

You can use {{site.data.keyword.atracker_full_notm}}, a platform service, to route auditing events in your account to destinations of your choice by configuring targets and routes that define where activity tracking events are sent. For more information, see see [About {{site.data.keyword.atracker_full_notm}}](/docs/atracker?topic=atracker-about).

You can use {{site.data.keyword.logs_full_notm}} to visualize and alert on events that are generated in your account and routed by {{site.data.keyword.atracker_full_notm}} to an {{site.data.keyword.logs_full_notm}} instance.

As of 28 March 2024, the {{site.data.keyword.at_full_notm}} service is deprecated and will no longer be supported as of 30 March 2025. Customers will need to migrate to {{site.data.keyword.logs_full_notm}} before 30 March 2025. During the migration period, customers can use {{site.data.keyword.at_full_notm}} along with {{site.data.keyword.logs_full_notm}}. Activity tracking events are the same for both services. For information about migrating from {{site.data.keyword.at_full_notm}} to {{site.data.keyword.logs_full_notm}} and running the services in parallel, see migration planning. 
{: important}

## Locations where activity tracking events are generated
{: #at-locations}



### Locations where activity tracking events are sent to {{site.data.keyword.atracker_full_notm}} hosted event search
{: #at-legacy-locations}



{{site.data.keyword.cloud-shell_notm}} sends activity tracking events to {{site.data.keyword.atracker_full}_notm} hosted event search in the regions that are indicated in the following table.

| Dallas (`us-south`) | Washington (`us-east`)  | Toronto (`ca-tor`) | Sao Paulo (`br-sao`) |
|---------------------|-------------------------|-------------------|----------------------|
| [Yes]{: tag-green} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Americas locations" caption-side="top"}
{: #at-table-1}
{: tab-title="Americas"}
{: tab-group="at"}
{: class="simple-tab-table"}
{: row-headers}

| Tokyo (`jp-tok`)    | Sydney (`au-syd`) |  Osaka (`jp-osa`) | Chennai (`in-che`) |
|---------------------|------------------|------------------|--------------------|
| [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Asia Pacific locations" caption-side="top"}
{: #at-table-2}
{: tab-title="Asia Pacific"}
{: tab-group="at"}
{: class="simple-tab-table"}
{: row-headers}

| Frankfurt (`eu-de`)  | London (`eu-gb`) | Madrid (`eu-es`) |
|---------------------------------------------------------------|---------------------|------------------|
| [Yes]{: tag-green} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Europe locations" caption-side="top"}
{: #at-table-3}
{: tab-title="Europe"}
{: tab-group="at"}
{: class="simple-tab-table"}
{: row-headers}

### Locations where activity tracking events are sent by {{site.data.keyword.atracker_full_notm}}
{: #atracker-locations}



{{site.data.keyword.cloud-shell_notm}} sends activity tracking events by {{site.data.keyword.atracker_full_notm}} in the regions that are indicated in the following table.

| Dallas (`us-south`) | Washington (`us-east`)  | Toronto (`ca-tor`) | Sao Paulo (`br-sao`) |
|---------------------|-------------------------|-------------------|----------------------|
| [Yes]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Americas locations" caption-side="top"}
{: #atracker-table-1}
{: tab-title="Americas"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: row-headers}

| Tokyo (`jp-tok`)    | Sydney (`au-syd`) |  Osaka (`jp-osa`) | Chennai (`in-che`) |
|---------------------|------------------|------------------|--------------------|
| [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Asia Pacific locations" caption-side="top"}
{: #atracker-table-2}
{: tab-title="Asia Pacific"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: row-headers}

| Frankfurt (`eu-de`)  | London (`eu-gb`) | Madrid (`eu-es`) |
|---------------------------------------------------------------|---------------------|------------------|
| [Yes]{: tag-green} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Europe locations" caption-side="top"}
{: #atracker-table-3}
{: tab-title="Europe"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: row-headers}

## Viewing activity tracking events for {{site.data.keyword.cloud-shell_notm}}
{: #at-viewing}



You can use {{site.data.keyword.logs_full_notm}} to visualize and alert on events that are generated in your account and routed by {{site.data.keyword.atracker_full_notm}} to an {{site.data.keyword.logs_full_notm}} instance.

Events that {{site.data.keyword.cloud-shell_short}} generates are automatically forwarded to the {{site.data.keyword.at_short}} service instance that is available in the same location.

### Launching {{site.data.keyword.logs_full_notm}} from the Observability page
{: #log-launch-standalone}



For information on launching the {{site.data.keyword.logs_full_notm}} UI, see [Launching the UI in the {{site.data.keyword.logs_full_notm}} documentation.](/docs/cloud-logs?topic=cloud-logs-instance-launch)


## List of platform events
{: #at_actions_platform}



The following table lists the activity tracking event actions that the {{site.data.keyword.cloud_notm}} platform generates {{site.data.keyword.cloud-shell_short}} instances are processed.

| Action             | Description       |
| ------------------ | ----------------- |
| `cloudshell.server.create` | An event is generated when a new session is created. |
| `cloudshell.server.configure` | An event is generated when a session is configured. This event is generated for configuring new sessions and reconfiguring an existing session. |
| `cloudshell.server.delete` | An event is generated when a session is deleted. |
| `cloudshell.account-settings.update` | An event is generated when {{site.data.keyword.cloud-shell_short}} settings are updated for an account. |
{: caption="Actions that generate platform events" caption-side="bottom"}

## Analyzing {{site.data.keyword.cloud-shell_short}} activity tracking events
{: #at_events_iam_analyze}



{{site.data.keyword.at_short}} events contain fields that describe the action that occurred. Values in the `requestData` and `responseData` fields are specific to {{site.data.keyword.cloud-shell_notm}}, and the other fields are common to all {{site.data.keyword.at_short}} events. For a more information about common fields, see [Audit events](/docs/cloud-logs?topic=cloud-logs-streaming_at_select).

When a user opens, configures, or closes a {{site.data.keyword.cloud-shell_short}} session, the event that is triggered has an `action` field set to `cloudshell.server.create`, `cloudshell.server.configure`, or `cloudshell.server.delete`. The event includes the following fields:

- The `initiator.name` field includes information about the user who interacted with the session.
- The `initiator.id` field shows the IBMid of the user who interacted with the session.
- The `target.id` field includes the Cloud Resource Name (CRN) of the {{site.data.keyword.cloud-shell_short}} account and server where the session was modified, in the format `crn:v1:bluemix:public:cloudshell:<REGION>:a/<ACCOUNT_ID>:<CLOUD_SHELL_SERVER_ID>::`

When a session is successfully opened, configured, or closed, the corresponding event that is generated has an `outcome` that is set to `success` with a 200 `reason.reasonCode`. Otherwise, the event has an `outcome` of `failure` with the appropriate HTTP status code in `reason.reasonCode`, and the `responseData` field contains details about the error.

When an account owner or {{site.data.keyword.cloud-shell_short}} administrator updates the {{site.data.keyword.cloud-shell_short}} settings, the event that is triggered has an `action` field set to `cloudshell.account-settings.update`.
