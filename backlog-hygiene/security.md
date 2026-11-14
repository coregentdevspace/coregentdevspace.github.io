---
title: "Security: Backlog Hygiene for Jira"
permalink: /backlog-hygiene/security
---

# Security: Backlog Hygiene for Jira

Backlog Hygiene for Jira is built by Coregent Digital Studio (Canberra, Australia). This page explains how the app protects your Jira data and how to report a security problem.

## How the app is built

- **Runs on Atlassian.** The app runs only on Atlassian Forge. It has no servers of its own, declares no outbound network access, and sends no data to our servers or to services we contract. It analyses work items with Atlassian's Forge LLMs service, which Atlassian runs on Amazon Bedrock as its sub-processor.
- **AI inside Atlassian.** The AI model is used through Atlassian's Forge LLMs, inside Atlassian's platform. It doesn't use your Rovo credits.
- **We can't see your data.** Coregent Digital Studio does not receive or access your Jira content. App data is stored in Atlassian's Forge hosted storage, which Atlassian encrypts at rest and which supports data residency.
- **Minimum permissions.** The app asks for four scopes: read work items, write work items, app storage, and the site's approximate user count (to set the AI usage limit for your price band). It doesn't read user profiles or attachments.
- **Admins stay in control.** Only Jira administrators can start sweeps, change settings, or approve or reject suggestions. This is checked for the signed-in user on every request. Nothing in Jira changes until an administrator approves a suggestion. Other users can read suggestions only for projects they can browse in Jira.
- **Retention.** Sweep data is kept for the 4 most recent sweeps. When you uninstall, Atlassian deletes the app's storage after 28 days. See the [privacy policy](privacy).

## How we develop it

- Source code is kept in a private repository with two-factor authentication.
- Dependencies are scanned for known vulnerabilities before each release and monitored continuously.
- No secrets, tokens or credentials are stored in the code. The app never asks for passwords or API tokens.
- Logs record run IDs, counts, timings, item keys and errors. The app does not deliberately log work-item text or personal data; error messages are shortened, but could in rare cases include fragments of Jira or AI service responses.

## Reporting a vulnerability

Email **security@coregent.com.au** with a description, steps to reproduce, and the affected site or version. Please don't test against Jira sites you don't own.

We will acknowledge your report within 2 business days and keep you updated. We fix confirmed issues within Atlassian's Marketplace security timelines (for cloud apps: critical within 10 days, high within 4 weeks, medium within 12 weeks, low within 25 weeks).

## If something goes wrong

If we learn of a security incident affecting the app, we will contain it, notify Atlassian within 24 hours, and notify affected customers, where possible within 72 hours, with what happened and what we are doing about it.

## Contact

Security: security@coregent.com.au
Support: support@coregent.com.au
Coregent Digital Studio, Unit 23, 5 Hely Street, Griffith ACT 2603, Australia
