<div align="center">

# Jim

### 把业务知识与资源，整合成可运行、可复用的系统

**全栈工程师 · AI 应用与自动化 · 企业数字化**

[![GitHub](https://img.shields.io/badge/GitHub-Jim--purch-181717?logo=github)](https://github.com/Jim-purch)
[![Email](https://img.shields.io/badge/cxxvcheng@gmail.com-ea4335?logo=gmail&logoColor=white)](mailto:cxxvcheng@gmail.com)

</div>

---

## 我是谁

懂**跨境贸易与供应链**业务的全栈工程师，TypeScript / Python 双栈。2024 年至今独立完成 **60 个项目（含 33 个企业级私有项目）**。

我做的事可以收拢成一句话：**把散落在一线的知识、数据、工具与 AI 能力，整合成一套能跑起来、能复用的系统。**

> 我的差异化不是某一项技术，而是**整合**。下面三层，就是这句话的展开。

---

## 一 · 知识整合　把业务经验变成可计算、可复用的资产

我在外贸一线积累的报价规则、库存与订单逻辑、配件编码体系、报关流程、客户分层方法，被系统性地从「人脑里的经验」整理成**数据模型、计算引擎、文档与 AI Skill**。

- **报价一致性系统**　把全部报价公式从云端文档搬进本地计算引擎复算，打通报价 / 库存 / 订单口径；订单自动转换为商业发票、装箱单、报关单。
- **多品牌配件数据逆向**　逆向解析 Crown（PSRT5 / SQL Server）、Jungheinrich（Jeti）、Linde（Service Guide）的配件数据，统一为可扩展的多品牌检索目录。
- **销售知识 Skill 化**　把客户分级、深度背调、话术起草、跟进提醒等销售经验封装成 AI 可调用的能力，而不是留在个人手里。

`Python` `FastAPI` `SQLite` `Next.js` `AirScript` `LLM Skill`

---

## 二 · 资源整合　把分散的数据源、工具与 AI 能力聚合成统一入口

把散落在阿里国际站（ICBU）、WhatsApp、邮件、飞书、WPS 表格、PDF 与图片里的数据，以及 Webhook、MCP、LLM、TTS 等能力，收拢成可查询、可调用的入口。

- **外贸销售 AI 中台**　多源实时采集客户会话与画像，本地增量归档、跨销售按手机号去重形成统一「客户公海」，再由 AI 完成翻译、分级、背调与跟进提醒——团队共享同一份客户认知。
  `ICBU` `WhatsApp` `邮件` `飞书` `SQLite / FTS5` `Chrome 扩展` `Hub + Agent`
- **jim-wps-mcp-server**　基于 MCP 协议打通 AI 与企业 WPS 云表格，支持 `stdio` 与 `HTTP/SSE` 双传输；已发布 npm，`npx` 一键运行。
  [github.com/Jim-purch/jim-wps-mcp-server](https://github.com/Jim-purch/jim-wps-mcp-server)
- **云表格快速查找**　集中管理 WPS / Google Sheets 脚本令牌，跨表多条件搜索、Token 权限分享、一键生成 MCP 配置。
  [github.com/Jim-purch/websearch-wps-webhook](https://github.com/Jim-purch/websearch-wps-webhook)
- **图像与文档流水线**　背景替换、条码识别命名、OCR 采集、图片分类、PDF 原位翻译，把人工重复操作整合成一键流水线。

---

## 三 · 能力整合　一个人跑通从业务建模到上线运维的完整链路

从需求调研、数据建模、API、前端交互，到 Docker / Caddy / FRP 部署与监控，独立闭环，不依赖外部平台。

- **海量配件数据库系统**　配件 2000 万+ 条、转换码 2900 万+ 条，数据库 30+ GB。设计 PostgreSQL 主从 + 读写分离 + Redis 多级缓存 + Elasticsearch 全文检索架构；支持 **1000+ 并发**，查询提速 **10–50 倍**，平均响应 **< 100ms**，相关人力由 **6 人降至 2 人**。
  `Flask` `PostgreSQL` `Redis` `Elasticsearch` `Docker` `PyQt5`
- **自托管基础设施**　Windows 上的 Caddy / FRP 站点与隧道管理面板、统一邮箱验证码鉴权与跨子域 SSO、文件搜索安全代理，让整套系统可私有化、可远程运维。
  `FastAPI` `Caddy` `FRP` `Nginx`
- **全栈产品**　从多人 AI 对话产品、太空探索放置游戏，到桌面工具与浏览器扩展，独立完成设计、开发与部署。

---

## 公开项目

| 项目 | 一句话 | 技术 |
| :--- | :--- | :--- |
| [**jim-wps-mcp-server**](https://github.com/Jim-purch/jim-wps-mcp-server) | 让 AI 直连企业 WPS 云表格的 MCP 服务器（已发布 npm） | TypeScript · MCP |
| [**websearch-wps-webhook**](https://github.com/Jim-purch/websearch-wps-webhook) | 云表格令牌管理与跨表快速搜索平台 | Next.js 16 · Supabase |
| [**soul-mirror-with-other.skill**](https://github.com/Jim-purch/soul-mirror-with-other.skill) | AI 引导的多人关系探索对话系统 | Skill · Prompt |
| [**OH-MindMirror**](https://github.com/Jim-purch/OH-MindMirror) | 基于 OH 卡牌原理的 AI 心理投射工具 | React · Gemini API |
| [**TeleChat**](https://github.com/Jim-purch/telechat) | DeepSeek 推理 + MiniMax 语音的 Telegram 机器人 | Node.js · Docker |
| [**know-yourself-tools**](https://github.com/Jim-purch/know-yourself-tools) | 人工咨询 + AI 结合的自我认知工具 | React · TypeScript |
| [**mac-voice-to-text**](https://github.com/Jim-purch/mac-voice-to-text) | 实时把内录系统声音与外录麦克风声音转成文字 | 桌面端 · 语音 |
| [**pdf-picture-extract-pc-tool**](https://github.com/Jim-purch/pdf-picture-extract-pc-tool) | 从标签 PDF 提取二维码图片，拖拽即用 | Python · GitHub Actions |
| [**qq-music-local-web-control**](https://github.com/Jim-purch/qq-music-local-web-control) | 局域网浏览器控制办公室电脑的 QQ 音乐 | Python · Playwright |
| [**put-watermark-web**](https://github.com/Jim-purch/put-watermark-web) | 纯浏览器端批量图片加水印，不上传服务器 | Vite · Docker |

---

## 技术与工具

- **语言**　TypeScript, Python, JavaScript, SQL
- **前端**　React 19, Next.js 15/16, Vue 3, Vite, Tailwind CSS, Zustand
- **后端**　FastAPI, Flask, Node.js, Express, Socket.IO, RESTful / SSE
- **数据**　PostgreSQL, SQLite（`node:sqlite`）, Redis, Elasticsearch, Supabase, FTS5
- **AI**　MCP Protocol, Agent Skill, LLM 编排（DeepSeek / 智谱 / Kimi / Gemini / OpenAI 兼容端点）, MiniMax TTS, Prompt Engineering
- **运维**　Docker / Compose, Nginx, Caddy, FRP, GitHub Actions, pm2, Vercel

---

## AI 如何进入我的流程

不是「用 AI 帮我写代码」，而是把 AI 工程化进交付链路：

1. **先文档后代码**　每个项目沉淀 `docs/`（调研、决策、部署、运维日志），需求模糊时先定方案；
2. **规范 + 工具化**　用项目规范文件 + 自定义 Skill + MCP Server 连接业务数据源，让 AI 在受控上下文里工作；
3. **人工把关**　AI 生成内容一律经代码审查、测试与部署验证，未经验证的数字与结论不写入交付物；
4. **一次解决，长期复用**　可复用的部分固化为 Skill、脚本管线或模板。

---

## 我在寻找什么

- **岗位方向**　AI 应用工程 / 全栈开发 / 企业数字化 / 技术负责人
- **合作方向**　AI 落地、企业流程自动化、跨境贸易系统
- 远程或线下均可，具体可聊。

<br>

<div align="center">

[![Email](https://img.shields.io/badge/📮_cxxvcheng@gmail.com-ea4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:cxxvcheng@gmail.com)

📄 详细版（项目与经历）：[Jim_Resume.md](./Jim_Resume.md)

</div>
