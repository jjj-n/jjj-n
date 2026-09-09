<!-- markdownlint-disable MD013 MD033 MD041 -->

<div align="center">
  <h1>你好，我是 jjj-n 👋</h1>
  <p><strong>Java Backend Developer · AI Agent / RAG Engineering</strong></p>
  <p>关注异步任务、缓存与消息可靠性，以及 AI Agent 的工程化落地</p>
  <p>
    <img alt="Java 21" src="https://img.shields.io/badge/Java-21-E76F00?style=flat-square&logo=openjdk&logoColor=white">
    <img alt="Spring Boot" src="https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=flat-square&logo=springboot&logoColor=white">
    <img alt="MySQL 8" src="https://img.shields.io/badge/MySQL-8-4479A1?style=flat-square&logo=mysql&logoColor=white">
    <img alt="Redis 7" src="https://img.shields.io/badge/Redis-7-DC382D?style=flat-square&logo=redis&logoColor=white">
    <img alt="RocketMQ 5" src="https://img.shields.io/badge/RocketMQ-5-D77310?style=flat-square">
    <img alt="Docker Compose" src="https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker&logoColor=white">
  </p>
</div>

## 👨‍💻 关于我

- **主要技术：** Golang、gRPC、Java、Spring Boot、MySQL、Redis、RocketMQ
- **工程方向：** 异步任务、幂等与去重、限流、任务恢复、可观测性
- **AI 方向：** LangChain4j、RAG、Agent Loop、多模态内容处理
- **近期实践：** 持续参与 Java 与 AI 基础设施相关开源项目

## 🚀 代表项目

### [DoVideoAI · 长视频内容理解 Agent](https://github.com/jjj-n/DoVideoAI)

> 将视频转化为可检索、可追溯、可继续追问的结构化知识。

- **可靠任务链路：** 使用分片上传、断点续传和 RocketMQ 异步消费处理长耗时任务
- **并发与成本控制：** 通过 Redis 去重、Redisson 锁、限流与失败重试保障任务执行
- **多模态上下文：** 融合 ASR、OCR、关键帧与时间戳，构建统一的 `VideoContext`
- **证据约束 Agent：** 由 Planner、Executor、Critic 组成 Agent Loop，约束模型输出
- **恢复与验证：** 通过 MySQL Checkpoint 与 Redis 热缓存恢复任务，并公开评测局限

**技术栈：** Java 21 · Spring Boot · MySQL · Redis · RocketMQ · MinIO ·
Qdrant · LangChain4j · FFmpeg · Vue 3

## 🌱 代表性开源贡献

| 项目 | 贡献 | 状态 |
| --- | --- | --- |
| [ArcadeDB #6973](https://github.com/ArcadeData/arcadedb/pull/6973) | 修复稀疏图遍历中 `CountOps` 对 provider node ID 的处理 | ✅ Merged |
| [DSpace #13021](https://github.com/DSpace/DSpace/pull/13021) | 收紧 collection item template 的授权边界并补充测试 | ✅ Merged |
| [Kroxylicious #4739](https://github.com/kroxylicious/kroxylicious/pull/4739) | 移除 AWS KMS 中已废弃的长期凭据与 EC2 metadata 凭据配置 | ✅ Merged |
| [OpenSearch k-NN #3508](https://github.com/opensearch-project/k-NN/pull/3508) | 修复 `RescoreKnnVectorQueryTests.testRescoreQuery` 的不稳定测试 | ✅ Merged |

更多记录见我的 [Pull Requests](https://github.com/search?q=author%3Ajjj-n+is%3Apr&type=pullrequests)。

## 🧩 扩展项目

### [Learn Claude Code Java Plus](https://github.com/jjj-n/learn-claude-code-java-plus)

基于以下项目进行二次开发：
[Chris-debug-0225/learn-claude-code-java](https://github.com/Chris-debug-0225/learn-claude-code-java)。
在这个 Java Coding Agent 学习项目中，逐步验证权限控制与工具调用设计。

- 实现 `ALLOW / DENY / ASK` 三态权限决策与多来源规则合并
- 支持 Bash 复合命令拆分、通配规则匹配与工具执行前权限闸门
- 修复第三方模型兼容、配置目录、Todo Schema 和上下文压缩等问题
- 保持与上游渐进式教学结构兼容，并补充单元测试

## 🛠️ 技术栈

<details>
<summary><strong>展开查看完整技术栈</strong></summary>

### 后端

Golang · gRPC · Java · Spring Boot · MySQL · Redis · RocketMQ · Redisson

### 工程

JUnit · Testcontainers · Docker Compose · GitHub Actions

### AI 与前端

LangChain4j · RAG · Qdrant · FFmpeg · Vue 3

</details>
