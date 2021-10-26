---
copyright:
  years: 2021
lastupdated: "2021-09-29"

keywords: security and compliance for IBM Cloud Shell, security for IBM Cloud Shell, compliance for IBM Cloud Shell, rules for IBM Cloud Shell

subcollection: cloud-shell

---

{:external: target="_blank" .external}
{:note: .note}
{:term: .term}
{:shortdesc: .shortdesc}
{:table: .aria-labeledby="caption"}


# Managing security and compliance with {{site.data.keyword.cloud-shell_notm}}
{: #manage-security-compliance}

{{site.data.keyword.cloud-shell_full}} is integrated with the {{site.data.keyword.compliance_short}} to help you manage security and compliance for your organization.
{: shortdesc}

With the {{site.data.keyword.compliance_short}}, you can monitor for controls and goals that pertain to {{site.data.keyword.cloud-shell_notm}}.

## Monitoring security and compliance posture with {{site.data.keyword.cloud-shell_notm}}
{: #monitor-cloudshell}

As a security or compliance focal, you can use the {{site.data.keyword.cloud-shell_notm}} [goals](#x2117978){: term} to help ensure that your organization is adhering to the external and internal standards for your industry. By using the {{site.data.keyword.compliance_short}} to validate the resource configurations in your account against a [profile](#x2034950){: term}, you can identify potential issues as they arise.

To start monitoring your resources, check out [Getting started with {{site.data.keyword.compliance_short}}](/docs/security-compliance?topic-security-compliance-getting-started).

### Available goals for {{site.data.keyword.cloud-shell_short}}
{: #cloudshell-available-goals}

* Check whether {{site.data.keyword.cloud-shell_short}} is enabled in account settings
* Check whether {{site.data.keyword.cloud-shell_short}} has one or more locations enabled in account settings
* Check whether {{site.data.keyword.cloud-shell_short}} has the file upload and download features enabled in account settings
* Check whether {{site.data.keyword.cloud-shell_short}} has the web preview feature enabled in account settings

## Governing {{site.data.keyword.cloud-shell_short}} resource configuration
{: #govern-cloudshell}

As a security or compliance focal, you can use the {{site.data.keyword.compliance_short}} to define configuration rules for {{site.data.keyword.cloud-shell_short}}.

[Config rules](#x3084914){: term} are used to enforce the configuration standards that you want to implement across your accounts. To learn more about the about the data that you can use to create a rule for {{site.data.keyword.cloud-shell_short}}, review the following table.

| Resource kind | Property | Operator | Value | Description |
|---------------|----------|---------------|-------|-------------|
| service | enabled | is_true  \n is_false | - | Indicates whether access to {{site.data.keyword.cloud-shell_short}} is allowed for an account. |
{: caption="Table 1. Rule properties for {{site.data.keyword.cloud-shell_short}}" caption-side="top"}

To learn more about formatting config rules, check out [Formatting rules and templates](/docs/security-compliance?topic=security-compliance-formatting-rule-templates).
