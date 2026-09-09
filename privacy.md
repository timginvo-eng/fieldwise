---
title: Privacy Policy — Field Stats
---

# Privacy Policy

**Field Stats**, published by Fieldwise. Last updated 9 September 2026.

## The short version

Field Stats stores nothing. It reads the issues you point it at, adds them up, draws a
chart, and forgets them. Nothing is written to a database, nothing is sent anywhere
outside Atlassian, and no analytics or tracking of any kind is collected.

## Where the app runs

Field Stats is built on Atlassian Forge and runs entirely on Atlassian's own
infrastructure. It has no servers, no database and no external endpoints. Your issue
data never travels to Fieldwise or to any third party, because there is nowhere for it
to travel to.

## What the app reads

The app holds a single Atlassian permission, `read:jira-work`, which lets it read
issues, fields and saved filters. It uses that to:

- list the fields defined on your site, so you can choose one to group by;
- list the saved filters you can already see, so you can choose a source;
- run the filter or query you configured and read only the specific fields the chart
  needs.

Every request is made **as the person viewing the dashboard**, using that person's own
Jira permissions. A gadget can never display an issue the viewer could not already open
in Jira, even if the dashboard is shared widely.

## What the app stores

Nothing. The app does not use Forge storage. Results are calculated when a gadget
renders and discarded when the response is returned. The only thing saved is the gadget
configuration itself, which field to group by and how to measure it. That is stored by
Jira as part of your dashboard, not by us.

## What we can see

Nothing about your data. We have no access to your Jira site, no logs of your issues,
and no telemetry. If you contact support, we see only what you choose to send us.

## Third parties

None. The app loads no external scripts, fonts, analytics or advertising.

## Personal data

The app processes personal data only in the sense that Jira fields such as Assignee
contain names, and those names appear as labels on your own chart. That data is read
from Jira and rendered in your browser. It is never stored or transmitted elsewhere.

## Changes

If this policy changes, the date at the top changes with it, and the current version is
always at this address.

## Contact

Questions about privacy, or a request relating to your data: **timginvo@gmail.com**
