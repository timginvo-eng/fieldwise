---
title: Security Incident Response Plan — Fieldwise
---

# Security incident response plan

**Fieldwise.** Last updated 9 September 2026. Reviewed annually.

Fieldwise apps run entirely on Atlassian Forge. We operate no servers, no databases and
no external endpoints, and the apps store no customer data. That shapes this plan: the
incidents we can actually have are a vulnerability in our app code, a compromise of a
developer account or workstation, or a supply-chain problem in a dependency.

## Roles and contacts

| Role | Who | Reach them at |
|---|---|---|
| Security contact and incident lead | Tim Ginvo | timginvo@gmail.com, subject line SECURITY |
| Atlassian | Developer and Marketplace Support | ecosystem.atlassian.net, and the Marketplace Security button on any app ticket |
| Customers | Jira administrators of installing sites | Marketplace listing notice and direct email |

The security contact holds an account on `ecosystem.atlassian.net` and monitors it.

## Severity

We use Atlassian's severity levels. **Critical** and **High** findings drive the
timelines in the Marketplace security bug fix policy; **Medium** and **Low** are fixed on
the normal release cycle.

## The steps

**1. Acknowledge.** Any report reaching the security address is acknowledged within two
business days, sooner for anything that reads as Critical.

**2. Triage.** Reproduce the issue against a test Jira site. Establish what data could be
reached, by whom, and whether it has been reached. Record the timeline as it is
established, not from memory.

**3. Contain.** Forge gives two immediate levers. A bad version can be rolled back by
deploying the previous build to production, which reaches every installed site without
customer action. In the worst case the app can be removed from the Marketplace so no
further installs occur.

**4. Notify Atlassian.** For any Critical or High vulnerability, raise it with Atlassian
through the Marketplace Security channel on the app ticket, using Atlassian's app
vulnerability notification template.

**5. Notify customers.** Where customer data could have been exposed, Jira administrators
of affected sites are told what happened, what data was involved, what we have done and
what they should do. We do not wait for a complete picture before saying something is
wrong.

**6. Fix and verify.** Ship the fix, confirm it on a real site, and confirm the
vulnerability is closed rather than moved.

**7. Review.** Write down the cause and the change that stops a repeat. Update this plan
if the incident showed it was wrong.

## What we can reconstruct

The app writes no log statements and stores no data, so there are no application logs of
customer activity to examine, by design. What is available is Forge platform invocation
logs through the Atlassian developer console for their retention window, the app's
deployment and version history, and the change history of our source.

## Reporting a vulnerability to us

Email **timginvo@gmail.com** with SECURITY in the subject. Do not open a public issue.
We will agree a disclosure timeline with you. See the [security policy](./security.html).
