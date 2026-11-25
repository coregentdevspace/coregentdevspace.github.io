---
title: "Data Processing Addendum: Backlog Hygiene for Jira"
permalink: /backlog-hygiene/dpa
---

# Data Processing Addendum: Backlog Hygiene for Jira

**Effective date:** 26 November 2026  
**Provider:** MD DELOWAR H MUNNA (sole trader) trading as Coregent Digital Studio, ABN 43 843 909 626  
**Contact:** privacy@coregent.com.au

## 1. Parties and scope

1.1 This Data Processing Addendum ("DPA") forms part of the agreement under which the customer ("Customer") uses the Atlassian Marketplace app **Backlog Hygiene for Jira** (the "App"): Atlassian's standard Marketplace end user agreement (Bonterms Standard End User Agreement v1.0) together with the Provider-Specific Terms (together, the "Agreement").

1.2 The provider is **MD DELOWAR H MUNNA (sole trader) trading as Coregent Digital Studio**, ABN **43 843 909 626**, Unit 23, 5 Hely Street, Griffith ACT 2603, Australia ("Provider").

1.3 This DPA applies only to Customer Personal Data that the App processes on the Customer's behalf, as described in Annex 1. It does not apply to personal data that Provider processes as a controller for its own purposes (Provider's technical logs and usage data, support correspondence, and licence and billing information received from Atlassian); Provider's privacy policy describes that processing. If Customer Personal Data reaches Provider incidentally, for example in a support message or in an error message in a log, Provider keeps it confidential, uses it only to help the Customer, and deletes it under section 10.4.

1.4 This DPA takes effect when the Customer installs the App and ends when all Customer Personal Data has been deleted under section 10.

## 2. Definitions

"Data Protection Laws" means all laws on the processing of personal data that apply to a party's processing under the Agreement, including, where applicable, the EU General Data Protection Regulation 2016/679 ("GDPR"), the UK GDPR and Data Protection Act 2018, the Swiss Federal Act on Data Protection, and the Australian *Privacy Act 1988* (Cth). "Customer Personal Data" means personal data contained in Customer Data that the App processes on the Customer's behalf, as described in Annex 1. "Customer Data" and "Sensitive Data" have the meanings given in the Agreement. "Controller", "processor", "data subject", "personal data", "personal data breach" and "processing" have the meanings given in the GDPR. "Sub-processor" means a third party engaged by Provider to process Customer Personal Data.

## 3. Roles and the Customer's responsibilities

3.1 The Customer is the controller (or a processor acting for its own controller) of Customer Personal Data. Provider is a processor (or, where the Customer is a processor, a sub-processor).

3.2 Provider processes Customer Personal Data only through the App running on Atlassian's Forge platform. Provider has no technical access to the data the App stores.

3.3 The Customer decides which Jira projects the App processes, and is responsible for having a lawful basis for that processing and for giving any notices its users and data subjects need.

3.4 **Sensitive data.** As the Agreement provides, the Customer will not submit Sensitive Data to the App. The App processes the free text that the Customer's users write into work items in the selected projects; it cannot detect or filter sensitive information in that text. The Customer should not select projects whose work items contain Sensitive Data or other sensitive information (for example health information or government identifiers). If such information is processed anyway, it is processed and deleted in the same way as other Customer Personal Data.

## 4. Instructions

4.1 Provider processes Customer Personal Data only on the Customer's documented instructions. The Agreement, the App's configuration chosen by the Customer's Jira administrators (projects, thresholds, schedule, close settings), and the approval or rejection of individual suggestions are the Customer's complete instructions.

4.2 Provider will tell the Customer if, in its opinion, an instruction infringes Data Protection Laws.

4.3 Provider does not sell Customer Personal Data, use it for advertising or profiling, or use it to train or improve AI models. Atlassian's handling of data sent to Forge LLMs is governed by Atlassian's terms with Provider (Annex 3); Provider makes no commitment on Atlassian's or its sub-processors' behalf.

## 5. Confidentiality

Provider ensures that anyone it authorises to process Customer Personal Data is bound by confidentiality. Today Provider's only personnel is its owner.

## 6. Security

Provider maintains appropriate technical and organisational measures, which at the date of this DPA include those described in Annex 2. Provider may update them, provided the overall level of protection is not materially reduced. Annex 2 describes Provider's measures; it is not "Security Measures" identified under the Agreement. Hosting, storage, runtime and AI-service security are provided by Atlassian under the Forge platform terms.

## 7. Sub-processors

7.1 The Customer authorises the sub-processors listed in Annex 3.

7.2 Provider will give at least 30 days' notice of a new sub-processor engaged by Provider, by updating its privacy policy and the App's Marketplace listing and release notes. Changes to Atlassian's own sub-processors are published by Atlassian at https://www.atlassian.com/legal/sub-processors; Provider will pass on notices it receives from Atlassian as soon as practicable. The Customer may object on reasonable data protection grounds; if the parties cannot resolve the objection, the Customer may stop using the App and uninstall it.

7.3 Provider remains responsible for its sub-processors. Atlassian processes Customer Personal Data for Provider under the Forge Data Processing Addendum, which applies to the provision of the Forge Framework and which Provider accepted with Atlassian's developer terms.

## 8. Data subject requests and assistance

8.1 Provider has no access to Customer Personal Data stored by the App and cannot identify data subjects within it. The Customer can meet most requests itself: by editing or deleting work items in Jira (the App stops processing them at the next sweep and its cached copies are replaced or rotate out), and by using **Delete app data** (section 10.3).

8.2 Provider will forward any request it receives from a data subject about Customer Personal Data to the Customer, and will provide reasonable help with requests, data protection impact assessments and consultations with supervisory authorities, taking into account the nature of the processing and the information available to Provider.

## 9. Personal data breaches

9.1 Provider will notify the Customer without undue delay, and where feasible within 72 hours, after becoming aware of a personal data breach affecting Customer Personal Data, including a breach Atlassian notifies to Provider.

9.2 The notice will describe, as far as known, the nature of the breach, the data and data subjects affected, likely consequences, and the measures taken or proposed. Provider will send it to the Customer's technical or billing contact known to Provider through the Marketplace, or through the Customer's support channel.

## 10. Deletion

10.1 **During use.** The App keeps only the 4 most recent sweeps' item snapshots and suggestions and deletes older ones automatically. AI summaries, cached judgements, decision records and settings are kept until the Customer deletes them (section 10.3) or uninstalls the App.

10.2 **Uninstall.** When the App is uninstalled, Atlassian keeps the App's Forge-hosted storage for 28 days (restorable on request within 21 days) and then deletes it, under Atlassian's data lifecycle for Forge-hosted storage. Backups follow Atlassian's schedule.

10.3 **Delete app data.** A Jira administrator of the Customer's site can delete the App's stored data at any time from the App's page. The App then:
(a) stops any running sweep and refuses new sweeps, approvals, rejections and settings changes until the deletion is finished;
(b) deletes every record it has stored for the site: work item snapshots, AI summaries, cached judgements, suggestions, approve and reject decisions (including administrators' account IDs) and settings;
(c) runs a second deletion pass about 15 minutes later to remove anything written by a processing step that was already running; and
(d) keeps only usage counters (numbers of AI requests and tokens and their cost per month, with no work item content or personal data) and a record of the deletion (timestamps and counts), so that usage limits continue to apply.
This function does not delete: changes already made in Jira with an administrator's approval (issue links, comments, labels and status changes), which are the Customer's Jira data; operational logs held by Atlassian; or data already processed by Atlassian's Forge LLMs service (Annex 3).

10.4 **Provider's records.** Provider has no copy of the App's stored data. Provider deletes Customer Personal Data that reaches it in operational logs or support correspondence in line with its privacy policy, and in any case within 60 days of a request after the Agreement ends, unless the law requires it to be kept.

## 11. Audits and information

11.1 On request, Provider will provide the information reasonably needed to show compliance with this DPA, including its completed security questionnaires and Atlassian's published security and compliance documentation for Forge.

11.2 Because Provider operates no infrastructure of its own, the parties agree that these documents are the primary means of showing compliance. If they are not enough because a supervisory authority requires it, or after a personal data breach affecting Customer Personal Data, the Customer may have an independent auditor, bound by confidentiality, review Provider's relevant records. The Customer must give at least 30 days' notice and pays its own and the auditor's costs. Audits take place no more than once in any 12 months, except where a supervisory authority requires otherwise. Atlassian's platform is covered by Atlassian's own certifications and reports, not by this clause.

## 12. Location and international transfers

12.1 Provider is located in Australia.

12.2 Data the App stores in Forge app storage is held in the location that applies under the Customer's Atlassian data residency settings, where the Customer uses data residency.

12.3 Data the App sends to Atlassian's Forge LLMs service is processed by Atlassian and Amazon Web Services in locations Atlassian determines, which may be outside the Customer's data residency region.

12.4 Atlassian's processing for Provider is covered by the Forge Data Processing Addendum, which incorporates the EU Standard Contractual Clauses (Modules Two and Three), the UK Addendum and Swiss adaptations, and by Atlassian's EU-US, UK and Swiss-US Data Privacy Framework certifications.

12.5 Where Customer Personal Data is transferred to Provider in Australia and a transfer mechanism is required:
(a) for transfers subject to the GDPR, the EU Standard Contractual Clauses (Commission Implementing Decision (EU) 2021/914), Module Two (or Module Three where the Customer is a processor), are incorporated by reference, with the Customer as data exporter and Provider as data importer; clause 7 (docking) does not apply; under clause 9, option 2 (general authorisation) applies, with the notice in section 7.2; the optional wording in clause 11 does not apply; clauses 17 and 18 select the law and courts of Ireland; Annex I is completed by section 1.2 and Annex 1 of this DPA, and Annex II by Annex 2; the competent supervisory authority is the one determined under clause 13;
(b) for transfers subject to the UK GDPR, the UK International Data Transfer Addendum (version B1.0) is incorporated, with its tables completed by the information in (a) and this DPA, and either party may end it as its section 19 allows;
(c) for transfers subject to the Swiss Federal Act on Data Protection, the clauses in (a) apply with references to the GDPR read as references to that Act, and the Swiss Federal Data Protection and Information Commissioner as the competent authority.
If the incorporated clauses conflict with this DPA, the clauses prevail.

## 13. General

13.1 If this DPA conflicts with the Agreement on the processing of Customer Personal Data, this DPA prevails.

13.2 Each party's liability under or in connection with this DPA is subject to the limitations and exclusions of liability in the Agreement, except where Data Protection Laws or the incorporated transfer clauses do not allow it.

13.3 This DPA is governed by the law that governs the Agreement, except where Data Protection Laws or the incorporated transfer clauses require otherwise.

---

## Annex 1: Details of processing (processor activity P1 only)

| Item | Description |
|---|---|
| Subject matter | Finding likely duplicate, obsolete and stale Jira work items, and applying administrator-approved changes |
| Duration | From installation until deletion under section 10 |
| Nature and purpose | Reading work items in the projects the Customer selects; storing snapshots, AI summaries, judgements, suggestions and decisions; sending work item text to an AI model through Atlassian's Forge LLMs service to judge candidates; writing links, comments, labels and status changes to Jira after approval |
| Categories of data subjects | Anyone named or described in work item text (Customer's employees, contractors, its own customers and end users); Jira administrators who approve or reject suggestions |
| Categories of personal data | Personal data that users write into work item summaries, descriptions and the last three comments (for example names, contact details, user reports); Atlassian account IDs of administrators who decide suggestions, with the time of the decision. The App does not read user profiles, email addresses or attachments. |
| Sensitive data | Not intended and excluded by the Agreement (section 3.4). Free text may still contain it if users write it there. |
| Storage | Forge app storage (Key-Value Store) for the Customer's site installation, hosted by Atlassian |
| Retention | Snapshots and suggestions: 4 most recent sweeps. Summaries, judgements, decisions, settings: until Delete app data or uninstall (+28 days). Usage counters: no personal data. |

## Annex 2: Technical and organisational measures

- **Platform:** the App runs only on Atlassian Forge: sandboxed runtime, no Provider servers, no outbound network access (no egress permissions declared in the App's manifest). The App is eligible for Atlassian's "Runs on Atlassian" programme.
- **Least privilege:** scopes are limited to `read:jira-work`, `write:jira-work`, `storage:app` and `read:license:jira` (the site's approximate user count only, to set the usage limit).
- **Access control in the App:** sweeps, settings, approvals, rejections and deletion require Jira administrator permission, checked as the user on every request. The review queue shows a suggestion only if the viewer can browse every project involved.
- **Human approval:** the App changes nothing in Jira until an administrator approves a suggestion.
- **Data minimisation:** only selected projects are read; descriptions are shortened to 2,400 characters and comments to 400 in snapshots; only the last three comments are read; old sweeps are deleted automatically; the App does not deliberately log work item text.
- **Deletion:** Delete app data (section 10.3).
- **Encryption:** provided by Atlassian's Forge platform. Atlassian's Forge shared responsibility model (https://developer.atlassian.com/platform/forge/shared-responsibility-model/, read 2026-11-19) lists among Atlassian's responsibilities: "Encrypt data at rest for data stored within Forge app storage" and "Use TLS to encrypt all traffic, including HSTS." The App stores Customer Personal Data only in Forge app storage, declares no external network access (egress), and Provider holds no encryption keys for it.
- **Provider account security:** two-step verification on the Atlassian, Google and GitHub accounts used to develop and publish the App; full-disk encryption on the development device; dependency alerts in the source repository; `npm audit` clean at release.
- **Vulnerability and incident handling:** published security policy (https://coregentdevspace.github.io/backlog-hygiene/security), reports to security@coregent.com.au, and an internal incident response plan.

## Annex 3: Sub-processors

| Sub-processor | Service | Data | Location |
|---|---|---|---|
| Atlassian (Atlassian Pty Ltd and its affiliates) | Forge hosting and runtime, Forge app storage, Forge logs, Forge LLMs | All Customer Personal Data the App processes | Storage: per the Customer's data residency settings. Runtime: Atlassian aims to run invocations in the host site's location. Forge LLMs and logs: locations Atlassian determines; not covered by data residency. |
| Amazon Web Services, Inc. (Amazon Bedrock), as Atlassian's sub-processor | Hosting of the AI model behind Forge LLMs (listed by Atlassian for Forge as "Generative AI services provider … End User Personal Data processed by Forge Apps") | Work item text sent for judging | As listed by Atlassian for its AWS Bedrock sub-processing (https://www.atlassian.com/legal/sub-processors). |
| Atlassian's other listed sub-processors for Forge | As listed by Atlassian | As listed | https://www.atlassian.com/legal/sub-processors |

The AI model is a model from Anthropic's Claude family (currently Claude Haiku 4.5), developed by Anthropic and made available through Amazon Bedrock. Anthropic is not listed as an Atlassian sub-processor. Moving to another Claude model offered through Forge LLMs does not add or change a sub-processor and does not change the processing described in this DPA; the model in use is named in the privacy policy.
