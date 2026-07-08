—————---
title: Audit Summary Report
source: https://help.observepoint.com/en/articles/9084064-audit-summary-report
---

# Audit Summary Report

*Written by Luiza Gircoveanu · June 19, 2024*

![ObservePoint mock logo](/self-healing-helpdocs/assets/op-logo.png)

## Overview

The Audit Summary report allows users to see a high-level summary of Audit results, but also drill down into other reports with filters specific to the desired insights. This report also helps you to focus in on the Primary Tags that you have identified in your account. When you open up the report you'll see the details of your Audit.

**Recommended actions**

- **Identify trends** — Use trending spark lines to pick out big changes in the number of tags, the number of broken tags, and the number of broken pages to get a sense of your site performance.
- **Primary tags** — Use primary tags to keep track of the tags that are most important for you to maintain across your entire site. Get a quick snapshot of their presence and performance.
- **Jump into reports** — Use the Audit Summary Report to pick out quick points of interest for both your site and specific tags, then jump straight into that report to review the details of that information.

## Audit Summary

The top-level summary metrics will display:

- How many pages were scanned
- How many of your primary tags were present
- How many rules were applied

## Audit Score

A single score summarizing overall Audit health.

## Tech Validation

This section of the report displays:

- The status of the applied rules
- Total number of unique tags
- Total number of broken tags
- Total number of broken final pages

**Identify trends** — Spot check these reports for any surprising changes. When checking an Audit you should check these trends to see if there have been spikes in rule failures, drops or sudden increases in the number of tags, or increases in the number of broken tags or pages.

Data is displayed as trending behavior. Click on individual trending lines to see more of your previous runs. You should use these trends to identify big changes in the behavior of your site. If you suddenly see many more tags appearing you should check that all the tags look familiar to you or that increase is expected. Similarly, you might use the trend of broken pages or broken tags to track down trouble.

> You can click on the graphs to expand those trending lines, and you can also click on any of these statistics. When you click on those numbers, you'll get the option to jump directly into a report of that data already filtered to what you are looking at.

### Privacy Validation

If you have applied Consent Categories to your Audit, then this section will display in your Summary report. You can also see mentioned the number of Consent Categories applied to your Audit and you can expand the section to see what Category was assigned.

The metrics in this section include:

- Pages With Unapproved Cookies
- Unapproved Cookies
- Pages With Unapproved Tags
- Unapproved Tags
- Pages With Unapproved Request Domains & Geos
- Unapproved Request Domains & Geos

## Health of Primary Tags

This table will have a breakdown of the tags you have configured as Primary Tags. It displays basic summaries of the health and implementation scope of these tags. These summary metrics include:

- The % of pages scanned that collected the tag
- The average tag load time
- The % of successful and unsuccessful status codes
- Any of your primary tags that were **not** found in the scan will also be identified

**Primary tags** — These tags should be the tags that you expect to see across 100% of your site. It's a way of getting quick information on your Analytics Tag, your Tag Manager, your Data Layer, etc.

This is a great way of checking for the tags that are most important to **you**. Here you can quickly see the implementation of your analytics tag, if it's present on all pages and how well it's behaving.

> You may need to adjust which tags are your Primary Tags — that's easy to do from this report. Simply hover over one of the present tags, then select the option to Edit Primary Tags in Tag Setup. From there simply toggle on or off the tags you want, or use the search bar to find and add a tag you don't see.

## Detected Tags

The bottom table is a list of all the tags detected across the Audit and some statistics on their behavior, including:

- The number of pages tagged
- The number of pages not tagged
- The average tag load time
- The number of unique tag accounts
- The number of unique variables

By clicking on any cells in this table, you can drill into another report filtered for the insight you selected (e.g. clicking on the load time for a tag would open the Tag Health report filtered to that tag). You can sort any of these columns by clicking on them. Use this table to quickly spot check your tags or quickly find information about a specific tag you're looking for.

**Jump into reports** — Audits have a lot of information in their reports; use the Audit Summary report as a means of jumping into data that is most interesting to you. Either dive into the trending data or use the list of Detected Tags to investigate a specific tag that is interesting to you. Almost every piece of information will lead you into another report and filter that information for you.

---

*Mirrored for demo purposes from the [original ObservePoint help article](https://help.observepoint.com/en/articles/9084064-audit-summary-report).*
