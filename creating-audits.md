---
title: Creating Audits
source: https://help.observepoint.com/en/articles/9099982-creating-audits
---

# Creating Audits

*Written by Luiza Gircoveanu · October 15, 2025*

![ObservePoint mock logo](/self-healing-helpdocs/assets/op-logo.png)

## Overview

Creating an Audit is simply configuring instructions for ObservePoint to follow. It automates what is traditionally a very tedious manual process of looking at each page and evaluating if all the tags are firing with all the correct variables implemented and set to the correct values. Do this for hundreds of pages and it quickly becomes apparent that an automated Audit is more reliable and faster than any traditional, manual approach.

Setting up an Audit does not require code to be implemented on a page, because when an Audit runs, the ObservePoint servers access pages on your site in a browser window. The ObservePoint tool sits inside the browser, visiting links and monitoring all the tag requests passing data to their collection servers as the pages load.

There are two setups that can be used for creating Audits.

## Simple Setup

This is the simple setup that can be used to create Audits. It needs just a few pieces of information before the Audit can start running:

- **Website URL/domain to Audit** — the URL/domain that has to be visited during the Audit.
- **Location to scan from** — what IP address the servers use to access pages on your site.
- **What you will get** — a brief summary of what you can get with the Simple Setup.

## Advanced Setup

### Scenario tab

Testing scenarios contain specific settings and conditions to ensure an application (in this case, a set of web pages) performs as expected. Several fields are required here to create an Audit:

**Audit Name (required)** — A best practice is using short names and labels to organize your Audits.

**Folder & sub-folder** — You can choose a folder or create a new one. Click the arrow next to the Audit Name field and choose "Add New Folder + Subfolder," then type in a name. The new folder shows up in the Data Sources screen and is available on the folder list inside the Audit setup screen.

**How fast should the Audit go?** — There are 4 different speeds you can set:

- 1 browser
- 5 simultaneous browsers
- 10 simultaneous browsers (default)
- 20 simultaneous browsers — for a faster Audit experience if you've allowlisted ObservePoint IP addresses
- 50 simultaneous browsers — same as above, for even faster completion

> Make sure ObservePoint IP addresses have been allowlisted if you run Audits at 20 or 50 simultaneous browsers. Failure to do so may result in a failed Audit that only reports 429 errors (too many requests) for every page scanned — a common anti-DDOS trigger.
>
> In the Starting URL section, if duplicate URLs are specified, the Audit scans each unique page only once. Subsequent occurrences of the same URL are disregarded to optimize the scanning process. The Audit continues scanning additional pages until reaching the specified limit.

**Location (required)** — Where should the Audit run from? The location determines what IP address the servers use to access pages on your site. Changing this is useful if you have geo-based content or restrictions on your site. By default, the location is set to Oregon, United States (Pacific Time Zone). Most Audits do not need to run from a different location.

**User Agent** — Tells the server what browser and operating system the visitor is using. You can override the default user agent string to see if there are significant changes in how pages are served.

**Browser Width & Height** — Change these to accommodate responsive testing during an Audit.

**Tag Blocking** — Select specific tags or categories of tags to block and effectively disable when the Audit runs. For example, block a Tag Management System tag to see only hard-coded tags, or block A/B testing tags for a more consistent site experience while testing.

**File Substitutions** — Test new files, scripts, and libraries on pages in your production environment before coding the new one onto the page.

**Custom Header Sets** — User-defined HTTP headers automatically included in requests and responses made by ObservePoint during Audits.

**VPN** — If enabled, allows outside access to secure content. Must be configured by an administrator and enabled by contract.

### Privacy settings

**Send GPC Signal** — A critical part of validating the various opt-in/opt-out user states required for privacy compliance. Report data reflects tags, cookies, and other technologies loading while in this state.

**CMP Accept All / Reject All** — Enable this for testing the important user states of "Accept All" or "Reject All." Configured per domain in the Pre-Audit Actions tab as the first action: navigate to the starting URL, clear cookies, then execute the configured action.

**Block 3rd Party Cookies** — Test how your website responds when third-party cookies are blocked, mimicking today's common browser behavior.

### Audit notifications (optional)

Enter as many email addresses as needed to receive alerts when the Audit completes.

## URL Sources Tab

**Which URLs should be used to start the scan?** — The Starting URL field can hold one or more URLs to visit first during the Audit. If the Audit hasn't reached the page limit, it uses include/exclude filters to guide it to additional pages. Use this field to load pages that may not be reachable from links on your site, such as landing pages.

**Maximum pages to be scanned? (required)** — The page limit controls how many pages are scanned during the Audit. Default is 100 pages. Start with a small Audit (10-25 pages) the first few times so you can evaluate quickly whether changes are needed. A best practice is to Audit up to 10,000 pages; usually fewer is enough — auditing beyond that rarely reveals new insight.

> If the number of scanned pages divided by the number of browsers is not bigger than 100, the number of sessions equals the number of browsers.
>
> If the number of scanned pages is lower than the number of browsers, the number of pages equals the number of sessions.

**Find Pages in Sitemaps** — Sitemap scanning helps discover and include pages from sitemaps and robots.txt files, exposing pages not easily discoverable through link crawling.

**De-duplicate URLs** — The Audit will only scan one instance of each page if query strings are used.

**Audit Same URLs** — Ensures the Audit crawls the same URLs as the previous run, eliminating randomness in the crawl to establish a baseline for direct comparison in future runs.

### Advanced URL constraints

You can specify sections of your website to include/exclude using RegEx. The app inserts a default RegEx statement when you enter the starting URL.

### Email Inboxes

Lists any Email Inboxes associated with this Audit test scenario. Audit test scenarios can be assigned to Email Inboxes from the Inbox Library.

This is all you need to set up an Audit — click Save Audit to begin running it automatically.

## Schedule Tab

Schedule when the Audit should run initially and set its frequency. Multiple preset options are available, or you can set a custom frequency at a specific time and date.

## Standards Tab

Lets you assign Alerts, Consent Categories for privacy testing, and pre-built rules — or create new ones on the fly. Rules can look for tags, accounts, and variables on a page, and you can filter which pages a rule runs on by URL, tags found, status codes, and variables.

## Pre-Audit Actions Tab

Lets you set up a login to access secure content, or define other parameters carried through the session, such as setting a language or country cookie. Pre-Audit Actions execute before the starting page(s). If you set up a login, you may also need an Exclude filter to prevent the Audit from executing any logout links.

## On-Page Actions Tab

Actions are steps taken during an Audit to interact with the page the way a user might. Actions can run on every page or only on pages matching specific URL patterns.

Turn on **Prevent Navigation** so the browser doesn't follow through on an action that would:

- Load another page, if doing so would interfere with the flow of the Audit (such as an exit link)
- Load another window or tab — Audits can only work in a single window or tab
- Load a binary file, such as a PDF — Audits can only browse web documents like HTML files

Examples of when you may need an action in an Audit:

- Confirm that a button can be clicked and passes analytics data as expected
- Verify that tags fire as expected on all download links
- Click an exit link to confirm it fires the expected analytics, using Prevent Navigation to capture the analytics without loading the destination page

---

*Mirrored for demo purposes from the [original ObservePoint help article](https://help.observepoint.com/en/articles/9099982-creating-audits).*
