# Awesome-CDN-Analytics-Platform

## Top CDN Analytics Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Real-Time Traffic Analysis, Cache Performance, Security Insights & Edge Log Management*
**Last updated: September 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **CDN Analytics**. These tools help developers, SREs, and security teams monitor CDN traffic patterns, cache hit ratios, origin performance, and security events across global content delivery networks.

**Examples** include Cloudflare Analytics, Fastly Real-Time Analytics, Akamai Cloud Monitor, Amazon CloudFront Reports, Google Cloud CDN Insights, Imperva CDN Analytics, CDN77 Analytics, Bunny.net Analytics, Gcore Analytics, and Edgio Analytics (the category leaders).

**Open-source emphasis**: The open-source ecosystem for CDN analytics is **concentrated at the log processing and general web analytics layers**. Proprietary CDN analytics platforms (Cloudflare, Fastly) are deeply integrated with their edge networks, and open-source alternatives cannot directly replicate that edge-native visibility. However, **GoAccess** provides zero-config real-time web server log analysis, **Graylog** and **OpenSearch** deliver enterprise-grade log aggregation, and **Matomo** and **Plausible** offer privacy-first traffic analytics. This section focuses on these self-hostable, production-grade solutions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Cloudflare Analytics](https://www.cloudflare.com/analytics/)**
  Comprehensive analytics products spanning account-level and zone-level metrics. Account-level includes Account Analytics (requests, bandwidth, security, cache, errors), Network Analytics (Enterprise, Spectrum/Magic Transit/BYOIP), and Web Analytics (privacy-first, no personal data collection). Zone-level provides Traffic (requests, data transfer, page views, visits, API requests), Security (threats, bots, rate limiting), Performance (origin performance, bandwidth saved), Workers, and Logs (Enterprise). GraphQL Analytics API enables custom views .

- **[Fastly Real-Time Analytics](https://www.fastly.com/products/observe)**
  Real-time, edge-native observability platform. Monitors **200+ performance, traffic, cache, origin, and security metrics**. Provides real-time log streaming (33+ integrations, 6 protocols), full historical reporting (back to a service's first day), custom dashboards, and alerts . **Log Explorer & Insights** allows storing, visualizing, and analyzing log data directly within the platform without third-party tools. **Origin Inspector** delivers real-time and historical origin server response data. **Domain Inspector** provides per-domain response data .

- **[Akamai Cloud Monitor](https://www.akamai.com/)**
  Cloud-based real-time push API service that streams critical transactional and security event data from Akamai's intelligent platform to reporting environments . Provides full request-response cycle metrics and origin response times. Logs include geographic data, HTTP data, network data, request/response header data, and WAF data, parsable and routable through platforms like Mezmo .

- **[Amazon CloudFront Reports](https://aws.amazon.com/cloudfront/)**
  Offers standard logs (delivered to S3 for Athena queries) and real-time logs (delivered to Kinesis Data Streams). Console includes built-in usage reports and charts (CSV download supported). CloudWatch automatically publishes distribution and edge function metrics, enabling alarms (e.g., TotalErrorRate).

- **[Google Cloud CDN Insights](https://cloud.google.com/cdn)**
  Cloud Monitoring provides predefined dashboards with no manual configuration. Core metrics include total requests, cache egress, total error rate, 4xx/5xx error rates, cache result ratio, and total cache fill . Dynamic geographic maps show client request origins, with custom dashboard queries available (e.g., bytes by cache result, P95 TCP round-trip latency, requests by country).

- **[Imperva CDN Analytics](https://www.imperva.com/)**
  Website dashboard monitors CDN impact on performance. On average, sites using Imperva CDN see 50% speed improvement and 70% bandwidth reduction . Provides real-time dashboards, L3/4 visibility, cache distribution statistics, security threat data (blocked visits by blacklist reason, suspicious bot sessions, WAF alerts), and custom security rule effectiveness analysis .

- **[CDN77 Analytics](https://www.cdn77.com/)**
  Provides statistics via API. Supported statistic types include bandwidth, costs, headers, hit-miss, traffic, and traffic-miss . Filterable by CDN resource, datacenter location, and aggregation granularity (5 minutes, 1 hour, 1 day, 1 month). Returns served size in bytes for cached and non-cached content.

- **[Bunny.net Analytics](https://bunny.net/)**
  Provides video analytics including total views, total watch time, views/watch time by country, datacenter traffic distribution, served bandwidth, and request counts. **Heatmap** visualizes viewer engagement for specific videos (most rewatched vs. drop-off regions). **Engagement Score** (0-100) based on watch duration and patterns, available only via API .

- **[Gcore Analytics](https://gcore.com/)**
  CDN analytics platform providing traffic, cache, and security metrics. Supports real-time monitoring and historical data analysis.

- **[Edgio Analytics](https://edg.io/)**
  Edge application analytics platform (formerly Layer0). Provides CDN performance metrics, traffic analysis, and edge function monitoring.

## Open-Source GitHub Projects

### Web Server Log Analysis

- **[GoAccess](https://github.com/allinurl/goaccess)**
  **Zero-config real-time web log analyzer**. Reads Apache, Nginx, and Caddy log files and generates terminal or HTML dashboards with no database or Docker required . Features visitors, bandwidth, status codes, GeoIP, and WebSocket real-time HTML updates. **Extremely fast**—processes millions of log lines in seconds. **Extremely low resource footprint** (around 10 MB RAM). **MIT licensed**. Note: limited to web server logs, no alerting features, no remote log collection .

### Log Aggregation & Management

- **[Graylog](https://github.com/Graylog2/graylog2-server)**
  Log management platform built on Elasticsearch/OpenSearch with a built-in Web UI, alerting engine, and log processing pipelines. **Full-text search** is extremely fast—find a specific error across millions of log entries instantly . **Processing pipelines** parse, enrich, and route logs (extract fields, add GeoIP, route critical errors to separate streams). Features dashboards, GELF input, and RBAC. **Requires Elasticsearch/OpenSearch + MongoDB**—minimum 4 GB RAM (8 GB+ for production).

- **[OpenSearch + Dashboards](https://github.com/opensearch-project/OpenSearch)**
  Apache 2.0 fork of Elasticsearch providing a complete ELK-style experience without Elastic licensing restrictions. **Full-text indexing**—the fastest search at massive log volumes. OpenSearch Dashboards provides Kibana-style visualization. **Security plugin** includes authentication, audit, and encryption. **Apache 2.0 licensed**. **Resource consumption is very high** (minimum 4 GB RAM, 8-16 GB recommended).

- **[Grafana Loki](https://github.com/grafana/loki)**
  **Label-indexed** (not full-text) log aggregation system. Search is fast for labels, slower for content. **Storage efficiency is excellent** (compression). Dashboards and alerts via Grafana. **Minimum RAM** around 500 MB (full stack). **AGPL-3.0 licensed**. Suited for resource-sensitive environments and teams already using Grafana .

### Privacy-First Web Analytics

- **[Matomo](https://github.com/matomo-org/matomo)**
  **GPL-3.0 licensed** open-source analytics platform. Provides self-hosted website tracking, advanced privacy controls, custom dashboards, and real-time insights into traffic sources, keywords, languages, and popular content. **No third-party data sharing**, no ad integration . Ranked among 201 alternatives, it is the most mature open-source Google Analytics replacement.

- **[Plausible Analytics](https://github.com/plausible/analytics)**
  **Privacy-first lightweight analytics**. Script under 1 KB, **cookieless**, **GDPR compliant**. Provides real-time dashboards, advanced filtering, custom events, multi-level location data, and map visualization. **Open source** .

- **[Umami](https://github.com/umami-software/umami)**
  **MIT licensed** self-hosted web analytics tool. Emphasizes simplicity and privacy, collecting only essential metrics in a single page view. **Open source** .

### Log Collection & Routing

- **[Fluentd](https://github.com/fluent/fluentd)**
  Open-source data collector that unifies log collection and consumption. **Flexible data routing**—events can be routed to multiple destinations simultaneously (files, RDBMS, NoSQL, IaaS, SaaS, Hadoop) based on tag rules. Optimized for **large-scale log processing and forwarding**, suitable as a collection and routing layer in front of Elasticsearch or other storage backends .

- **[Syslog-ng](https://github.com/syslog-ng/syslog-ng)**
  Open-source log management program that collects, classifies, transforms, and routes log data from multiple sources. **Unique capability: structured processing**—logs can be normalized into a consistent format before forwarding. Supports RFC3164, RFC5424, JSON, and key-value formats. **TLS-encrypted transport**. **Conditional routing**—a single instance can route authentication failures to a security team stream and application errors to a dev team stream. **Not an analytics platform**—no query UI, dashboards, or alerts, serving as a collection layer in front of Elasticsearch or Graylog .

### Additional Strong Open-Source Options

- **Log Collection**: **Fluentd** (flexible routing), **Syslog-ng** (structured processing), **Vector** (high-performance log pipeline).
- **Web Analytics**: **Matomo** (most mature, GPL-3.0), **Plausible** (privacy-first, <1KB), **Umami** (MIT, minimal), **GoatCounter** (hosted/self-hosted, simple).
- **Log Analysis**: **GoAccess** (zero-config real-time analysis), **Graylog** (full-text search), **OpenSearch** (ELK alternative), **Loki** (label-indexed, storage-efficient).

**Frameworks for building custom systems**: Combine **Fluentd** or **Syslog-ng** as the log collection and routing layer, **Graylog** or **OpenSearch** as the log storage and full-text search backend, and **Grafana** or **OpenSearch Dashboards** for visualization. For web traffic analytics, add **GoAccess** (fast log analysis) or **Matomo/Plausible** (privacy-first tracking). Add **PostgreSQL/MongoDB** for persistence.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- CDN analytics platforms handle sensitive traffic and user data; ensure compliance with GDPR, CCPA, and relevant data protection regulations.
- **Open-source reality**: The open-source ecosystem is mature at the **web server log analysis** (GoAccess) and **log aggregation** (Graylog, OpenSearch) layers, but **cannot directly replicate the edge-native analytics capabilities** of CDN vendors (e.g., Cloudflare's real-time metrics across 300+ data centers, Fastly's 200+ edge metrics). Open-source solutions require collecting and aggregating CDN logs (via Logpush, S3, etc.) before analysis. For scenarios requiring edge-native visibility, commercial CDN analytics platforms remain the primary choice.

---

**Made for SREs, platform engineers, web performance teams, and CDN operators.**
Let's make CDN analytics more open, transparent, and observable.
