# DocuSign IAM Transition – Prep Plan

| Field | Details |
| :--- | :--- |
| **Direct Link** | [Claude Doc](https://claude.ai/artifact/QSAtYKptoEP2oxFBKnigzY) |
| **Category** | `docusign` |
| **Tags** | `docusign`, `iam`, `clm`, `esignature`, `sso`, `migration` |
| **Added Date** | 2026-11-04 |

---

## 📌 Overview & Summary

I'm helping with the setup phase only: configuration and access for IAM, and the CLM shutdown. DocuSign PS migrates the contracts from Insight and sets up IAM features. Order: L1 person, then the tech lead, then the call with DocuSign on Thursday.

## 1. L1 Support Person (GITS)

Goal: see what DocuSign looks like from the user side. A quick chat; do it first.

- Which DocuSign tickets come in most often? (login, access requests, missing documents)
- How do new users get access today: a ticket, a request form, or automatically?
- Who do you escalate DocuSign issues to? That's probably the real admin.
- Any recent tickets or questions about CLM? If none, that supports the claim that nobody uses it.
- Is there a knowledge base article or runbook for DocuSign?
- Can you show me a few example tickets?

## 2. Tech Lead (Private Call)

Goal: agree on my role, and get access and the facts about the current setup. If time is short, cover role, admin access and SSO.

**Role and boundaries**

- What exactly do you need from me, and until when?
- Who takes this over once the setup is done?
- What can I decide myself, and what needs your approval?

**Current setup**

- Which identity provider handles SSO for DocuSign? Is our domain claimed in DocuSign Admin?
- How are users provisioned: SSO auto-provisioning, SCIM, or manually?
- Who are the DocuSign admins today?
- Which systems connect to DocuSign (Salesforce, SharePoint, custom apps)? Which API keys or service accounts exist?

**CLM**

- Does anything technical still connect to CLM?
- Is any data in CLM that must be kept before it's shut down?

**Access and Thursday**

- Can you give me admin access to DocuSign Admin, or tell me who can?
- Will you join Thursday's call, or should I go with the question list?

## 3. Call with DocuSign (Thu Nov 5, 10am CT)

The business lead hosts the call. GITS covers configuration and access. If nobody from GITS can join, send these questions ahead of time.

### Account and Licensing

- Will IAM be in the same DocuSign account and organization as our current eSignature setup, or a new one?
- Does the IAM plan replace or sit alongside our eSignature licenses? Will existing eSignature users need new or different seats?
- Will we get a sandbox or test environment before production?

### Identity and Access

- Will our current SSO setup for eSignature (identity provider, claimed domain) also cover IAM, or does it need separate configuration?
- How should users be provisioned: manually, by SSO auto-provisioning, or SCIM? Is that the same as for eSignature?
- What roles and permission profiles does IAM use (for example, for viewing the contract repository)? Who should hold admin rights?
- Which admin access does PS need from us, and for how long?

### Configuration GITS Must Provide

- Give us the full list of tasks PS expects from GITS, with due dates.
- Are there network, firewall, email domain, or DNS changes needed?
- Are integrations planned (for example Salesforce, SharePoint, Microsoft 365)? If so, what API keys, connected apps, or service accounts do we need to create?

### Impact on eSignature

- Will anything change for current eSignature users, templates, envelopes, or integrations during or after the move?
- Is there any planned downtime or cutover window?
- Do any existing API integrations or connected apps need to be reconfigured?

### Insight to IAM Migration (Security Questions)

- How will contract data be extracted from Insight and loaded into IAM? Does any data pass through systems outside DocuSign?
- Where will IAM data be stored (region or data residency)?
- What happens to Insight and its data after migration, and when is Insight turned off?
- Can DocuSign provide security and compliance documents for IAM if our security review needs them?

### CLM Decommission

- What is the process and timeline for shutting down CLM, and when does the CLM license end?
- Is any data left in CLM, and will DocuSign export or delete it? Can we get written confirmation of deletion?
- Are there CLM users, SSO apps, or integration keys we should remove on our side?

### Project Coordination

- Who is our PS contact for configuration and access issues?
- What is the overall timeline and go-live date?
- What support model applies after go-live: DocuSign support, PS, or GITS?

## 4. Learn Before the Calls

About an hour in total, in order of priority. For my role, the video and a look at DocuSign Admin are enough.

1. [Video playlist: Docusign IAM](https://dsucustomers.docusign.com/video-playlist-docusign-iam), about 13 minutes. Start here.
2. [IAM overview blog](https://www.docusign.com/blog/docusign-iam-an-overview-of-intelligent-agreement-management): what the pieces of IAM are.
3. [Docusign Admin product page](https://www.docusign.com/en-ca/products/admin): SSO, SCIM and admin features, which are included in all IAM plans.
4. [Microsoft Entra SSO tutorial for DocuSign](https://github.com/MicrosoftDocs/entra-docs/blob/main/docs/identity/saas-apps/docusign-tutorial.md): only if we use Entra ID. Covers claiming the domain and setting up SSO.
5. [IAM courses at DocuSign University](https://community.docusign.com/tips-from-docusign-155/begin-your-iam-journey-with-docusign-university-24389): for later.

**Hands-on (15 minutes):** get read access to admin.docusign.com and look at the organization, claimed domains, identity providers and linked accounts. Also check the DocuSign app in our identity provider.

**New names you'll hear:** Navigator is now Agreement Manager (the contract repository), and Maestro is now Workflow Builder.
