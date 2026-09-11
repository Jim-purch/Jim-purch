# Jim - 知识与资源整合者 & AI 协作产品构建者

> 把散落在业务一线的知识、行业数据、工具脚本与 AI 能力，整合成可复用、可交付、可持续进化的系统。

> 📌 简历入口见 [README](./README.md)；本文件是**项目与经历的详细版**。

## 基本信息

- **姓名**: Jim
- **GitHub**: [Jim-purch](https://github.com/Jim-purch)
- **邮箱**: cxxvcheng@gmail.com
- **专业定位**: 知识与资源整合者 / AI 协作产品构建者
- **核心命题**: 我的核心能力不是某一项技术，而是**整合**——把「行业 Know-how × 数据资产 × AI 能力 × 工程交付」串成闭环，让知识可沉淀、资源可流动、经验可复用。
- **核心哲学**: AI 不是替代人的威胁，而是增强人的工具。人提供方向与判断，AI 提供执行与可能性。

## 核心技能

### AI协作与工具应用

- **AI工具精通**: Claude Code, ChatGPT, DeepSeek, LM Studio, 本地大模型部署与优化
- **MCP生态构建**: 基于 Model Context Protocol 开发工具服务器，打通 AI 与企业数据 (WPS MCP Server 已发布 npm)
- **提示工程**: 精准需求描述、复杂业务逻辑拆解、AI输出质量控制
- **AI服务集成**: DeepSeek / MiniMax TTS / Gemini API 集成，多模态应用 (语音、图像、文本)

### 全栈开发能力

- **前端**: React 18/19, Next.js 16, Vite 6, TypeScript, Tailwind CSS v4, Zustand
- **后端**: Flask, FastAPI, Node.js, RESTful API 设计
- **数据库**: PostgreSQL, SQLite, Redis, Elasticsearch, Supabase
- **DevOps**: Docker, Docker Compose, Nginx, FRP内网穿透, GitHub Actions, Vercel 部署
- **桌面应用**: PyQt5, PySide6, tkinter GUI 开发与打包

### 产品与需求管理

- **需求工程**: 深度业务调研、用户故事编写、功能需求文档化
- **产品设计**: 业务流程梳理、系统架构设计、用户体验优化
- **项目管理**: 敏捷开发流程、里程碑管理、跨部门协作
- **质量控制**: AI生成代码审查、功能测试设计、部署验证

### 业务领域专长

- **企业数字化**: 传统业务流程AI化改造、自动化解决方案设计
- **海量数据处理**: 2000万+配件记录、2900万+转换码记录的分布式系统经验
- **跨境贸易**: 出口业务流程、海关合规、贸易文档自动化
- **供应链管理**: 配件管理、库存优化、采购流程设计

---

## 核心项目经验

### 1. 海量配件数据库系统 (linkImgDataProcess) ⭐⭐⭐⭐⭐

**项目描述**: 企业级配件数据管理系统，从单体 SQLite 应用演进为 Docker 分布式微服务架构，支持千万级数据的毫秒级查询  
**我的角色**: 系统架构师 & 全栈开发者  
**项目时间**: 2024年6月 - 持续迭代  

**数据规模与性能**:
- 配件数据 **2,000万+** 条记录，转换码数据 **2,900万+** 条记录
- 数据库体量 **30+ GB**，支持 **1000+** 用户并发访问
- 查询速度提升 **10-50倍**，平均响应时间 **< 100ms**

**核心贡献**:
- **分布式架构设计**: 设计 PostgreSQL 主从复制 + 读写分离 + Redis 多级缓存 + Elasticsearch 全文搜索的完整架构
- **客户端-服务器架构**: PyQt5 桌面客户端 + Flask RESTful API + SQLite/PostgreSQL 后端
- **管理端系统**: 开发功能完整的管理后台，支持数据导入、用户权限管理、服务监控、供应商管理
- **容器化部署**: 基于 Docker Compose 一键部署，集成 Prometheus + Grafana 监控告警
- **性能优化**: 多级缓存策略、热点数据预加载、查询优化、异步多线程处理

**技术栈**: Python, Flask, PostgreSQL, Redis, Elasticsearch, Docker, PyQt5, Nginx, Prometheus, Grafana

---

### 2. WPS MCP Server (jim-wps-mcp-server) ⭐⭐⭐⭐⭐

**项目描述**: 基于 Model Context Protocol 的 WPS 表格集成服务器，让 AI 应用 (Claude Desktop 等) 直接查询和操作企业云表格数据  
**我的角色**: 独立开发者  
**项目时间**: 2025年 (已发布 npm)  

**核心贡献**:
- **MCP协议实现**: 完整实现 MCP 标准，支持 stdio 和 HTTP/SSE 双传输模式
- **工具集设计**: 设计 `search`、`batch_search`、`get_table_list`、`get_image_urls` 等 AI 可调用工具
- **多配置管理**: 支持多 Webhook 配置，一套服务连接多个 WPS 表格
- **npm发布**: 包 `jim-wps-mcp-server` 已发布，支持 `npx` 一键运行
- **开源生态**: 为 AI + 办公自动化场景提供了标准化的连接方案

**技术栈**: TypeScript, Node.js, MCP Protocol, WPS AirScript, npm

---

### 3. 云表格快速查找 SaaS (wps-database-websearch) ⭐⭐⭐⭐⭐

**项目描述**: 全栈云表格搜索管理平台，集中管理 WPS/Google Sheets 脚本令牌，支持跨表多条件搜索、分享分发和 MCP 配置生成  
**我的角色**: 全栈开发者 & 产品设计  
**项目时间**: 2025年  

**核心贡献**:
- **全栈SaaS架构**: Next.js 16 App Router + Supabase (Auth + PostgreSQL + RLS行级安全)
- **跨表搜索引擎**: 多条件 AND 搜索、批量搜索、自动分批回退、增量结果流式展示
- **Token管理系统**: 脚本令牌集中管理、分享码安全分发、权限控制 (view/use)、过期时间
- **用户系统**: 注册登录、角色管理 (user/admin)、账户激活、登录日志、使用统计
- **MCP配置生成**: 一键生成选中 Token 的 MCP 配置 JSON
- **AirScript生态**: 提供多维表格/智能表格的只读查询与编辑脚本模板

**技术栈**: Next.js 16, React 19, TypeScript, Tailwind CSS v4, Supabase, ExcelJS, Vercel

---

### 4. OH-MindMirror — AI 心理投射工具 ⭐⭐⭐⭐

**项目描述**: 基于 OH 卡牌原理的数字疗愈应用，结合 AI 引导用户进行潜意识探索与自我对话  
**我的角色**: 产品设计 & 全栈开发  
**项目时间**: 2025年 (公开项目)  

**核心贡献**:
- **AI集成**: 接入 Gemini API 实现智能对话引导，根据卡牌组合生成个性化探索方向
- **产品创新**: 将心理学 OH 卡牌投射原理数字化，融合专业量表与大模型能力
- **前端架构**: React + TypeScript + Vite 构建，响应式设计
- **用户体验**: 精心设计卡牌交互、引导式对话流程、结果可视化

**技术栈**: React, TypeScript, Vite, Gemini API

---

### 5. TeleChat — Telegram AI 智能语音机器人 ⭐⭐⭐⭐

**项目描述**: 集成 DeepSeek AI 推理与 MiniMax 语音合成的 Telegram 机器人，提供智能文本+语音双通道交互  
**我的角色**: 独立开发者  
**项目时间**: 2024年 - 2025年 (公开项目)  

**核心贡献**:
- **多AI服务编排**: DeepSeek (文本推理) + MiniMax TTS (语音合成) + Moonshot (多模型切换)
- **工程化部署**: Docker 容器化、离线部署包、一键部署脚本、自动重启
- **会话管理**: 用户级配置管理、多语音角色切换、上下文记忆
- **可观测性**: 完整的操作日志、错误追踪、文件管理

**技术栈**: Node.js, DeepSeek API, MiniMax TTS, Docker, Telegram Bot API

---

### 6. Everything Proxy Service (tmtImageServer) ⭐⭐⭐⭐

**项目描述**: Everything 文件搜索引擎的安全代理服务，增强用户认证、访问日志、路径混淆和 GUI 管理界面  
**我的角色**: 系统架构师 & 全栈开发  
**项目时间**: 2025年  

**核心贡献**:
- **安全增强层**: 用户认证系统、Session管理、路径混淆防目录结构泄露
- **管理GUI**: 实时服务状态监控、用户管理、访问日志查看、系统配置面板
- **双数据库支持**: SQLite (本地开发) + PostgreSQL (生产环境) 无缝切换
- **自动更新**: GitHub 私有仓库版本检查、安全回滚、备份机制
- **FRP穿透**: 内置 Fast Reverse Proxy 支持远程访问

**技术栈**: Python, Flask, PyQt5, SQLite, PostgreSQL, FRP

---

### 7. WPS 企业自动化工具集 (tmtPartWps) ⭐⭐⭐⭐

**项目描述**: 基于 WPS 多维表格的企业级自动化解决方案，涵盖报价系统、库存管理、编码转换和标签打印  
**我的角色**: 产品设计 & 开发  
**项目时间**: 2024年 - 2025年  

**核心贡献**:
- **报价系统**: 智能增量备份、按编号去重、关联字段转换、分页处理大数据量
- **库存管理**: 批量入库/出库、采购状态自动更新、仓库订单状态同步
- **标签打印服务**: Bartender HTTP API 集成、CSV数据处理、多线程打印、实时日志
- **数据标准化**: 配件编码查重、OE码转换、转换码数据整合、品牌编码映射

**技术栈**: WPS AirScript (JavaScript), Python, Flask, Bartender SDK

---

### 8. 星海方舟 — 太空探索放置游戏 (aquor-space-site-game) ⭐⭐⭐⭐

**项目描述**: 宇宙方舟主题的太空探索放置类网页游戏，包含10种资源、4个星域、科技树、巨型工程和声望系统  
**我的角色**: 独立全栈开发  
**项目时间**: 2025年  

**核心贡献**:
- **复杂游戏系统**: 资源采集、星系跃迁、方舟舱室升级、科技研究、物质合成(EMC)、巨型工程、声望重置
- **状态管理**: 基于 Zustand 的完整游戏循环引擎 (tick / 自动存档)
- **云端集成**: Supabase 邮箱认证、云端存档、基于服务器时间戳的离线收益 (防作弊)
- **国际化**: 中英双语 i18n 支持
- **测试覆盖**: 早期节奏、离线收益、最优路径、进度曲线等单元测试

**技术栈**: React 18, TypeScript, Vite 6, Tailwind CSS, Zustand, Supabase, Vitest

---

### 9. 批量水印工具 (put-watermark-web) ⭐⭐⭐

**项目描述**: 纯前端批量图片加水印工具，所有处理在浏览器本地完成，支持文本/图片水印和 ZIP 打包下载  
**我的角色**: 独立开发  
**项目时间**: 2025年 (公开项目)  

**核心贡献**:
- **隐私优先**: 图片处理完全在浏览器完成，不上传服务器
- **Docker部署**: 多阶段构建 (Node构建 + Nginx静态服务)，一键私有化部署
- **灵活配置**: 文本/图片水印、平铺/居中、字号颜色角度不透明度全面可调

**技术栈**: Vite, JavaScript, Docker, Nginx

---

### 10. 七牛云鉴权服务 (qiniuyun-upload-auth) ⭐⭐⭐

**项目描述**: 七牛云对象存储鉴权 HTTP 服务，支持上传凭证生成、私有下载地址、回调签名验证  
**我的角色**: 独立开发  
**项目时间**: 2025年  

**核心贡献**:
- **完整鉴权链路**: 上传凭证、私有下载URL、回调验证 (QBox/Qiniu)、任意请求签名
- **Docker容器化**: 环境变量配置密钥，安全运行
- **API文档**: FastAPI 自动生成 Swagger 文档

**技术栈**: Python, FastAPI, uvicorn, Docker, 七牛云SDK

---

## 近期项目整合实践（2025–2026）

近一年，我将一线业务知识、数据资产与 AI 能力系统性整合，落地了 30+ 个企业级项目（多数为私有），形成六条可复用的能力主线：

### 1. 外贸销售 AI 中台

从阿里国际站（ICBU）、WhatsApp、邮件、飞书等多源实时采集客户会话与画像，本地增量归档、跨销售按手机号去重形成「客户公海」，再由 AI Skill 完成翻译、分级、深度背调、话术起草与跟进提醒，让销售团队共享同一份客户认知。

**代表项目**: icbu-tm-daily（多模式增量拉取 + FTS5 全文检索 + 客户分层仪表盘）、tm-msg-archive（Hub + Agent 局域网归档，零依赖纯标准库）、whatsapp-msg-reading（浏览器扩展 + 本地备份 + 客户公海聚合）、toomotoo-sale.skill（七大能力销售助手）、emailAutoProcess、feishu-ai-groupchat（飞书群聊 AI 托管平台）

### 2. 报价与多源数据一致性

用本地服务复算全部报价公式替代云端文档查询，保证报价、库存、订单口径一致；订单自动转换为商业发票、装箱单、报关单等专业单据，消除人工转录。

**代表项目**: kdocs.toomotoo.online（Next.js 15 + FastAPI 计算引擎 + SQLite）、tmtPartWps、partsdb、tmt-mapping、orderListForSale

### 3. 多品牌配件数据逆向与检索

逆向解析 Crown（PSRT5 / SQL Server）、Jungheinrich（Jeti）、Linde（Service Guide）等品牌配件数据，统一为可扩展的多品牌检索目录，后端承载千万级记录并支持毫秒级查询。

**代表项目**: ForkliftPartsData（FastAPI + SQLite + Vue 3，三品牌适配器）、linkImgDataProcess（千万级记录分布式系统）、parts-catalog-pdf-to-xlsx（矢量 PDF 图文转 XLSX）

### 4. 图像与文档批处理流水线

把背景替换、条码识别命名、OCR 采集、图片分类、PDF 原位翻译等人工重复操作，做成一次投入、长期复用的脚本流水线。

**代表项目**: webPicProcessTMT、hongT-pic-process、ocrMulti、picReadOcr、xlsxImageOutput、classify_images、bgremove-zbar-rename、pdf-inplace-translate.skill

### 5. 自托管基础设施

让整套系统可私有化、可远程运维：Caddy / FRP 站点与隧道管理面板、统一邮箱验证码鉴权与跨子域 SSO、文件搜索安全代理、内网服务编排。

**代表项目**: server-windows、tmtImageServer、tmt-blog、nocobase、teable-tool

### 6. AI 应用与心理探索产品

在业务系统之外，把 AI 能力延伸到心理探索与关系联结场景，探索 AI + 人文的结合点。

**代表项目**: companion-text-adventure-game（灵魂镜子 · 多人 AI 关系探索对话游戏）、aquor-space-site-game（星海方舟太空放置游戏）、OH-MindMirror、know-yourself-tools、soul-mirror-with-other.skill

---

## 专业特长与核心竞争力

### AI协作专长

- **AI工具精通**: 深度掌握 Claude Code、ChatGPT、DeepSeek 等主流AI工具，擅长复杂提示工程
- **MCP生态先行者**: 独立开发并发布 MCP 工具服务器，打通 AI 与企业办公数据的连接
- **需求转化能力**: 将模糊业务需求精确转化为AI可执行的技术方案
- **多模态AI应用**: 语音合成 (TTS)、文本推理、图像识别、心理对话等多领域AI集成经验
- **协作流程设计**: 创建高效的人机协作工作流，最大化AI生产力

### 商业价值创造

- **数字化转型专家**: 通过AI工具将传统业务流程数字化，效率提升 300%+
- **成本优化**: LINK项目通过分布式架构改造，减少 67% 人力成本 (6人→2人)
- **海量数据处理**: 2000万+配件记录的分布式系统设计与性能优化经验
- **全栈交付能力**: 从前端到后端、从桌面到云端、从开发到部署的完整技术闭环
- **跨行业经验**: 外贸、制造、内容管理、心理健康、游戏等多领域的数字化实践

---

## 技术水平评估

### 核心能力评分 (1-10分)

| 能力领域           | 评分 | 代表项目                              | 市场竞争力 |
| ------------------ | ---- | ------------------------------------- | ---------- |
| AI工具协作         | 9/10 | 所有项目均通过AI协作实现              | 极强       |
| 全栈开发           | 8/10 | 云表格SaaS, 星海方舟, WPS MCP Server  | 强         |
| 系统架构设计       | 9/10 | 海量配件数据库 (2000万+记录)          | 极强       |
| 业务流程优化       | 9/10 | WPS自动化工具集, orderListForSale     | 极强       |
| AI服务集成         | 8/10 | TeleChat, OH-MindMirror, imageToVideo | 强         |
| 跨行业理解         | 9/10 | 外贸、制造、心理健康、游戏等领域      | 极强       |

---

## 职位适配度分析

### 最适合岗位 (95%+ 匹配度)

- **AI产品经理 / AI解决方案架构师**: MCP生态构建、AI服务集成、产品全流程经验
- **全栈工程师**: React/Next.js + Python/Flask + 数据库 + Docker 全栈能力
- **数字化转型专家**: 企业业务流程AI化改造、海量数据处理经验
- **技术负责人 / Tech Lead**: 从单体到分布式的架构演进、团队协作工具建设

### 目标行业方向

- **AI/大模型公司**: MCP工具开发、AI应用集成、Prompt工程经验
- **企业服务/SaaS**: 全栈SaaS产品开发、Supabase/PostgreSQL经验
- **跨境电商/外贸**: 行业深度理解和完整的数字化改造成功案例
- **咨询/数字化服务**: 跨行业AI解决方案设计和实施经验

---

## 项目组合总结

### 项目统计

- **核心项目**: 60 个项目（含 33 个企业级私有项目），涵盖分布式系统、SaaS平台、AI应用、AI Skill、企业自动化、桌面工具、浏览器插件、Web游戏等领域
- **技术广度**: TypeScript, React, Next.js, Vue 3, Python, Flask, FastAPI, Node.js, PostgreSQL, SQLite, Redis, Elasticsearch, Supabase, Docker, PyQt5 等现代化技术栈
- **开源贡献**: TeleChat, OH-MindMirror, put-watermark-web, jim-wps-mcp-server, soul-mirror-with-other.skill 等多个公开项目
- **npm生态**: jim-wps-mcp-server 已发布至 npm registry
- **时间跨度**: 2024年至今，持续活跃的项目开发与AI协作实践
- **商业价值**: 多个项目带来显著的效率提升和成本降低

### 代表性成就

- **海量配件数据库系统**: 2000万+记录、1000+并发、查询提速10-50倍的分布式架构
- **WPS MCP Server**: npm发布的AI工具服务器，连接AI与企业办公数据
- **云表格快速查找SaaS**: Next.js 16 + Supabase 全栈产品，完整的用户/权限/分享体系
- **TeleChat**: DeepSeek + MiniMax TTS 多AI服务编排的智能语音机器人
- **OH-MindMirror**: AI驱动的心理投射工具，探索AI+心理健康新场景
- **星海方舟**: 复杂游戏系统的独立全栈实现，展现产品设计与工程能力
- **外贸销售 AI 中台**: 多源客户会话采集 + 客户公海去重 + AI Skill 全链路辅助，销售团队共享客户认知
- **报价一致性系统**: 本地复算全部报价公式，打通报价 / 库存 / 订单口径，并自动生成报关单据

---

*基于 60 个项目（含 33 个企业级私有项目）和持续的全栈开发实践，我的差异化在于「整合」：把行业 Know-how、数据资产、AI 能力与工程交付串成闭环。既具备企业级分布式系统架构能力、AI 生态（MCP / Skill）构建经验和完整的产品全栈交付能力，也具备把一线业务知识沉淀为可复用系统的落地经验，在企业数字化转型与 AI 解决方案领域具有强劲市场竞争力。*
