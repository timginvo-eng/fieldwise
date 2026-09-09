---
title: Field Stats documentation
---

# Field Stats

A dashboard gadget for Jira Cloud. Point it at a saved filter or a JQL query, group the
matching issues by any field, and measure each group by a count or by the sum, average,
median, minimum or maximum of a numeric field.

- [Install it](#install-it)
- [Add the gadget to a dashboard](#add-the-gadget-to-a-dashboard)
- [The settings](#the-settings)
- [Two fields at once](#two-fields-at-once)
- [Dates](#dates)
- [Copying the numbers out](#copying-the-numbers-out)
- [What each person sees](#what-each-person-sees)
- [Troubleshooting](#troubleshooting)
- [Getting help](#getting-help)

## Install it

A Jira administrator installs the app from the Atlassian Marketplace. The app runs on
Atlassian Forge inside Atlassian's cloud, so there is nothing to host and no account to
create with us.

The app asks for one permission, `read:jira-work`. That is read access to issues,
fields and saved filters. It writes nothing and stores nothing.

## Add the gadget to a dashboard

1. Open the dashboard you want the chart on.
2. Choose **Add gadget**.
3. Find **Field Stats** in the list and add it.
4. The gadget opens straight into its settings. Fill them in and choose **Save**.

To change a chart later, use **Edit** on the gadget.

## The settings

**Issues from** — either **A saved filter**, chosen from the filters you can see, or
**A JQL query** you type yourself, for example `project = ABC AND statusCategory != Done`.

**Group by** — the field that becomes the rows, bars or slices. Every field on your site
is offered, including custom fields, under the name your administrator gave it. Status
category is offered as well as status, so To Do, In Progress and Done roll up without a
separate filter for each status.

**Measure** — what each group is worth:

| Measure | What it does |
|---|---|
| Count of issues | How many issues fall in the group |
| Sum of | Adds up a numeric field, such as story points or time spent |
| Average of | Mean of that field across the group |
| Median of | Middle value, which ignores one huge outlier |
| Minimum of / Maximum of | Smallest and largest value in the group |

Anything but a count asks for a second choice: the numeric field to measure. Story
points, original estimate, time spent and your own number fields all appear here.

**Show as** — Bar (horizontal), Column (vertical), Stacked column, Line, Pie, Donut,
Pivot table, or Single value for one large headline number.

**Sort** — by name, largest first, or smallest first.

**Limit to top** — keeps the chart readable when a field has hundreds of values.

**Include issues with no value** — issues that have nothing in the measured field are
shown as a group called None rather than being counted as zero. Turn it off to leave
them out entirely.

## Two fields at once

**Then split by (optional)** adds a second field. The chart becomes a pivot table with
row totals, or a stacked column chart, depending on what you chose under Show as.
Priority against status, or story points per month by team, are two fields each.

The two fields have to be different. The gadget says so if they are not.

## Dates

Choose a date field under Group by and a **Bucket dates by** setting appears: Day, Week,
Month, Quarter or Year. The time axis stays in date order rather than sorting
alphabetically, so a line chart of points delivered per month reads left to right.

## Copying the numbers out

**Copy CSV** puts the table behind the chart on your clipboard, headers included. Paste
it into a spreadsheet. Pivot tables copy with their row totals.

## What each person sees

Every query runs with the permissions of the person looking at the dashboard. A shared
dashboard can never show someone an issue they could not already open in Jira, so two
people can see different totals on the same gadget. That is the intended behaviour.

## Troubleshooting

**"This site has no numeric fields to measure."** The site has no number fields, or none
that you can see. Count of issues still works. Ask an administrator to check that the
field is a number field and is on a screen you can view.

**A custom field is missing from Group by.** Field lists are read from your own site and
respect your permissions. If you cannot see the field in an issue, the gadget cannot
offer it.

**The chart is empty.** Check that the filter or JQL returns issues when run in the
issue search.

**Totals look low.** Issues with no value for the measured field are grouped under None
rather than counted as zero. The None group holds the difference.

## Getting help

Raise a request in the [support portal](https://timginvo.atlassian.net/servicedesk/customer/portal/1),
or email [timginvo@gmail.com](mailto:timginvo@gmail.com). We aim to reply within two
business days.
