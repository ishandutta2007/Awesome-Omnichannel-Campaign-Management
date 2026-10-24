# Awesome-Omnichannel-Campaign-Management

# Top Omnichannel Campaign Management Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Self-Hosted Customer Journeys, Event-Triggered Messaging & Data Sovereignty*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Omnichannel Campaign Management**. These tools help marketing and product teams orchestrate customer journeys across email, SMS, push, in-app, and messaging channels — with a spectrum running from polished commercial suites to self-hosted platforms that keep customer data on your own infrastructure.

**Examples** include Laudspeaker, Dittofeed, Mautic, Helio, Kling.to, and the commercial platforms (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, event-triggered cross-channel journeys, and unlimited contacts without per-subscriber pricing — ideal for engineering-led teams who want Braze or Customer.io capabilities without sending customer PII to a third party.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Braze** — **The reference cross-channel engagement platform.** Real-time messaging across push, email, SMS, and in-app, with journey orchestration and AI-powered optimization. **Enterprise subscription pricing**. **Best for mobile-first enterprises** needing the most mature cross-channel orchestration and deep SDK integrations, accepting significant cost and data-export requirements .

- **Customer.io** — **The behavioral messaging standard.** Event-triggered emails, SMS, and push based on user activity, with a visual journey builder. **Subscription-based** per-profile pricing. **Best for product-led SaaS teams** wanting sophisticated behavioral triggers without building infrastructure, accepting per-contact costs that scale with growth .

- **Iterable** — **The cross-channel journey platform.** Visual workflow builder for email, SMS, push, and in-app with AI optimization. **Enterprise subscription pricing**. **Best for growth teams** needing deep cross-channel orchestration with a no-code builder .

- **Adobe Campaign** — Enterprise campaign management within Adobe Experience Platform. Cross-channel orchestration with deep Adobe ecosystem integration.

- **Salesforce Marketing Cloud** — Enterprise marketing automation with Journey Builder, email, mobile, and advertising channels.

## Open-Source GitHub Projects

- **Laudspeaker** — **The open-source Braze and Customer.io alternative.** **Y Combinator-backed**, self-hostable or hosted, with **event-triggered cross-channel messages** across email, Slack, SMS, and Firebase push . **No-code journey builder** for creating customer journeys with time delays and time windows for drip campaigns . **User segments** and **database imports** (Postgres, CSV) . **PostHog plugin** for integrating with product analytics . **The honest caveat**: **smaller channel ecosystem than commercial platforms** — SMS is beta, and more channels are planned . **Best for teams wanting a self-hosted Braze alternative** with a journey builder and product analytics integration .

- **Dittofeed** — **The open-source Customer.io and Klaviyo alternative.** **Self-hostable or low-cost cloud**, with **segment-driven automated journeys** built in a visual editor . **Sends templated messages over email, SMS, webhooks, mobile push, and WhatsApp** . **Segments computed from your own event streams** — every user event stays in your infrastructure . **Architecture**: Postgres for app data, ClickHouse for user events and segmentation, Temporal for journey orchestration . **Deployable via Railway** with a lite bundle (API + dashboard + worker in one service) . **The honest caveat**: **ClickHouse is memory-hungry** — give it ~2 GB for comfortable segment computation . **Best for teams wanting a self-hosted Customer.io alternative** with event-driven segmentation and multi-channel messaging .

- **Mautic** — **The veteran open-source marketing automation platform.** GPL-licensed, **40,000+ companies** use it, with **unlimited contacts and campaigns** at flat infrastructure cost . **Full marketing automation**: contacts, segments, newsletters, email campaigns, forms, landing pages, lead scoring, and multi-step campaigns triggered by what contacts do . **Data sovereignty**: use your own database, no vendor lock-in, no per-contact pricing . **Email, SMS, browser and web notifications** out of the box, with a plugin ecosystem for additional channels . **The honest caveat**: **the cron worker is the make-or-break piece** — without it, campaigns silently never send; most self-hosted Mautic failures come from missing cron configuration . **Best for teams wanting a mature, community-owned marketing automation platform** with unlimited contacts and full data ownership .

- **Helio** — **The AI-native, self-hosted growth platform with CDP built in.** **Self-hostable and data-sovereign**, with **Segment/RudderStack-compatible HTTP Tracking API** so existing instrumentation points straight at Helio . **Visual journey builder** (React Flow) generating validated DAGs, with **durable execution on Temporal** that survives crashes . **AI copilot** for drafting segments, journeys, and emails, plus predictive lead scoring and send-time optimization — with bring-your-own AI . **Multi-tenant isolation at the database** via PostgreSQL row-level security . **The honest caveat**: **multi-channel is roadmap, not shipped** — SMS, WhatsApp, and web push are planned; current channels are email and webhooks . **Best for teams wanting a modern, AI-native platform** with Temporal-based durable journeys and existing Segment-compatible instrumentation .

- **Kling.to** — **The self-hosted marketing automation platform for e-commerce.** **No per-contact pricing, no message limits**, with email, SMS, WhatsApp, RCS, and push from one platform . **AI-powered campaign creation** — describe intent ("Email customers who spent over $100 last month with a 15% discount") and Kling builds a ready-to-send campaign . **Visual automation flows** for cart abandonment, welcome series, post-purchase follow-ups, and win-back campaigns . **30+ segmentation filters** including purchase history, predicted lifetime value, and churn risk . **Integrates with Shopify, WooCommerce, BigCommerce, Wix, Magento, Salesforce Commerce, and Square** . **Best for e-commerce teams** outgrowing Klaviyo, Omnisend, or Mailchimp who want self-hosted automation with AI-powered campaign creation .

### Additional Strong Open-Source Options

- **erxes** — **The open-source HubSpot and Qualtrics alternative.** Source-available, self-hosted, with **Team Inbox** (live chat, email, forms), **Sales Management**, **Lead Generation**, **Engage** (email, SMS, messenger), **Contact Management**, and **Knowledgebase** plugins . **Best for teams wanting a combined CRM plus marketing automation platform** with a plugin architecture .

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Omnichannel campaign management tools differ significantly in channel coverage, deployment model, and data ownership. **Laudspeaker and Dittofeed are the closest open-source Braze and Customer.io alternatives** with event-triggered journeys, but **Laudspeaker's SMS is beta** and **Dittofeed requires ClickHouse** (~2 GB RAM) for segmentation . **Mautic is the most mature open-source marketing automation platform** with unlimited contacts, but **its cron worker is essential** — without it, campaigns silently never send . **Helio is AI-native with durable Temporal journeys**, but **multi-channel is roadmap, not shipped** . **Kling.to is e-commerce-focused** with AI campaign creation and platform integrations . **erxes combines CRM and marketing automation** but requires MongoDB, Redis, RabbitMQ, and Elasticsearch . **The choice often comes down to architecture**: do you need a journey builder (Laudspeaker, Dittofeed, Helio), a full marketing suite (Mautic), or e-commerce-specific automation (Kling.to)?
- Self-hosted open-source solutions require proper infrastructure (ClickHouse for Dittofeed, MongoDB stack for erxes, Temporal for Helio), email provider configuration (SMTP or API-based), and awareness that "free" self-hosted still has infrastructure and maintenance costs.

---

**Made for marketing engineers, growth teams, and organizations building omnichannel campaign management platforms they can own and control.**
Let's make omnichannel campaign management more open, data-sovereign, and event-triggered.
