# Awesome-CDN-Analytics-Platform

# 顶级 CDN 分析平台生态系统

**精选 SaaS 产品与开源 GitHub 项目列表**
*聚焦实时流量分析、缓存性能、安全洞察与边缘日志管理*
**最后更新：2026 年 9 月**

本仓库追踪 **CDN 分析** 领域的知名 **SaaS 平台**与**开源项目**。这些工具帮助开发者、SRE 和安全团队监控 CDN 流量模式、缓存命中率、源站性能和安全事件，确保全球内容分发网络的可见性和可靠性。

**示例**包括 Cloudflare Analytics、Fastly Real-Time Analytics、Akamai Cloud Monitor、Amazon CloudFront Reports、Google Cloud CDN Insights、Imperva CDN Analytics、CDN77 Analytics、Bunny.net Analytics、Gcore Analytics 和 Edgio Analytics（该领域的领先者）。

**开源重点**：CDN 分析领域的开源生态**主要集中在日志处理和通用 Web 分析层面**。CDN 厂商的专有分析平台（Cloudflare、Fastly）深度集成其边缘网络，开源替代方案无法直接复制其边缘原生可见性。然而，**GoAccess** 提供了零配置的实时 Web 服务器日志分析，**Graylog** 和 **OpenSearch** 提供了企业级日志聚合能力，**Matomo** 和 **Plausible** 提供了隐私优先的流量分析。本列表重点收录这些可自托管的生产级方案。

欢迎贡献！提交 PR 以添加/更新条目。保持描述事实性，并链接到官方网站。

## 目录

- [SaaS/托管平台](#saas托管平台)
- [开源 GitHub 项目](#开源github项目)
- [如何贡献](#如何贡献)
- [免责声明](#免责声明)

## SaaS/托管平台

- **[Cloudflare Analytics](https://www.cloudflare.com/analytics/)**
  全面的分析产品，涵盖账户级和域名级指标。账户级包括 Account Analytics（请求、带宽、安全、缓存、错误）、Network Analytics（Enterprise，Spectrum/Magic Transit/BYOIP）和 Web Analytics（隐私优先，无个人数据收集）。域名级提供 Traffic（请求、数据传输、页面浏览、访问、API 请求）、Security（威胁、爬虫/机器人、速率限制）、Performance（源站性能、节省带宽）、Workers 和 Logs（Enterprise）。GraphQL Analytics API 支持自定义视图 。

- **[Fastly Real-Time Analytics](https://www.fastly.com/products/observe)**
  实时、边缘原生的可观测性平台。监控 **200+ 性能、流量、缓存、源站和安全指标**。提供实时日志流式传输（33+ 集成、6 种协议）、完整历史报告（回溯至服务第一天）、自定义仪表板和警报 。**Log Explorer & Insights** 允许在平台内直接存储、可视化和分析日志数据，无需第三方工具。**Origin Inspector** 提供源站服务器实时和历史响应数据。**Domain Inspector** 提供每个域名的响应数据 。

- **[Akamai Cloud Monitor](https://www.akamai.com/)**
  基于云的实时推送 API 服务，将关键事务和安全事件数据从 Akamai 智能平台传输到报告环境 。提供完整的请求-响应周期指标和源站响应时间。日志包含地理数据、HTTP 数据、网络数据、请求/响应头数据和 WAF 数据，可通过 Mezmo 等平台解析和路由 。

- **[Amazon CloudFront Reports](https://aws.amazon.com/cloudfront/)**
  提供标准日志文件（发送到 S3 供 Athena 查询）和实时日志（发送到 Kinesis Data Streams）。控制台内置使用情况报告和图表（支持 CSV 下载）。CloudWatch 自动发布分发和边缘函数指标，支持创建警报（如 TotalErrorRate）。

- **[Google Cloud CDN Insights](https://cloud.google.com/cdn)**
  Cloud Monitoring 提供预定义仪表板，无需手动配置。核心指标包括总请求数、缓存出口、总错误率、4xx/5xx 错误率、缓存结果比率和总缓存填充量 。动态地理地图显示客户端请求来源，支持自定义仪表板查询（如按缓存结果分类的字节数、P95 TCP 往返延迟、按国家分类的请求数）。

- **[Imperva CDN Analytics](https://www.imperva.com/)**
  网站仪表板监控缓存对性能的影响。平均而言，使用 Imperva CDN 的网站速度提升 50%，带宽消耗减少 70% 。提供实时仪表板、L3/4 可见性、缓存分布统计、安全威胁数据（按黑名单原因分类的阻止访问、可疑机器人会话、WAF 警报）以及自定义安全规则效果分析 。

- **[CDN77 Analytics](https://www.cdn77.com/)**
  通过 API 提供统计数据。支持的统计类型包括 bandwidth、costs、headers、hit-miss、traffic 和 traffic-miss 。可按 CDN 资源、数据中心位置和聚合粒度（5 分钟、1 小时、1 天、1 月）进行筛选。返回缓存和非缓存内容的服务大小（字节）。

- **[Bunny.net Analytics](https://bunny.net/)**
  提供视频分析功能，包括总观看次数、总观看时间、按国家查看次数/观看时间、数据中心流量分布、服务带宽和请求数。**热图**可视化观众对特定视频的参与度（重看最多 vs 掉线区域）。**参与度评分**（0-100）基于观看时长和模式，仅通过 API 提供 。

- **[Gcore Analytics](https://gcore.com/)**
  CDN 分析平台，提供流量、缓存和安全指标。支持实时监控和历史数据分析。

- **[Edgio Analytics](https://edg.io/)**
  边缘应用分析平台（原 Layer0）。提供 CDN 性能指标、流量分析和边缘函数监控。

## 开源 GitHub 项目

### Web 服务器日志分析

- **[GoAccess](https://github.com/allinurl/goaccess)**
  **零配置实时 Web 日志分析器**。读取 Apache、Nginx、Caddy 日志文件并生成终端或 HTML 仪表板，无需数据库或 Docker 。功能包括访问者、带宽、状态码、GeoIP 和 WebSocket 实时 HTML 更新。**极其快速**——数秒处理数百万日志行。**极低资源占用**（约 10 MB RAM）。**MIT 许可**。注意：仅限 Web 服务器日志，无警报功能，不支持远程日志收集 。

### 日志聚合与管理

- **[Graylog](https://github.com/Graylog2/graylog2-server)**
  基于 Elasticsearch/OpenSearch 的日志管理平台，自带 Web UI、警报引擎和日志处理管道。**全文本搜索**极快——跨数百万日志条目瞬间查找特定错误 。**处理管道**支持解析、富化和路由日志（提取字段、添加 GeoIP、路由关键错误到独立流）。功能包括仪表板、GELF 输入、RBAC。**需要 Elasticsearch/OpenSearch + MongoDB**——最低 4 GB RAM（生产 8 GB+）。

- **[OpenSearch + Dashboards](https://github.com/opensearch-project/OpenSearch)**
  Elasticsearch 的 Apache 2.0 分支，提供完整的 ELK 式体验，无 Elastic 许可限制。**全文本索引**——海量日志量下最快的搜索。OpenSearch Dashboards 提供 Kibana 式可视化。**安全插件**包含认证、审计和加密。**Apache 2.0 许可**。**资源消耗极高**（最低 4 GB RAM，推荐 8-16 GB）。

- **[Grafana Loki](https://github.com/grafana/loki)**
  **标签索引**（非全文本）的日志聚合系统。搜索速度快（标签），内容搜索较慢。**存储效率极佳**（压缩）。通过 Grafana 提供仪表板和警报。**最低 RAM** 约 500 MB（完整栈）。**AGPL-3.0 许可**。适合资源敏感环境和已有 Grafana 栈的团队 。

### 隐私优先 Web 分析

- **[Matomo](https://github.com/matomo-org/matomo)**
  **GPL-3.0 许可**的开源分析平台。提供自托管网站跟踪、高级隐私控制、自定义仪表板、实时流量来源/关键词/语言/热门内容洞察。**无第三方数据共享**，无广告集成 。拥有 201 个替代品排名，是最成熟的开源 Google Analytics 替代方案。

- **[Plausible Analytics](https://github.com/plausible/analytics)**
  **隐私优先的轻量级分析**。脚本小于 1KB，**无 Cookie**，**GDPR 合规**。提供实时仪表板、高级过滤、自定义事件、多级位置数据和地图可视化。**开源** 。

- **[Umami](https://github.com/umami-software/umami)**
  **MIT 许可**的自托管 Web 分析工具。强调简单性和隐私，仅收集必要指标，单页查看。**开源** 。

### 日志收集与路由

- **[Fluentd](https://github.com/fluent/fluentd)**
  开源数据收集器，统一日志收集和消费。**灵活数据路由**——事件可同时路由到多个目的地（文件、RDBMS、NoSQL、IaaS、SaaS、Hadoop）基于标签规则。优化用于**大规模日志处理和转发**，适合作为 Elasticsearch 或其他存储后端前的收集和路由层 。

- **[Syslog-ng](https://github.com/syslog-ng/syslog-ng)**
  开源日志管理程序，从多源收集、分类、转换和路由日志数据。**独特能力：结构化处理**——日志可在转发前规范化为一致格式。支持 RFC3164、RFC5424、JSON 和键值格式。**TLS 加密传输**。**条件路由**——单个实例可将认证失败路由到安全团队流、应用错误路由到开发团队流。**不是分析平台**——无查询 UI、仪表板或警报，作为 Elasticsearch 或 Graylog 前的收集层 。

### 其他强开源选项

- **日志收集**：**Fluentd**（灵活路由）、**Syslog-ng**（结构化处理）、**Vector**（高性能日志管道）。
- **Web 分析**：**Matomo**（最成熟，GPL-3.0）、**Plausible**（隐私优先，<1KB）、**Umami**（MIT，极简）、**GoatCounter**（托管/自托管，简单）。
- **日志分析**：**GoAccess**（零配置实时分析）、**Graylog**（全文本搜索）、**OpenSearch**（ELK 替代）、**Loki**（标签索引，存储高效）。

**构建自定义系统的框架**：结合 **Fluentd** 或 **Syslog-ng** 作为日志收集和路由层，**Graylog** 或 **OpenSearch** 作为日志存储和全文本搜索后端，**Grafana** 或 **OpenSearch Dashboards** 用于可视化。对于 Web 流量分析，添加 **GoAccess**（快速日志分析）或 **Matomo/Plausible**（隐私优先跟踪）。添加 **PostgreSQL/MongoDB** 用于持久化。

## 如何贡献

1. Fork 仓库。
2. 在 `README.md` 中添加/编辑条目（遵循现有格式）。
3. 包含：名称、链接、1-2 句描述，以及是 SaaS 还是开源。
4. 提交 PR 并附简短说明。

如果你觉得这个仓库有用，请点星！

## 免责声明

- 这是一个**社区精选**列表——并非详尽无遗，也不构成认可。
- CDN 分析平台处理敏感的流量和用户数据；确保符合 GDPR、CCPA 和相关数据保护法规。
- **开源现实**：CDN 分析的开源生态在 **Web 服务器日志分析**（GoAccess）和 **日志聚合**（Graylog、OpenSearch）层面成熟，但**无法直接复制 CDN 厂商的边缘原生分析能力**（如 Cloudflare 的 300+ 数据中心实时指标、Fastly 的 200+ 边缘指标）。开源方案需要自行收集和聚合 CDN 日志（通过 Logpush、S3 等），然后使用上述工具进行分析。对于需要边缘原生可见性的场景，商业 CDN 分析平台仍是首选。

---

**为 SRE、平台工程师、Web 性能优化团队和 CDN 运维人员打造。**
让 CDN 分析更开放、透明、可观测。
