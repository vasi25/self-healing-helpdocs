---
title: Creating Journeys
source: https://help.observepoint.com/en/articles/9101987-creating-journeys
---

# Creating Journeys

*Written by Luiza Gircoveanu · March 25, 2026*

## Overview

Journeys simulate a user interacting with your website's pages, forms, funnels, and more. They report on tags, cookies, console errors, and other data collected. Journeys are used for testing critical paths on a website, such as:

- Testing whether a loan application form captures and submits data correctly
- Validating the functionality of a shopping cart funnel
- Confirming that tags are collecting the right data in a conversion path

## Journey Setup

To create a User Journey, click **Create New → Journey** in the left navbar, then fill out the Journey Setup screen:

**Sub-folder (required)** — The Journey must belong to a sub-folder. Choose one from the list or create a new one.

**Journey Name (required)** — Unique and descriptive of the action it imitates, e.g. "mysite.com Purchase" or "Marketing Lead Form Submission."

**Journey Run Scheduling (required)**

- **Frequency** — How often the Journey should run. Be careful with a higher frequency on low-traffic paths, since your analytics could be skewed — best practice is to allowlist ObservePoint servers or exclude their traffic from analytics. Paused Journeys don't run unless manually activated or the frequency is updated. If a Journey errors out too many times in a row, it pauses automatically.
- **Initial Run Date (required)** — Defaults to the current date; override to start at a future date.
- **Initial Run Time** — Time of day the Journey begins. If a Journey is still running when the next scheduled time passes, the new run is skipped so the current run can finish (and an email is sent suggesting a frequency change). Default time zone is MST, so adjust for your use case.

**File Substitutions** — Test scripts/libraries on production pages without actually inserting them onto the page.

**Location (required)** — Choose where the Journey runs from. In most cases the default location suffices unless you have a geographic or time-zone issue to work around.

**Custom Proxy** — Configure a Journey to run from a specific location not otherwise listed, by entering your own proxy.

**Complete Webhook URL** — A webhook notifies another application when the Journey finishes running. The endpoint must accept HTTP `POST` requests.

**User Agent (required)** — Select the browser/OS the Journey should imitate. Journeys themselves always run on Chrome on Linux; changing the User Agent string only changes what the server sees, not the actual browser or OS. Best practice: copy a Journey and vary the user agent to compare server responses.

**VPN** — If enabled, allows outside access to secure content; must be configured by an administrator and enabled by contract.

**Send Notifications To (optional)** — Email addresses to notify when the Journey fails to complete, or the first time it succeeds after a failure.

**Global Rules (optional)** — A rule applied globally within the Journey only needs to pass once during the run. Rules on a specific step must pass on that step.

**Browser Width Override (optional)** — Viewport width to imitate, matching your chosen user agent's device.

**Email Alerts (optional)** — Notifies listed recipients when the Journey fails, or succeeds after a prior failure.

**Monitor This Journey** — Notifies the Journey Support team to keep an eye on your Journey; ObservePoint will remediate issues within 48 hours. Use descriptive action names for each step to document expected results.

> When Monitor Journey is enabled, the number of requests is reduced when your Journey has an action failure that gets repaired by the Journey Support team.

## Privacy Settings

**Send GPC Signal** — Validates opt-in/opt-out user states required for privacy compliance; report data reflects tags, cookies, and technologies loading while in this state.

**CMP Accept All / Reject All** — Tests the "Accept All" or "Reject All" user states. Configured per domain, set as the first action: navigate to the starting URL, clear cookies, then execute the configured action.

**Block 3rd Party Cookies** — Mimics browsers that block third-party cookies, so you can validate the end-user experience under that condition.

## Setting Up Actions

Actions are commands the Journey executes on web pages to imitate what a user would do. Each Action executes in order and can be rearranged. Identifiers resolve in this order: ID attribute, Name attribute, XPath, CSS selector, HTML.

Action types:

- **Navigate To** — Opens the specified URL; a Journey always starts with a navigation action.
- **Click** — Presses a link or button, located by ID, Name, XPath, or CSS selector.
- **Input** — Enters text into a field, e.g. login credentials.
- **Masked Input** — Like Input, but for passwords/secure text; stored using AES encryption and cannot be viewed later, even by ObservePoint employees.
- **Select** — Clicks a select list item, located by its Value attribute.
- **Check/Uncheck** — Selects or deselects a radio button or checkbox.
- **Execute** — Runs one or more lines of JavaScript (test in the browser console first).
- **Watch** — Pauses for a specified number of seconds, useful for letting a video play before capturing tags.
- **Switch to iFrame / Leave iFrame** — Steps into or out of an iFrame before interacting with elements inside it.
- **Action Set** — Inserts a reusable set of steps from the Action Set Library.
- **Clear all Cookies** — Removes every cookie from the browser up to that point.
- **Consent Manager State (CMP) – Accept All/Reject All**

**Add Action Wait Time (optional)** — Adds delay after an action, useful when a triggered tag (like a form submission) takes time to process. Journey actions don't wait for network silence except for the Navigate action. Standard wait time is 8 seconds per action, and any custom wait time is added on top of that.

**Prevent Nav (optional)** — Stops an action from navigating to its expected destination — useful for recording analytics on a link click (e.g. a download link) without actually loading the destination.

**Rules (optional)** — Apply Rules to each Action to validate data at each step of the Journey.

Once all Actions are configured, click **Save and Finish**.

---

*Mirrored for demo purposes from the [original ObservePoint help article](https://help.observepoint.com/en/articles/9101987-creating-journeys).*
