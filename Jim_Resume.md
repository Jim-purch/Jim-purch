# Jim - 知识与资源整合者 & AI 协作产品构建者

> 把散落在业务一线的知识、行业数据、工具脚本与 AI 能力，整合成可复用、可交付、可持续进化的系统。

> 📌 简洁概览见 [README](./README.md) · 🌐 在线交互版简历与技术手记见 **[jim-resume.vercel.app](https://jim-resume.vercel.app/)**；本文件是**项目与经历的完整详细版**。

## 基本信息

- **姓名**: Jim
- **在线主页 / Portfolio**: [https://jim-resume.vercel.app/](https://jim-resume.vercel.app/)
- **技术手记 / Blog**: [https://jim-resume.vercel.app/blog](https://jim-resume.vercel.app/blog)
- **GitHub**: [github.com/Jim-purch](https://github.com/Jim-purch)
- **邮箱**: cxxvcheng@gmail.com
- **专业定位**: 知识与资源整合者 / AI 协作与全栈数字化产品构建者
- **核心命题**: 我的核心能力不是某一项单一技术，而是**整合**——把「行业 Know-how × 数据资产 × AI 能力 × 工程交付」串成闭环，让知识可沉淀、资源可流动、经验可复用。
- **核心哲学**: AI 不是替代人的威胁，而是增强人的工具。人提供方向与判断，AI 提供执行与可能性。

## 核心技能

### AI协作与工具应用

- **AI工具精通**: Claude Code, ChatGPT, DeepSeek, Gemini, LM Studio, 本地大模型部署与优化
- **MCP生态构建**: 基于 Model Context Protocol 开发工具服务器，打通 AI 与企业数据（[jim-wps-mcp-server](https://github.com/Jim-purch/jim-wps-mcp-server) 已发布 npm）
- **Agent Skill 沉淀**: 将业务复盘、销售SOP与深度对话封装为可复用 Skill（[soul-mirror-with-other.skill](https://github.com/Jim-purch/soul-mirror-with-other.skill)、[accio-work-output.skill](https://github.com/Jim-purch/accio-work-output.skill)）
- **AI服务集成**: DeepSeek / MiniMax TTS / Gemini 多模态 / Whisper ASR 集成（语音、图像、文本）

### 全栈开发能力

- **前端**: React 18/19, Next.js 15/16, Vue 3, Vite 6, TypeScript, Tailwind CSS v4, Zustand
- **后端**: FastAPI, Flask, Node.js, RESTful API / SSE 设计
- **数据库**: PostgreSQL, SQLite, Redis, Elasticsearch, Supabase (Auth + RLS)
- **DevOps**: Docker, Docker Compose, Nginx, Caddy, FRP 内网穿透, GitHub Actions, Vercel 部署
- **原生与桌面端**: macOS Swift (ScreenCaptureKit), PyQt5, PySide6, Chrome Extension

### 产品与需求管理

- **需求工程**: 深度业务调研、用户故事编写、功能需求文档化
- **产品设计**: 业务流程梳理、系统架构设计、Warm-Tech 人本交互体验打磨
- **质量控制**: AI生成代码审查、自动化单元测试、容器化与线上部署验证

### 业务领域专长

- **企业数字化**: 传统业务流程 AI 化改造、跨系统自动化同步解决方案设计
- **海量数据处理**: 2000万+ 配件记录、2900万+ 转换码记录的分布式系统经验
- **跨境贸易与供应链**: 出口业务流程、海关单证自动化、多品牌配件编码标准化与库存协同

---

## 核心项目经验

### 1. 海量配件数据库系统 (linkImgDataProcess) ⭐⭐⭐⭐⭐

**项目描述**: 企业级配件数据管理系统，从单体 SQLite 应用演进为 Docker 分布式微服务架构，支持千万级数据的亚秒级查询  
**我的角色**: 系统架构师 & 全栈开发者  
**项目性质与链接**: 企业核心私有库 · 📖 [架构演进实录](https://jim-resume.vercel.app/blog/parts-database-architecture) · 🔗 配套目录提取开源工具 [parts-catalog-pdf-to-xlsx](https://github.com/Jim-purch/parts-catalog-pdf-to-xlsx)  

**数据规模与性能**:
- 配件数据 **2,000万+** 条记录，转换码数据 **2,900万+** 条记录
- 数据库体量 **30+ GB**，支持 **1000+** 用户并发访问
- 查询速度提升 **10-50倍**，平均响应时间 **< 100ms**，相关人力由 **6 人降至 2 人**

**核心贡献**:
- **分布式架构设计**: 设计 PostgreSQL 主从复制 + 读写分离 + Redis 多级缓存 + Elasticsearch 全文搜索的完整架构
- **客户端-服务器架构**: PyQt5 桌面客户端 + Flask RESTful API + SQLite/PostgreSQL 后端
- **管理端系统**: 支持数据导入、用户权限管理、服务监控、供应商管理
- **容器化部署**: 基于 Docker Compose 一键部署，集成 Prometheus + Grafana 监控告警

**技术栈**: Python, Flask, PostgreSQL, Redis, Elasticsearch, Docker, PyQt5, Nginx, Prometheus, Grafana

---

### 2. WPS MCP Server (jim-wps-mcp-server) ⭐⭐⭐⭐⭐

**项目描述**: 基于 Model Context Protocol 的 WPS 表格集成服务器，让 Claude Desktop / Cursor / Cline 等智能体直接查询和操作企业云表格数据  
**我的角色**: 独立开发者（已发布 npm）  
**开源仓库与文档**: 🔗 [github.com/Jim-purch/jim-wps-mcp-server](https://github.com/Jim-purch/jim-wps-mcp-server) · 📖 [开源介绍与接入指南](https://jim-resume.vercel.app/blog/wps-mcp-server-guide)  

**核心贡献**:
- **MCP协议实现**: 完整实现 MCP 标准，支持 `stdio` 和 `HTTP/SSE` 双传输模式
- **工具集设计**: 设计 `search`、`batch_search`、`get_table_list`、`get_image_urls` 等 AI 可调用工具
- **多配置管理**: 支持多 Webhook 配置，一套服务连接多个 WPS 表格
- **npm发布**: 包 `jim-wps-mcp-server` 已发布，支持 `npx` 一键运行

**技术栈**: TypeScript, Node.js, MCP Protocol, WPS AirScript, npm

---

### 3. 云表格快速查找 SaaS (websearch-wps-webhook) ⭐⭐⭐⭐⭐

**项目描述**: 全栈云表格搜索管理平台，集中管理 WPS / Google Sheets 脚本令牌，支持跨表多条件搜索、分享分发和 MCP 配置生成  
**我的角色**: 全栈开发者 & 产品设计  
**开源仓库与文档**: 🔗 [github.com/Jim-purch/websearch-wps-webhook](https://github.com/Jim-purch/websearch-wps-webhook) · 📖 [全栈 SaaS 构建手记](https://jim-resume.vercel.app/blog/cloud-sheet-saas-guide)  

**核心贡献**:
- **全栈SaaS架构**: Next.js 16 App Router + Supabase (Auth + PostgreSQL + RLS 行级安全)
- **跨表搜索引擎**: 多条件 AND 搜索、批量搜索、自动分批回退、增量结果流式展示
- **Token管理系统**: 脚本令牌集中管理、分享码安全分发、权限控制 (view/use)、过期时间
- **MCP配置生成**: 一键生成选中 Token 的 MCP 配置 JSON

**技术栈**: Next.js 16, React 19, TypeScript, Tailwind CSS v4, Supabase, ExcelJS, Vercel

---

### 4. OH-MindMirror — AI 心理投射工具 ⭐⭐⭐⭐

**项目描述**: 基于 OH 卡牌原理的数字疗愈应用，结合 Gemini 多模态 AI 引导用户进行潜意识探索与自我对话  
**我的角色**: 产品设计 & 全栈开发  
**开源仓库与文档**: 🔗 [github.com/Jim-purch/OH-MindMirror](https://github.com/Jim-purch/OH-MindMirror) · 📖 [多模态心理镜像开发手记](https://jim-resume.vercel.app/blog/oh-mindmirror-intro)  

**核心贡献**:
- **两步阶梯引导**: 通过客观图像观察到主观投射提问，规避模型说教与廉价鸡汤
- **关联生态**: 同步开源自我探索工具集 [know-yourself-tools](https://github.com/Jim-purch/know-yourself-tools) 与多人关系对话 Skill [soul-mirror-with-other.skill](https://github.com/Jim-purch/soul-mirror-with-other.skill)

**技术栈**: React, TypeScript, Vite, Gemini 2.0 API

---

### 5. Mac Voice to Text — macOS 免驱动双通道实时听写 ⭐⭐⭐⭐

**项目描述**: 解决 macOS 线上会议与播客实时转文字痛点，免安装虚拟声卡即可同步采集系统内录与麦克风外录并实时转写  
**我的角色**: 独立开发者  
**开源仓库与文档**: 🔗 [github.com/Jim-purch/mac-voice-to-text](https://github.com/Jim-purch/mac-voice-to-text) · 📖 [ScreenCaptureKit 音频实践指南](https://jim-resume.vercel.app/blog/mac-voice-to-text-guide)  

**核心贡献**:
- **免驱动内录**: 基于 Apple 原生 `ScreenCaptureKit` 采集系统播放音频
- **双通道混音与低延迟转写**: `AVAudioEngine` 重采样混音，串联本地/云端 Whisper 实时输出字幕

**技术栈**: Swift, macOS ScreenCaptureKit, AVAudioEngine, Whisper ASR

---

### 6. TeleChat — Telegram AI 智能语音机器人 ⭐⭐⭐⭐

**项目描述**: 集成 DeepSeek AI 推理与 MiniMax 语音合成的 Telegram 机器人，提供智能文本+语音双通道交互  
**我的角色**: 独立开发者  
**开源仓库与文档**: 🔗 [github.com/Jim-purch/telechat](https://github.com/Jim-purch/telechat) · 📖 [双通道语音机器人部署指南](https://jim-resume.vercel.app/blog/telechat-voice-bot)  

**核心贡献**:
- **多AI服务编排**: DeepSeek (深度推理) + MiniMax TTS (高拟真语音合成) 流式分句播报
- **工程化部署**: Docker 容器化、离线部署包、一键部署脚本与会话级语音角色切换

**技术栈**: Node.js / Python, DeepSeek API, MiniMax TTS, Docker, Telegram Bot API

---

### 7. WPS 企业自动化与跨云同步套件 (sheets2kdocs & tmtPartWps) ⭐⭐⭐⭐

**项目描述**: 围绕金山文档（WPS 多维表格/智能表格）与 Google Sheets 构建的企业级自动化体系，涵盖跨云定时同步、报价复算、库存管理与标签打印  
**我的角色**: 产品设计 & 全栈开发  
**开源仓库**: 🔗 [github.com/Jim-purch/sheets2kdocs](https://github.com/Jim-purch/sheets2kdocs)（核心 ERP 报价脚本为企业私有）  

**核心贡献**:
- **跨云定时同步 (`sheets2kdocs`)**: 自托管 FastAPI 服务，支持管理后台、字段映射及 Upsert / Replace 模式将 Google Sheets 自动同步至 WPS 智能表格
- **报价与库存自动化**: 智能增量备份、配件编码去重、Bartender HTTP API 多线程标签打印

**技术栈**: Python, FastAPI, WPS AirScript, Flask, Bartender SDK

---

### 8. Everything Proxy Service & 自托管鉴权套件 ⭐⭐⭐⭐

**项目描述**: Everything 文件搜索引擎的安全代理服务（增强认证、访问日志、路径混淆、PyQt5 管理面板与 FRP 穿透）及云存储鉴权服务  
**我的角色**: 系统架构师 & 全栈开发  
**关联开源仓库**: 🔗 [github.com/Jim-purch/qiniuyun-upload-auth](https://github.com/Jim-purch/qiniuyun-upload-auth)（Everything 代理核心为企业内网私有）  

**技术栈**: Python, Flask, FastAPI, PyQt5, SQLite, PostgreSQL, FRP, Docker

---

### 9. 星海方舟 — 太空探索放置游戏 (aquor-space-site-game) ⭐⭐⭐⭐

**项目描述**: 宇宙方舟主题的太空探索放置类网页游戏，包含 10 种资源、4 个星域、科技树、巨型工程和声望系统  
**我的角色**: 独立全栈开发  
**关联公开项目**: 🔗 [github.com/Jim-purch/ball-webgame](https://github.com/Jim-purch/ball-webgame)（星海方舟完整商业级工程为独立私有库）  

**技术栈**: React 18, TypeScript, Vite 6, Tailwind CSS, Zustand, Supabase, Vitest

---

### 10. 纯前端批量水印与图像文档开源工具链 ⭐⭐⭐⭐

**项目描述**: 100% 浏览器本地处理的隐私优先批量图片加水印工具，以及配套的企业图像/PDF 自动化开源工具集  
**我的角色**: 独立开发  
**开源仓库与文档**:
- 🔗 [put-watermark-web](https://github.com/Jim-purch/put-watermark-web) · 📖 [Canvas 离屏渲染与 15MB Docker 私有化手记](https://jim-resume.vercel.app/blog/batch-watermark-privacy-guide)
- 🔗 [bgremove-zbar-rename](https://github.com/Jim-purch/bgremove-zbar-rename)（产品图自动去背景 + 条码识别重命名）
- 🔗 [pdf-picture-extract-pc-tool](https://github.com/Jim-purch/pdf-picture-extract-pc-tool)（标签 PDF 提取二维码桌面端）
- 🔗 [pdf-to-svg-png](https://github.com/Jim-purch/pdf-to-svg-png) & [image-ocr-csv](https://github.com/Jim-purch/image-ocr-csv)

**技术栈**: Vite, HTML5 Canvas, Web Worker, Python, Docker, Nginx

---

## 近期项目整合实践（2025–2026）

近一年，我将一线业务知识、数据资产与 AI 能力系统性整合，落地了 30+ 个企业级项目（多数为私有），形成六条可复用的能力主线：

1. **外贸销售 AI 中台**：从阿里国际站（ICBU）、WhatsApp、邮件、飞书等多源实时采集客户会话与画像，本地增量归档、跨销售按手机号去重形成「客户公海」，再由 AI Skill 完成翻译、分级、深度背调、话术起草与跟进提醒。
2. **报价与多源数据一致性**：用本地服务复算全部报价公式替代云端文档查询，保证报价、库存、订单口径一致；订单自动转换为商业发票、装箱单、报关单等单据。
3. **多品牌配件数据逆向与检索**：逆向解析 Crown、Jungheinrich、Linde 等品牌配件数据，统一为可扩展的多品牌检索目录，后端承载千万级记录并支持亚秒级查询。
4. **图像与文档批处理流水线**：把背景替换、条码识别命名、OCR 采集、图片分类、PDF 原位翻译做成一次投入、长期复用的自动化管线。
5. **自托管基础设施**：Caddy / FRP 站点与隧道管理面板、统一邮箱验证码鉴权与跨子域 SSO、文件搜索安全代理与局域网终端协同（[tv-webserver](https://github.com/Jim-purch/tv-webserver)、[qq-music-local-web-control](https://github.com/Jim-purch/qq-music-local-web-control)）。
6. **AI 应用与人文心理探索**：把 AI 能力延伸到心理探索与关系联结场景（[OH-MindMirror](https://github.com/Jim-purch/OH-MindMirror)、[know-yourself-tools](https://github.com/Jim-purch/know-yourself-tools)、[soul-mirror-with-other.skill](https://github.com/Jim-purch/soul-mirror-with-other.skill)）。

---

## 职位适配方向

- **AI 应用工程师 / AI 解决方案架构师**：MCP 生态构建、Agent Skill 设计、多模态 AI 服务编排、产品全流程落地
- **全栈工程师**：React / Next.js + Python (FastAPI / Flask) + PostgreSQL / Supabase + Docker 全栈交付
- **企业数字化转型负责人 / Tech Lead**：从单体到千万级分布式系统的架构演进、跨部门业务流程 AI 化改造

---

*基于 60+ 个项目（含 33 个企业级私有项目与 27+ 个公开开源仓库）的持续实践，我的差异化在于「整合」：把行业 Know-how、数据资产、AI 能力与工程交付串成闭环。在线体验与架构实录请访问 [jim-resume.vercel.app](https://jim-resume.vercel.app/)。*
