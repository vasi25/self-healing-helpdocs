---
title: "Accessibility: Proactively Manage and Resolve Issues"
source: https://help.observepoint.com/en/articles/11084249-accessibility-proactively-manage-and-resolve-issues
---

# Accessibility: Proactively Manage and Resolve Issues

*Written by Product Enablement · December 15, 2025*

![ObservePoint mock logo](/self-healing-helpdocs/assets/op-logo.png)

The Accessibility report empowers teams to monitor accessibility across their entire account, helping them achieve compliance with legal and organizational accessibility standards.

**Features**

- **Flexible exploration** — Easily group, sort, and filter issues by type, WCAG version (e.g., 2.0, 2.1), severity (critical, major, minor), and conformance level (A, AA, AAA).
- **Prioritization tools** — Quickly identify critical issues that may block access for users with disabilities.
- **Proactive insights** — Spot recurring accessibility patterns to address underlying structural or content-related problems.

Below are common jobs that can be accomplished with this report — a subset of what's possible using filters, groupings, and saved views.

## Example reports

**Show me all critical accessibility issues**

- Filter by Impact = Critical
- Group by Issue Type and WCAG Criteria
- Use this to prioritize issues that present major accessibility barriers

**Find all WCAG 2.1 AA specific issues**

- Filter by WCAG Version = 2.1 (inclusive of 2.0)
- Filter by Conformance Level AA (inclusive of A)
- Optionally add an Impact filter to only show Critical issues

**Identify issues across sites**

- Group by Issue Type, then count distinct Pages Affected
- Helpful for identifying template-level or component issues that need upstream fixes
- Add a URL domain grouping to quickly see which sites share common accessibility issues

**Show issues by page type**

- Use page URL patterns or path grouping to isolate issues by microsite, section, or page template

**Find accessibility issues by location**

- If you run scans with geographic targeting or per-market segmentation, group by Audit or location

**Track accessibility fix progress over time**

- Use a Saved View filtered by a specific issue type or severity
- Re-run Audits and track how issue counts change

**Export accessibility issues for engineering or compliance teams**

- Use the Export option to share actionable lists, including metadata like severity, guideline reference, and page URL

## Available data

**Accessibility issues info**

| Name | Description |
| --- | --- |
| Accessibility Issue Type | The type of accessibility problem detected (e.g., missing label, low contrast). |
| Accessibility Issue Description | A brief explanation of the issue and how it may affect users. |
| Accessibility Issue Category | The general category of the issue (e.g., Forms, Color Contrast, Navigation). |
| Accessibility Issue Rule | The specific rule or check that triggered the issue (e.g., aria-roles, color-contrast). |
| WCAG Criteria | The specific WCAG success criterion associated with the issue (e.g., 1.1.1 Non-text Content). |
| Impact | The severity of the issue's impact on users, especially those relying on assistive technologies. |
| WCAG Version | The version of the WCAG standard the issue is mapped to (e.g., WCAG 2.1, 2.2). |
| WCAG Conformance Level | A, AA, or AAA — indicating the strictness of the requirement. |
| Is Manual Inspection Needed | Whether human review is required to confirm or clarify the issue. |
| Failure Summary | An explanation of how the issue can be resolved. |
| Fix One Of | One or more possible fixes — resolving just one may be sufficient. |
| Fix All Of | Required actions where all must be completed to fully resolve the issue. |
| Do Not Of | Actions or patterns the page should avoid (e.g., auto-playing media, using color alone to convey meaning). |
| Accessibility Issue HTML | The HTML snippet where the issue was found. |
| CSS Selectors | The CSS selector(s) identifying the related element(s). |
| Shadow DOM CSS Selectors | The CSS selector(s) locating elements inside a Shadow DOM context. |

**Page info** includes Page ID, Page Title, Page Source Type, Initial/Final Page URL (and their schema, domain, port, fragment, query), status codes, redirect count, load time, page size, visit start/end time, link count, browser errors, failed on-page action count, Core Web Vitals (LCP, FCP, TTFB, CLS), screenshot URL, and scan recency.

**Run properties** include Audit Run ID, run start/end timestamp and date, total pages scanned, whether it's the most recent run, completion status, CMP action status, pre-audit and on-page action status/counts, run duration, and who/what requested the run.

**Audit settings** include Audit ID/Name, page limit, location, labels, simultaneous browsers, browser width/height, starting URLs, page URL filters, schedule, notes, owner, folder/sub-folder, user agent, custom proxy, VPN mode, GPC signal, third-party cookie blocking, blocked technologies, file substitutions, consent categories, webhook, and dedupe/pause settings.

**Email messages** include Email Inbox, Email Subject, and Message Received timestamp, where applicable.

---

*Mirrored for demo purposes from the [original ObservePoint help article](https://help.observepoint.com/en/articles/11084249-accessibility-proactively-manage-and-resolve-issues).*
