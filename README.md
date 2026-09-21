<!-- markdownlint-disable MD013 MD033 MD041 -->

<div align="center">
  <h1>你好，我是 jjj-n 👋</h1>
  <p><strong>AI 应用开发 · Go / Java 后端</strong></p>
  <p>关注 Agent、RAG 与流式交互，也关注支撑它们的并发、缓存和任务可靠性。</p>
  <p>
    <img alt="Go" src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&amp;logo=go&amp;logoColor=white">
    <img alt="Java" src="https://img.shields.io/badge/Java-E76F00?style=flat-square&amp;logo=openjdk&amp;logoColor=white">
    <img alt="gRPC" src="https://img.shields.io/badge/gRPC-244C5A?style=flat-square">
    <img alt="Spring Boot" src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&amp;logo=springboot&amp;logoColor=white">
    <img alt="Redis" src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&amp;logo=redis&amp;logoColor=white">
    <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&amp;logo=docker&amp;logoColor=white">
  </p>
</div>

## 关于我

2027 届软件工程本科生，正在从事 AI 应用开发实习，使用 Go 和 Java 构建后端服务与 AI 应用。

- Go 实践：语音 Agent、gRPC 流式交互、工具调用与执行可靠性。
- Java 实践：基于 Spring Boot 构建长视频理解应用，处理异步任务、缓存、消息消费与断点恢复。
- AI 工程：Agent 编排、Function Calling、RAG、证据校验与回归评测。
- 开源参与：向 Go、Java 及 AI 相关项目提交功能改进、缺陷修复和回归测试。

## 代表性开源贡献

以下 PR 均已合并。这里选取与 AI 应用和后端工程相关的贡献，完整记录见 [Pull Requests](https://github.com/search?q=author%3Ajjj-n+is%3Apr&type=pullrequests)。

| 项目 | 方向 | 贡献 |
| --- | --- | --- |
| [Tencent WeKnora #3124](https://github.com/Tencent/WeKnora/pull/3124) | Go · RAG / Agent | 补齐 Agent 执行完成后的 IM 流终止信号，区分同步与异步回答的结束语义，并补充取消、错误及终态缺失回归测试。 |
| [Zalando Skipper #4251](https://github.com/zalando/skipper/pull/4251) | Go · 网关 / 缓存 | 为缓存过滤器新增 Redis 二级存储支持，适配 TTL 写入、删除、缓存未命中及 Redis / Valkey 后端选择。 |
| [ORAS Go #1349](https://github.com/oras-project/oras-go/pull/1349) | Go · 容器基础设施 | 分离 Registry 警告日志与 HTTP 调试日志，保留兼容回退，并在关闭调试日志时跳过报文格式化与响应体检查。 |
| [ArcadeDB #6973](https://github.com/ArcadeData/arcadedb/pull/6973) | Java · 图数据库 | 修复稀疏图遍历中 `CountOps` 对 provider node ID 的处理。 |
| [DSpace #13021](https://github.com/DSpace/DSpace/pull/13021) | Java · 访问控制 | 收紧 collection item template 的授权边界，并补充回归测试。 |
| [OpenSearch k-NN #3508](https://github.com/opensearch-project/k-NN/pull/3508) | Java · 向量检索测试 | 修复 `RescoreKnnVectorQueryTests.testRescoreQuery` 的不稳定测试。 |

## 代表项目

### [DoVideoAI · 长视频内容理解 Agent](https://github.com/jjj-n/DoVideoAI)

面向长视频内容理解，将 ASR、OCR 与时间戳证据组织为可检索、可追溯、可继续追问的结构化知识。

- 异步任务与并发控制：分片上传与断点续传，RocketMQ 异步消费，结合 Redis 去重、Redisson 锁与限流控制重复执行和调用成本。
- 多模态内容处理：ASR / OCR 双路并行，融合语音、画面文字、关键帧与时间戳，构建统一的 `VideoContext`。
- 检索与 Agent 编排：结合关键词与向量检索，通过 Planner–Executor–Critic 工作流生成结论、检查证据并定向补检。
- 恢复与评测：使用 MySQL Checkpoint 与 Redis 热缓存恢复任务；公开评测方法、数据集说明和适用边界。

**技术栈：**Java 21 · Spring Boot · MySQL · Redis · RocketMQ · MinIO · Qdrant · LangChain4j · FFmpeg · Vue 3

[查看项目与运行说明](https://github.com/jjj-n/DoVideoAI) · [查看评测方法与结果](https://github.com/jjj-n/DoVideoAI/tree/master/benchmark)

### [Learn Claude Code Java Plus · Coding Agent 学习与扩展](https://github.com/jjj-n/learn-claude-code-java-plus)

基于 [Chris-debug-0225/learn-claude-code-java](https://github.com/Chris-debug-0225/learn-claude-code-java) 二次开发，在 Java Coding Agent 中实践工具调用与权限控制。

- 实现 `ALLOW / DENY / ASK` 三态权限决策与多来源规则合并。
- 支持 Bash 复合命令拆分、通配规则匹配与工具执行前权限检查。
- 修复第三方模型兼容、配置目录、Todo Schema 和上下文压缩等问题，并补充单元测试。

## 技术与实践

| 方向 | 使用与实践 |
| --- | --- |
| Go 后端 | goroutine / channel、gRPC、流式服务、并发取消、数据竞争检测 |
| Java 后端 | Java、Spring Boot、并发处理、JUnit、Testcontainers |
| AI 应用 | Agent 编排、Function Calling、RAG、Qdrant、LangChain4j、ASR / LLM / TTS 链路集成 |
| 数据与任务 | MySQL、PostgreSQL、Redis、RocketMQ、幂等与去重、重试与断点恢复 |
| 工程工具 | Git、Linux、Docker Compose、GitHub Actions、日志排查与回归测试 |
