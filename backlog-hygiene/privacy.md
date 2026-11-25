---
title: "Privacy Policy: Backlog Hygiene for Jira"
permalink: /backlog-hygiene/privacy
---

# Privacy Policy: Backlog Hygiene for Jira

**Effective date:** 26 November 2026  
**Vendor:** MD DELOWAR H MUNNA (sole trader) trading as Coregent Digital Studio, ABN 43 843 909 626, Unit 23, 5 Hely Street, Griffith ACT 2603, Australia ("we", "us")  
**Contact:** privacy@coregent.com.au

## 1. What this policy covers

This policy explains how the Atlassian Marketplace app **Backlog Hygiene for Jira** (the "App") handles data when it is installed on an Atlassian Jira Cloud site, and how we handle the limited information that reaches us (logs, support messages, licence and billing information). **We, not Atlassian, are responsible for the App's processing of your data.** Atlassian's own products and the Atlassian Marketplace website are covered by Atlassian's privacy policy.

## 2. Summary

- The App runs on **Atlassian's Forge platform**. We operate no servers for it, and the App sends no data to servers we operate or to any service we contract.
- **We cannot access the data the App stores.** It lives in Forge app storage for your site's installation, hosted by Atlassian.
- To analyse work items, the App uses **Atlassian's Forge LLMs service**, which Atlassian runs on Amazon Bedrock (Amazon Web Services) as Atlassian's sub-processor (section 5).
- We do receive some information directly: operational logs, if your site shares them (section 8); support and privacy messages you send us; and licence and billing information from Atlassian (section 9).
- **Nothing in Jira changes without approval.** The App writes to Jira only after a Jira administrator approves a suggestion.

## 3. Data the App reads

In the Jira projects that a Jira administrator selects in the App's settings, the App reads:

- for open work items, and for done work items updated in the last 12 months: the key, project, issue type, summary, description, status, created, updated and resolved dates, labels, and links to other work items;
- the last three comments of each work item;
- the project's workflow statuses and the site's resolutions, to offer close settings;
- the list of projects the App can access, to offer project selection;
- the site's approximate number of users, to set the App's AI usage limit for your price band (a single number, not personal data).

The App also checks whether the person using its page is a Jira administrator, and which projects they can browse, using Jira's permission checks for that person.

The App does not read user profiles, email addresses, attachments, or work items in projects that are not selected.

## 4. Data the App stores, where, and for how long

The App stores data in **Forge app storage**, which Atlassian hosts as part of the App's installation on your site.

**Where it is stored:** Forge app storage supports Atlassian data residency. If your site uses data residency, the App's stored data is kept in your pinned region. Otherwise the data is in Atlassian's "Global" location: Atlassian assigns it to, and may move it between, its hosting regions, which are listed on Atlassian's data residency page (https://support.atlassian.com/security-and-access-policies/docs/understand-data-residency/).

| Data | Purpose | Retention |
|---|---|---|
| A snapshot of the work items read in a sweep (description shortened to 2,400 characters, each comment to 400) | To find and judge candidates during that sweep | The **4 most recent sweeps**; older sweeps are deleted automatically when a new sweep starts |
| Suggestions produced by a sweep (item keys, reason, confidence) | The review queue | The 4 most recent sweeps |
| A short AI-generated summary of each work item, cached until the item changes | To find duplicates worded differently without re-processing unchanged items | Until an administrator deletes App data, or the App is uninstalled |
| Cached judgements for pairs or items whose content hasn't changed | To keep weekly sweeps fast and low-cost | Until an administrator deletes App data, or the App is uninstalled |
| Approve/reject decisions, with the Atlassian account ID of the administrator who made them and the time | To apply approved changes, hide rejected suggestions, and show who decided | Until an administrator deletes App data, or the App is uninstalled |
| Settings (projects, thresholds, run day, close settings) | To run as configured | Until an administrator deletes App data, or the App is uninstalled |
| The site's approximate user count (one number) | To apply the AI usage limit for your price band | Refreshed at each sweep; deleted with App data, then read again at the next sweep |
| AI usage counters (number of AI requests, tokens and cost per month, and during a trial; no work item content and no personal data) | To enforce the App's AI usage limits | Kept after "Delete app data" so the limits keep working; deleted with the rest of the storage after uninstall |
| A record that App data was deleted (time and number of records) | To show the deletion status and keep usage limits working | As for the usage counters |

**Deleting App data.** A Jira administrator can delete the App's stored data at any time from the App's page (**Delete app data**, confirmed by typing DELETE):

- The App stops any running sweep and deletes the stored data in the background.
- It runs a second check about 15 minutes later, to remove anything written by a step that was already running.
- Sweeps, approvals and settings changes are paused until it finishes, normally within about 20 minutes.
- Only the usage counters and the deletion record above are kept.

It does not remove:
- changes the App already made in Jira with an administrator's approval (links, comments, labels, status changes), which are part of your Jira data and can be edited or removed in Jira;
- operational logs held by Atlassian (section 8);
- data already processed by Atlassian's Forge LLMs service (section 5).

**Uninstalling.** When the App is uninstalled, Atlassian keeps its Forge app storage for 28 days, so it can be restored if the App is reinstalled (on request within 21 days), and then deletes it, together with backups on Atlassian's schedule ([Atlassian's storage documentation](https://developer.atlassian.com/platform/forge/storage-reference/hosted-storage-data-lifecycle/)).

## 5. AI processing

To judge candidates, the App sends work item text (summary, description, recent comments, and the cached AI summaries above) to an AI model from Anthropic's Claude family (currently **Claude Haiku 4.5**), through **Atlassian's Forge LLMs** service. We may move to another Claude model offered through Forge LLMs, for example when Atlassian retires a model; the data sent, the processing path and the protections described in this section stay the same, and this page will name the model in use. Atlassian provides this service using **Amazon Bedrock**, operated by Amazon Web Services as Atlassian's sub-processor. The request does not go to any server we operate, and we have no separate contract with an AI vendor for this App.

- **Location:** Atlassian decides where Forge LLMs processing takes place. It is not covered by data residency, so it may happen outside your site's data residency region.
- **Retention and training:** we do not use your data to train or improve AI models. Atlassian's handling of Forge LLMs requests is governed by Atlassian's terms and policies.
- **Output:** the AI's output is a suggestion with a reason and a confidence score. It is never applied automatically; a Jira administrator must approve each change.

## 6. Changes the App makes in Jira

Only after a Jira administrator approves a suggestion, the App, acting as the App user, may:

- create an issue link ("duplicates" or "relates to");
- add a comment explaining the change, including details carried over from a duplicate;
- add a label (`hygiene-duplicate`, `hygiene-obsolete` or `hygiene-stale`) when the workflow cannot set a resolution;
- move the work item to a Done status, with the configured resolution where the workflow allows it.

## 7. Personal data and our role

The App processes personal data only to the extent that it appears in **work item text** written by your users (for example a name in a description or comment), and in the **Atlassian account IDs** of administrators who approve or reject suggestions.

| Activity | Your role | Our role |
|---|---|---|
| The App reading, storing and analysing your Jira work items (sections 3–6) | Controller | Processor, acting on your configuration and approvals, with Atlassian as our sub-processor |
| Operational logs we view (section 8) | — | Controller, for troubleshooting and improving the App |
| Support, privacy and security messages you send us | — | Controller |
| Licence and billing information Atlassian shares with us (section 9) | — | Controller (Atlassian is a separate controller for billing) |

The App does not collect names, email addresses or other profile data, and we do not use any data for advertising, profiling, or training AI models. Where you need a data processing addendum, see our [Data Processing Addendum](/backlog-hygiene/dpa).

**Sensitive information.** Please don't select projects whose work items contain sensitive information, such as health information, financial account numbers or government identifiers. Your agreement for the App also excludes such data. The App can't detect it in free text, so it would be processed like any other work item text.

## 8. Logs

The Forge platform records operational logs for the App. The App logs:
- sweep and deletion identifiers, counts, timings and errors;
- the licence mode and the site's approximate user count;
- work item keys in some error messages.

It does not deliberately log work item text, names or account IDs. Error messages from Jira or the AI service are logged shortened, and could in rare cases contain fragments of those responses.

Atlassian shares these logs with us by default, and a site administrator can turn log sharing off. We can see shared logs for 30 days, and use them only to troubleshoot and improve the App. Atlassian stores the logs under its own retention policy; they are not covered by data residency.

## 9. Information we receive directly, and sharing

- **Support and privacy messages** you send to support@, privacy@ or security@coregent.com.au: we use them to respond, and keep them for 24 months after the matter is closed unless the law requires longer. These messages are held in Google Workspace (Google LLC), our email provider.
- **Licence and billing information** that Atlassian shares with Marketplace vendors (for example your organisation, site and licence details, and technical or billing contacts): we use it to manage licences, keep business and tax records, and contact you about the App where you've asked us to or the law requires.

We do not sell your data. We share it only with Atlassian, which hosts and runs the App (including Amazon Web Services as Atlassian's sub-processor for Forge LLMs), and where the law requires. Atlassian's sub-processors are listed at https://www.atlassian.com/legal/sub-processors.

## 10. Security

The App relies on Atlassian Forge's security model. Its code runs in Atlassian's sandboxed runtime, declares no outbound network access, and its access is limited to the declared scopes:
- `read:jira-work`
- `write:jira-work`
- `storage:app`
- `read:license:jira` (only the site's approximate number of users, used to set the App's usage limit)

Actions that change Jira, run sweeps, change settings or delete App data require Jira administrator permission, checked on every request.

## 11. Your choices

- A Jira administrator can choose which projects the App sweeps, stop weekly sweeps, reject any suggestion, and uninstall the App at any time.
- A Jira administrator can delete the App's stored data at any time (section 4).
- A site administrator can turn off log sharing in Atlassian Administration.
- To ask about this policy, access or correction of information we hold, or deletion, contact privacy@coregent.com.au.

## 12. Australian privacy law and international transfers

We are based in Australia. Whether or not the Australian Privacy Principles in the *Privacy Act 1988* (Cth) apply to us as a small business, we choose to handle personal information in line with them. Information we receive directly (section 9) and logs (section 8) are accessed by us in Australia. Where data protection law requires a transfer mechanism for personal data from the EEA, UK or Switzerland, we use the European Commission's Standard Contractual Clauses, with the UK International Data Transfer Addendum and Swiss adaptations, as set out in our data processing addendum; Atlassian's processing is covered by Atlassian's own data processing terms. If you are not satisfied with our response to a privacy concern, you may be able to contact the Office of the Australian Information Commissioner at [oaic.gov.au](https://www.oaic.gov.au), or your local data protection authority. This policy is governed by the laws of the Australian Capital Territory, Australia.

## 13. Changes to this policy

We will update this policy when the App's data handling changes, post the new version at this URL with a new effective date, note material changes in the Marketplace listing's release notes, and tell Atlassian as the Marketplace Partner Agreement requires.

## 14. Contact

MD DELOWAR H MUNNA (sole trader) trading as Coregent Digital Studio  
Unit 23, 5 Hely Street, Griffith ACT 2603, Australia  
privacy@coregent.com.au
