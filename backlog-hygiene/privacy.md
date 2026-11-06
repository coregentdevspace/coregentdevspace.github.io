---
title: "Privacy Policy: Backlog Hygiene for Jira"
permalink: /backlog-hygiene/privacy
---

# Privacy Policy: Backlog Hygiene for Jira

**Effective date:** 6 November 2026  
**Vendor:** Coregent Digital Studio, Unit 23, 5 Hely Street, Griffith ACT 2603, Australia ("we", "us")  
**Contact:** coregent.devspace+privacy@gmail.com

## 1. What this policy covers

This policy explains how the Atlassian Marketplace app **Backlog Hygiene for Jira** (the "App") handles data when it is installed on an Atlassian Jira Cloud site. It does not cover Atlassian's own products or services, which are governed by Atlassian's privacy policy, or the Atlassian Marketplace website.

## 2. Summary

- The App runs entirely on **Atlassian Forge** and is eligible for **Runs on Atlassian**. It has no servers of its own, does not send data outside Atlassian's platform, and uses no third-party services.
- **We (the vendor) have no access to your Jira data.** The App's data lives in Forge app storage on your Atlassian site's installation, and only the App itself can read it.
- The App uses an AI model through **Atlassian's Forge LLMs** service to judge whether work items are duplicates, obsolete or stale. That processing happens on Atlassian's platform.
- **Nothing in Jira changes without approval.** The App writes to Jira only after a Jira administrator approves a suggestion.

## 3. Data the App reads

In the Jira projects that a Jira administrator selects in the App's settings, the App reads:

- for open work items, and for done work items updated in the last 12 months: the key, project, issue type, summary, description, status, created, updated and resolved dates, labels, and links to other work items;
- the last three comments of each work item;
- the project's workflow statuses and the site's resolutions, to offer close settings;
- the list of projects the App can access, to offer project selection.

The App also checks whether the person using its page is a Jira administrator, using Jira's permission check for that person.

The App does not read user profiles, email addresses, attachments, or work items in projects that are not selected.

## 4. Data the App stores, and for how long

The App stores data in **Forge app storage**, which Atlassian hosts as part of the App's installation on your site:

| Data | Purpose | Retention |
|---|---|---|
| A snapshot of the work items read in a sweep (description shortened to 2,400 characters, each comment to 400) | To find and judge candidates during that sweep | The **4 most recent sweeps**; older sweeps are deleted automatically when a new sweep starts |
| Suggestions produced by a sweep (item keys, reason, confidence) | The review queue | The 4 most recent sweeps |
| A short AI-generated summary of each work item, cached until the item changes | To find duplicates worded differently, without re-processing unchanged items | Until the App is uninstalled |
| Cached judgements for pairs or items whose content hasn't changed | To keep weekly sweeps fast and low-cost | Until the App is uninstalled |
| Approve/reject decisions, with the Atlassian account ID of the administrator who made them and the time | To apply approved changes, hide rejected suggestions, and show who decided | Until the App is uninstalled |
| Settings (projects, thresholds, run day, close settings) | To run as configured | Until the App is uninstalled |

When the App is uninstalled, Atlassian deletes its Forge app storage according to Atlassian's platform data-retention policy. Under Atlassian's current documentation, Forge-hosted storage is kept for 28 days after uninstallation, so it can be restored if the App is reinstalled, and is then deleted ([Data lifecycle for Forge-hosted storage](https://developer.atlassian.com/platform/forge/storage-reference/hosted-storage-data-lifecycle/)).

## 5. AI processing

To judge candidates, the App sends work item text (summary, description, recent comments, and the AI summaries above) to an AI model, **Claude Haiku 4.5**, through **Atlassian's Forge LLMs** service. Forge LLMs is part of Atlassian's platform: the request does not go to any server operated by us, and we have no separate contract with an AI vendor for this App.

The AI's output is a suggestion with a reason and a confidence score. It is never applied automatically: a Jira administrator must approve each change. How Atlassian handles and retains these requests is governed by your agreement with Atlassian and [Atlassian's privacy policy](https://www.atlassian.com/legal/privacy-policy).

## 6. Changes the App makes in Jira

Only after a Jira administrator approves a suggestion, the App, acting as the App user, may:

- create an issue link ("duplicates" or "relates to");
- add a comment explaining the change, including details carried over from a duplicate;
- add a label (`hygiene-duplicate`, `hygiene-obsolete` or `hygiene-stale`) when the workflow cannot set a resolution;
- move the work item to a Done status, with the configured resolution where the workflow allows it.

## 7. Personal data

The App processes personal data only to the extent that it appears in:

- **work item text** written by your users (for example a name mentioned in a description or comment), processed as described in sections 3–5;
- **Atlassian account IDs** of administrators who approve or reject suggestions, stored with the decision.

The App does not collect names, email addresses, or other profile data, and does not use data for advertising, profiling, or training AI models.

For the purposes of data protection law, you (the Atlassian customer) are the controller of the data in your Jira site. We do not access or receive the data the App processes: it stays on Atlassian's platform, which processes it under your agreement with Atlassian.

## 8. Logs

The Forge platform records operational logs for the App, such as sweep ids, counts, timings, errors, and the licence mode at the start of a sweep. The App does not deliberately log work item text. Atlassian may make these logs available to us for troubleshooting under Atlassian's terms. Log sharing is on by default for new installations, and a site administrator can turn it off in Atlassian Administration. We use shared logs only to troubleshoot the App.

## 9. Sharing

We do not sell or share your data. The App's data is processed only by Atlassian's platform, as described above. We have no sub-processors for this App other than Atlassian.

## 10. Security

The App relies on Atlassian Forge's security model. Its code runs in Atlassian's sandboxed runtime, and its access is limited to the declared scopes:
- `read:jira-work`
- `write:jira-work`
- `storage:app`

Actions that change Jira, run sweeps, or change settings require Jira administrator permission, checked on every request.

## 11. Your choices

- A Jira administrator can choose which projects the App sweeps, stop weekly sweeps, reject any suggestion, and uninstall the App at any time.
- To ask about this policy or request deletion of App data before uninstalling, contact coregent.devspace+privacy@gmail.com.

## 12. Australian privacy law

We are based in Australia. We handle any personal information we receive (for example, in a support or privacy email) in line with the Australian Privacy Principles in the *Privacy Act 1988* (Cth). If you are not satisfied with our response to a privacy concern, you can contact the Office of the Australian Information Commissioner at [oaic.gov.au](https://www.oaic.gov.au). This policy is governed by the laws of the Australian Capital Territory, Australia.

## 13. Changes to this policy

We will update this policy when the App's data handling changes, and post the new version at this URL with a new effective date. Material changes are also noted in the Marketplace listing's release notes.

## 14. Contact

Coregent Digital Studio  
Unit 23, 5 Hely Street, Griffith ACT 2603, Australia  
coregent.devspace+privacy@gmail.com
