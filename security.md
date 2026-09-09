---
title: Security Policy — Fieldwise
---

# Security Policy

**Fieldwise.** Last updated 9 September 2026.

## Reporting a vulnerability

Email **timginvo@gmail.com** with "SECURITY" in the subject. We aim to acknowledge
within two business days and to agree a disclosure timeline with you. Please do not
open a public issue for a security problem.

## What our apps run on

Every Fieldwise app is built on Atlassian Forge and runs entirely inside Atlassian's
own cloud infrastructure. We operate no servers, no databases and no external
endpoints, so there is no Fieldwise system for an attacker to reach.

## Data handling

- **No storage.** Our apps do not use Forge storage. Results are computed when a
  gadget renders and discarded with the response.
- **No egress.** The app manifest declares no external fetch permissions, so the code
  is not permitted to make outbound requests to any address, including our own.
- **No logging of customer data.** The app writes no log statements.
- **Least privilege.** Field Stats holds a single Atlassian scope, `read:jira-work`,
  and every request is made with the permissions of the person viewing the dashboard.
  A gadget cannot display an issue that viewer could not already open in Jira.

## Platform assurances

Because the app runs on Forge, it inherits Atlassian's infrastructure controls,
tenancy isolation and platform patching. Atlassian publishes those at
[atlassian.com/trust](https://www.atlassian.com/trust).

## If something goes wrong

Our [security incident response plan](./incident-response.html) sets out who leads, how we
contain a problem, and when we tell Atlassian and affected customers.

## Scope and limits

We are a small vendor. We do not currently hold SOC 2 or ISO 27001 certification, and
we do not run a paid bug bounty. We would rather say so plainly than imply coverage we
do not have. If your procurement process needs assurances beyond this page, write to
the address above and we will answer honestly about what we can and cannot provide.
