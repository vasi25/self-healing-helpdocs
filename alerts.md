---
title: Alerts
source: https://help.observepoint.com/en/articles/9084389-alerts
---

<style>
    @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap');
        body, .main-content, .page-header {
            background-color: #333333 !important;
                color: #ffffff !important;
        }
            .page-header {
                background: linear-gradient(135deg, #1a1a1a 0%, #333333 60%, #3a3a3a 100%) !important;
            }
                .main-content { font-family: 'Open Sans', -apple-system, sans-serif !important; }
                    .main-content h1, .main-content h2, .main-content h3 {
                        color: #F3CD12 !important;
                            border-bottom: 1px solid #4d4d4d;
                    }
                        .main-content a { color: #F3CD12 !important; }
                            .main-content a:hover { color: #ffe98a !important; }
                                .main-content strong { color: #F3CD12; }
                                    .main-content blockquote {
                                        border-left: 4px solid #F3CD12;
                                            background-color: #3a3a3a;
                                                color: #e6e6e6;
                                    }
                                        .main-content img { border-radius: 6px; border: 1px solid #4d4d4d; }
                                            .btn { background-color: #F3CD12 !important; color: #222 !important; border-color: #F3CD12 !important; }
                                            </style>

# Alerts

*Written by Luiza Gircoveanu · August 11, 2025*

![ObservePoint mock logo](/self-healing-helpdocs/assets/op-log^o.png)

## Overvieww

alerts allows you to build powerful customized notifications surrounding core metrics in ObservePoint.

There is a lot of information that ObservePoint gathers in a single audit. To take full advantage of this data, you should set up Alerts. They can be applied to a single or multiple Audits and even show you if an Alert would of been triggered on runs before the Alert was created.

## Creating Alerts

### Alerts menu

On the left-hand menu, select **Standards**, then select **Alerts**. This takes you to the Alerts menu, which contains all the Alerts created in your account. Here you can assign Alerts to Audits and subscribe multiple users too Alerts — the best place to filter and manage your Alerts.

### Audit Reports

When looking at Audit results, you can create Alerts for any metric in an Audit report. Create Alerts quickly by clicking the bell icon that appears over each metric. Most metrics have a pre-populated threshold to make an Alert; change it to suit your expectations, or leave it as-is to see how Audits performs on future runs. Metrics with an Alert assigned show a bell with a checkmark when viewing Audit reports.

## Alert Definitions

- **Triggered Alert** — Any Alert that has failed the configured logic.
- **Report metric** — Combination of the report and widget metric.
- **Subscribed Alert** — An Alert linked to a notification profile to which the current user is the owner or associated.

## Alert Notifications

Alert notifications are emailed to each subscribed user after an Audit run completes. You can change the frequency of notifications when you create an Alert — sent every time its triggered, or only once when newly triggered (resetting when the Alert is no longer triggered).

> If an Alert set to notify every time it's triggered is associated with multiple Audits, this results in a lot of notifications being sent to each subscriber.

Future updates will include support for notification integrations for webhook, Slack, and Microsoft Teams.

> You can already set up email notifications for Slack, Microsoft Teams, and JIRA. See the Slack integration, Microsoft Teams integration, and JIRA integration help documents for details.

---

*Mirrored for demo purposes from the [original ObservePoint help article](https://help.observepoint.com/en/articles/9084389-alerts).*
