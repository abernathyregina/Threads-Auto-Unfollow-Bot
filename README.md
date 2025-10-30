# Threads Auto Unfollow Bot

Automate the cleanup of your Threads following list with safe, human-like Android interactions. This Threads Auto Unfollow Bot streamlines account hygiene by unfollowing inactive, bot-like, or non-engaging profiles at scale—without risking bans due to sloppy automation. The result: healthier follower/following ratios, improved feed quality, and better account trust.
<p align="center">
  <a href="https://Appilot.app" target="_blank">
    <img src="media/appilot-baner.png" alt="Appilot Banner" width="100%">
  </a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20Appilot%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:support@appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Email-support@appilot.app-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

<p align="center"> 
   Created by Appilot, built to showcase our approach to Automation!<br>
   <strong>If you are looking for custom Threads Auto Unfollow Bot, you've just found your team — Let’s Chat.👆👆</strong>
</p>

## Introduction
This system automates unfollow actions on Threads from real Android devices or emulators, executing safe, human-like interactions across multiple accounts. It removes manual tedium, enforces per-account safety rules, and keeps your following list clean using filters (inactive, no-mutuals, no-engagement, risk-flags).

### Automating Threads Unfollow Management
- Targets non-engaging or high-risk profiles using smart filters (no mutuals, low interaction score, age/inactivity thresholds).
- Enforces granular safety policies: daily/ hourly caps, random delays, jitter, and break windows to mimic real usage.
- Operates across multi-device farms with proxy isolation, rotating fingerprints, and per-account profiles.
- Full observability: live run-logs, screenshots on action, and error-aware retries with backoff.

## Core Features
- **Real Devices and Emulators:** Works with physical Android phones/tablets and emulator stacks (Bluestacks/Nox/Firebase Test Lab) for true app-level behavior and better anti-detection resilience.
- **No-ADB Wireless Automation:** Control devices over Wi-Fi via Appilot’s non-ADB channel, reducing ADB artifacts while preserving input precision (taps, swipes, text).
- **Mimicking Human Behavior:** Randomized scroll speeds, dwell times, gesture variance, and micro-pauses; night/quiet hours; action jitter to avoid obvious patterns.
- **Multiple Accounts Support:** Isolated profiles, cookies, and storage per account with individual schedules, limits, and rule sets.
- **Multi-Device Integration:** Queue-driven orchestration to fan out workloads across 10–1000+ devices with per-device proxy and health checks.
- **Exponential Growth for Your Account:** By pruning low-value followings, improve follow-back quality, engagement rate, and algorithmic trust over time.
- **Premium Support:** Priority onboarding, device-farm sizing guidance, and escalation SLAs for production incidents.

## Additional capabilities:

| Feature | Description |
|---|---|
| **Smart Filters & Scoring** | Score candidates by inactivity, no-mutuals, recent interactions, private/public status, and risk heuristics before unfollowing. |
| **Scheduler & Queue** | CRON-like schedules with a work queue; throttling by account, device, and IP to keep actions within safe boundaries. |
| **Proxy & Fingerprint Isolation** | Per-account mobile/residential proxies and device fingerprint isolation (Multilogin/AdsPower-style profiles) to minimize linkage. |
| **Rules Engine** | YAML/JSON policies for caps, cooldowns, blackout windows, and conditional logic (e.g., skip verified or recent followers). |
| **Observability & Alerts** | Structured logs, action screenshots, metrics, and webhook/Telegram/Discord alerts on anomalies. |
| **Safe Retry & Backoff** | Idempotent retries with exponential backoff; circuit-breaker when the app rate-limits or UI states change. |

</p>
<p align="center">
  <a href="https://appilot.app" target="_blank">
    <img src="media/threads-auto-unfollow-bot-banner.png" alt="threads-auto-unfollow-bot-architecture" width="95%">
  </a>
</p>

## How It Works
1. **Input or Trigger** — From the Appilot dashboard, select accounts/devices, define filters (inactive/no-mutuals), and set schedules (daily windows, action caps).
2. **Core Logic** — Appilot drives the Threads app via UI Automator/Appium to open the following list, evaluate each profile against rules, and execute unfollow with human-like gestures and pacing.
3. **Output or Action** — The bot unfollows selected profiles, records proofs (timestamps, screenshots, profile IDs), and emits metrics/webhooks for downstream systems.
4. **Other functionalities** — Automatic retries, circuit-breakers on repeated failures, structured logging, rollup reports, and parallel processing across devices with per-IP isolation.

## Tech Stack
- **Language:** Kotlin, Java, Python, JavaScript/TypeScript  
- **Frameworks:** Appium, UI Automator, Espresso, Robot Framework, Cucumber  
- **Tools:** Appilot, Android Debug Bridge (ADB), Appium Inspector, Bluestacks, Nox Player, Scrcpy, Firebase Test Lab, MonkeyRunner, Accessibility  
- **Infrastructure:** Dockerized device farms, Cloud emulators, Residential/Mobile proxies, Parallel Device Execution, Task Queues, Real device farm

## Directory Structure
```
threads-auto-unfollow-bot/
│
├── src/
│ ├── main.py
│ ├── automation/
│ │ ├── device_controller.py
│ │ ├── threads_actions.py
│ │ ├── filters.py
│ │ ├── scheduler.py
│ │ ├── workers/
│ │ │ ├── queue_worker.py
│ │ │ └── metrics_exporter.py
│ │ └── utils/
│ │ ├── logger.py
│ │ ├── proxy_manager.py
│ │ ├── fingerprint_profile.py
│ │ ├── config_loader.py
│ │ └── safe_retry.py
│ ├── kotlin/
│ │ └── DeviceService.kt
│ └── java/
│ └── UiAutomatorHooks.java
│
├── configs/
│ ├── rules.yaml
│ ├── scheduler.yaml
│ ├── devices.yaml
│ └── credentials.env.example
│
├── dashboards/
│ ├── grafana.json
│ └── alerts.yaml
│
├── tests/
│ ├── test_filters.py
│ ├── test_scheduler.py
│ └── fixtures/
│ └── sample_following.json
│
├── media/
│ └── threads-auto-unfollow-bot-banner.png
│
├── logs/
│ ├── app.log
│ └── device/
│ └── device-001.log
│
├── output/
│ ├── reports/
│ │ ├── run-2025-10-30.csv
│ │ └── rollup.json
│ └── screenshots/.keep
│
├── docker/
│ ├── Dockerfile
│ └── compose.yml
│
├── requirements.txt
├── package.json
└── README.md
```

## Use Cases
- **Social managers** use it to prune non-engaging follows across many accounts, so they can maintain clean, high-signal audiences.  
- **Agencies** use it to enforce hygiene policies at scale, so they can improve trust scores and campaign performance.  
- **Creators** use it to keep feeds focused and boost engagement rates, so they can grow more reliably.  
- **Ops teams** use it to run nightly maintenance, so they can keep metrics stable without manual labor.

## FAQs
**How do I configure this for multiple accounts?**  
Define profiles in `devices.yaml` with per-account limits, proxies, and schedules. The queue assigns work with isolation so accounts never share IP/fingerprint contexts.

**Does it support proxy rotation or anti-detection?**  
Yes. Assign per-account residential/mobile proxies and optional fingerprint profiles. Rotation cadence and sticky sessions are configurable in `proxy_manager.py`.

**Can I schedule it to run periodically?**  
Use `scheduler.yaml` to define CRON-like windows, daily caps, and blackout periods. The queue throttles by account and device to respect limits.

**What if the Threads UI changes?**  
Selectors and flows are versioned. The bot falls back to heuristic anchors, and you can hot-patch locator maps without redeploying core logic.

**Can it skip VIPs or recent followers?**  
Yes. Add rules in `rules.yaml` to whitelist handles, verified accounts, or “recent follow” windows.

## Performance & Reliability Benchmarks
- **Execution Speed:** ~350–600 candidate evaluations per device/hour with conservative human-like pacing (action and scroll jitter enabled).  
- **Success Rate:** Operational success rate of **95%** across mixed device farms when proxies and rules are properly configured.  
- **Scalability:** Horizontally scales to **300–1000** Android devices using queue-based fan-out and per-device isolation.  
- **Resource Efficiency:** Lightweight workers (<200MB RSS typical) with ephemeral media capture; configurable screenshot sampling to reduce I/O.  
- **Error Handling:** Exponential backoff, max-retry caps, circuit-breakers on rate-limit patterns, structured logs, and alerting via webhooks/Telegram/Discord.

##
<p align="center">
<a href="https://cal.com/app-pilot-m8i8oo/30min" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
</p>






