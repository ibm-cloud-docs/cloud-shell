
---

copyright:
  years: 2020, 2024
lastupdated: "2024-10-23"

keywords: cloud shell activity tracker events, cloud shell event, audit Cloud Shell commands, Cloud Shell logs

subcollection: cloud-shell

---

{{site.data.keyword.attribute-definition-list}}

# Auditing events for {{site.data.keyword.cloud-shell_notm}}
{: #at_events}

As a security officer, auditor, or manager, you can use the {{site.data.keyword.at_full_notm}} service to track how users interact with {{site.data.keyword.cloud-shell_full}}. {{site.data.keyword.cloud-shell_short}} automatically generates events that you can analyze in the {{site.data.keyword.at_short}} service.
{: shortdesc}

{{site.data.keyword.at_short}} records user-initiated activities that change the state of a service in {{site.data.keyword.cloud_notm}}. You can use this service to investigate abnormal activity and critical actions and to comply with regulatory audit requirements. In addition, you can be alerted about actions as they happen. The events that are collected comply with the Cloud Auditing Data Federation (CADF) standard. For more information, see [{{site.data.keyword.at_full_notm}}](/docs/activity-tracker?topic=activity-tracker-getting-started).

## List of events
{: #at_actions}

The following table lists actions in {{site.data.keyword.cloud-shell_notm}} that generate an event.

| Action             | Description       |
| ------------------ | ----------------- |
| `cloudshell.server.create` | An event is generated when a new session is created. |
| `cloudshell.server.configure` | An event is generated when a session is configured. This event is generated for configuring new sessions and reconfiguring an existing session. |
| `cloudshell.server.delete` | An event is generated when a session is deleted. |
| `cloudshell.account-settings.update` | An event is generated when {{site.data.keyword.cloud-shell_short}} settings are updated for an account. |
{: caption="Actions that generate events" caption-side="top"}

## Viewing events
{: #at_ui}

Events that {{site.data.keyword.cloud-shell_short}} generates are automatically forwarded to the {{site.data.keyword.at_short}} service instance that is available in the same location.

{{site.data.keyword.at_short}} can have only one instance per location. To view events, you must access the web UI of the {{site.data.keyword.at_short}} service in the same location where your service instance is available. For more information, see [Launching the web UI through the IBM Cloud UI](/docs/activity-tracker?topic=activity-tracker-launch).

## Analyzing events
{: #at_events_analyze}

{{site.data.keyword.at_short}} events contain fields that describe the action that occurred. Values in the `requestData` and `responseData` fields are specific to {{site.data.keyword.cloud-shell_notm}}, and the other fields are common to all {{site.data.keyword.at_short}} events. For a more information about common fields, see [Event fields](/docs/activity-tracker?topic=activity-tracker-event).

When a user opens, configures, or closes a {{site.data.keyword.cloud-shell_short}} session, the event that is triggered has an `action` field set to `cloudshell.server.create`, `cloudshell.server.configure`, or `cloudshell.server.delete`. The event includes the following fields:

- The `initiator.name` field includes information about the user who interacted with the session.
- The `initiator.id` field shows the IBMid of the user who interacted with the session.
- The `target.id` field includes the Cloud Resource Name (CRN) of the {{site.data.keyword.cloud-shell_short}} account and server where the session was modified, in the format `crn:v1:bluemix:public:cloudshell:<REGION>:a/<ACCOUNT_ID>:<CLOUD_SHELL_SERVER_ID>::`

When a session is successfully opened, configured, or closed, the corresponding event that is generated has an `outcome` that is set to `success` with a 200 `reason.reasonCode`. Otherwise, the event has an `outcome` of `failure` with the appropriate HTTP status code in `reason.reasonCode`, and the `responseData` field contains details about the error.

When an account owner or {{site.data.keyword.cloud-shell_short}} administrator updates the {{site.data.keyword.cloud-shell_short}} settings, the event that is triggered has an `action` field set to `cloudshell.account-settings.update`.
