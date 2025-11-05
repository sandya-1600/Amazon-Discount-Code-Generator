# Amazon Discount Code Generator

Automate the creation of Amazon promotional codes, coupons, and percentage-off vouchers across multiple marketplaces and accounts. This system removes repetitive Seller Central workflows, enforces guardrails, and outputs ready-to-share codes with usage limits and schedules. Expect fewer clicks, fewer mistakes, and faster go-to-market for your Amazon campaigns — all powered by Android automation.

<p align="center">
  <a href="https://Appilot.app" target="_blank"><img src="media/appilot-baner.png" alt="Appilot Banner" width="100%"></a>
</p>
<p align="center">
 <a href="https://t.me/devpilot1" target="_blank"><img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"></a>
 <a href="mailto:support@appilot.app" target="_blank"><img src="https://img.shields.io/badge/Email-support@appilot.app-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"></a>
 <a href="https://appilot.app" target="_blank"><img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website"></a>
 <a href="https://discord.gg/r5sJ5vhf" target="_blank"><img src="https://img.shields.io/badge/Join-Appilot_Community-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Appilot Discord"></a>
</p>

<p align="center"> 
   Created by Appilot, built to showcase our approach to Automation!<br>
   <strong>If you are looking for custom Amazon Discount Code Generator, you've just found your team — Let’s Chat.👆👆</strong>
</p>

## Introduction
**What it does:** Automates end-to-end creation of Amazon coupon/promo codes (e.g., Money Off, Percentage Off, Single-Use, Multi-Use) in Seller Central, including targeting, budget capping, and scheduling.  
**Problem it solves:** Manual creation is slow and error-prone — especially at scale across marketplaces and multiple brands.  
**Benefit:** Launch promotions faster, stay compliant with marketplace rules, and standardize settings for reliable results.

### Automating Multi-Marketplace Promo Operations
- Creates single-use and multi-use codes in batches with configurable redemption limits and start/end dates.
- Applies ASIN targeting from CSV/Google Sheets and validates eligibility before submission.
- Enforces standardized naming, budgets, and policy guardrails to avoid accidental overspend.
- Supports multi-account rotation with isolated sessions, proxies, and human-like timings.
- Generates exportable audit logs and code lists for your CRM, Klaviyo, or influencer programs.

## Core Features

- **Real Devices and Emulators:** Works on physical Android phones/tablets and Android emulators (Bluestacks, Nox). Device-farm ready for parallel promo creation.
- **No-ADB Wireless Automation:** Headless, ADB-less control via Accessibility + input bridges to minimize detection and keep devices fully wireless.
- **Mimicking Human Behavior:** Randomized delays, scroll paths, viewport jitter, and OCR-assisted element matching to reduce bot fingerprints.
- **Multiple Accounts Support:** Segregated profiles, cookies, and session vault; marketplace-aware configs (US, UK, DE, etc.) with per-brand templates.
- **Multi-Device Integration:** Distribute promo jobs across 10–300 devices with queue-based load balancing and throttling per account.
- **Exponential Growth for Your Account:** Rapid promo iteration and distribution that accelerates coupon campaigns, influencer drops, and seasonal pushes.
- **Premium Support:** SLA-backed assistance, onboarding playbooks, and help with marketplace nuances and safe scaling.
- **Template-Driven Promo Builder:** Save reusable policy-compliant templates (naming, discount type, budget cap, targeting rules).
- **Eligibility & Policy Checks:** Pre-flight validation for ASIN eligibility, category constraints, min price/quantity, and conflict detection.
- **Audit & Reporting:** Structured logs (JSON/CSV) with promo IDs, code ranges, redemption caps, and creation status for compliance.

## Additional Feature Set

| Feature | Description |
|---|---|
| Batch Code Generation | Create thousands of single-use codes per campaign with segmented prefixes for influencers, affiliates, or email cohorts. |
| CSV/Sheets Import | Load ASINs, discounts, and timing from CSV or Google Sheets; field mapping UI and schema validation built-in. |
| Proxy & Profile Isolation | Integrate static/mobile proxies and per-account device profiles (WebView/App caches) to minimize cross-account leakage. |
| Scheduler & Retry Queue | Time-based triggers, exponential backoff, and idempotent retries for flaky Seller Central steps. |
| Webhooks & Exports | Push created codes to webhooks/REST endpoints and export reports to CSV/JSON for BI tools. |
| Notifications | Slack/Discord alerts on job start/finish, error spikes, or approval holds. |

</p>
<p align="center">
  <a href="https://appilot.app" target="_blank">
    <img src="media/amazon-discount-code-generator-banner.png" alt="amazon-discount-code-generator-architecture" width="95%">
  </a>
</p>

## How It Works 
1. **Input or Trigger** — The automation is triggered from the Appilot dashboard where you select the target account(s), upload ASIN lists, choose template (discount type, budget, dates), and set job size/parallelism.  
2. **Core Logic** — Appilot drives the Android Seller Central app/web via UI Automator/Appium/Accessibility to navigate Promotions → Create, fills fields (name, products, budget, dates), attaches code rules, and submits for review.  
3. **Output or Action** — The system returns created promo identifiers and (if applicable) the generated discount codes, exports CSV/JSON, and triggers optional webhooks to your CRM or affiliate manager.  
4. **Other functionalities** — Robust retry logic, screenshot-on-failure, device rotation, rate limiting, per-step timeouts, and detailed logging are managed centrally in the Appilot dashboard.

## Tech Stack
- **Language:** Kotlin, Java, Python, JavaScript  
- **Frameworks:** Appium, UI Automator 2, Espresso, Robot Framework, Cucumber  
- **Tools:** Appilot, Android Debug Bridge (ADB), Appium Inspector, Bluestacks, Nox Player, Scrcpy, Firebase Test Lab, MonkeyRunner, Accessibility  
- **Infrastructure:** Dockerized device farms, Cloud-based emulators, Proxy networks, Parallel Device Execution, Task Queues, Real device farm

## Directory Structure
```
amazon-discount-code-generator/
│
├── src/
│ ├── main.py
│ ├── appilot_jobs/
│ │ ├── promo_builder.py
│ │ ├── asin_validator.py
│ │ ├── scheduler.py
│ │ ├── exporters/
│ │ │ ├── csv_exporter.py
│ │ │ └── webhook_publisher.py
│ │ └── utils/
│ │ ├── logger.py
│ │ ├── proxy_manager.py
│ │ ├── device_pool.py
│ │ └── config_loader.py
│ ├── android/
│ │ ├── uiactions.kt
│ │ ├── selectors.json
│ │ └── accessibility/
│ │ └── event_hooks.kt
│ └── webview/
│ ├── appium_caps.json
│ └── gestures.yaml
│
├── config/
│ ├── settings.yaml
│ ├── templates/
│ │ ├── percentage_off.yaml
│ │ ├── money_off.yaml
│ │ └── single_use_codes.yaml
│ ├── marketplaces.yaml
│ └── credentials.env
│
├── data/
│ ├── input/
│ │ ├── asins.csv
│ │ └── campaigns.xlsx
│ └── output/
│ ├── created_codes.csv
│ └── promo_report.json
│
├── logs/
│ ├── run.log
│ └── device/
│ └── device-001.log
│
├── tests/
│ ├── unit/
│ │ └── test_validator.py
│ └── integration/
│ └── test_full_flow.robot
│
├── docker/
│ ├── Dockerfile
│ └── compose.yaml
│
├── requirements.txt
└── README.md
```


## Use Cases
- **Amazon agencies** use it to generate single-use discount codes for influencer drops, so they can attribute sales by cohort with minimal manual work.  
- **Brand owners** use it to launch multi-market coupons simultaneously, so they can standardize budgets and reduce setup errors.  
- **Growth teams** use it to prepare seasonal promotions in batches, so they can ship thousands of codes with controlled redemption caps.  
- **Marketplace ops** use it to enforce policy-safe templates, so they can prevent accidental overspend and maintain compliance.

## FAQs
**How do I configure this automation for multiple accounts?**  
Define accounts in `config/credentials.env` and attach marketplace settings in `config/marketplaces.yaml`. The runner spins up isolated device profiles with per-account proxies and queues jobs to avoid overlap.

**Does it support proxy rotation or anti-detection?**  
Yes. You can assign static/mobile proxies per account and enable randomized timings, scroll jitter, and OCR-assisted selectors to mimic natural behavior. Profiles/caches are isolated per device.

**Can I schedule campaigns to start/stop automatically?**  
Use the built-in scheduler. Set `start_at`/`end_at` in your template or upload timing columns in your CSV; the queue will dispatch tasks and pause/resume as configured.

**What inputs are required for batch code generation?**  
At minimum: ASINs, discount type/amount, code type (single/multi), budget cap, and dates. Optional fields include marketplace, naming template, prefix, and per-segment redemption limits.

**How are results exported?**  
Created promotions and code lists are written to `data/output/` (CSV/JSON) and can be sent to webhooks (e.g., CRM, email service, affiliate manager).

## Performance & Reliability Benchmarks
- **Execution Speed:** ~250–600 promo steps/hour per device depending on marketplace latency and discount type; horizontal scaling near-linearly with more devices.  
- **Success Rate:** **95%** end-to-end under normal network conditions with retries enabled.  
- **Scalability:** Validated on **50–300** concurrent Android instances; architecture supports bursts toward **1000** with tuned queues and proxy pools.  
- **Resource Efficiency:** Lightweight workers (<250MB RAM per emulator avg.), adaptive timeouts, and capped CPU usage per device for predictable density.  
- **Error Handling:** Exponential backoff, step-level idempotency, screenshot/DOM snapshots on failure, Slack alerts, and automatic reruns for transient errors.

##
<p align="center">
<a href="https://cal.com/app-pilot-m8i8oo/30min" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
</p>
