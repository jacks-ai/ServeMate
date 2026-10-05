# ServeMate


> 基于 Agentic RAG 的电商客服智能体：混合检索支撑售后政策问答与溯源，Agent 调用 MCP 工具查询订单、办理售后，写操作人工确认，支持跨会话续办。


## 技术栈

### 后端

- Java 17
- Spring Boot 3.5.x
- MyBatis-Plus
- Redisson
- RocketMQ
- Milvus 2.6.x
- Apache Tika

### 前端

- React 18
- TypeScript
- Vite
- Tailwind CSS

### 模块划分

- `bootstrap`：业务入口与核心应用编排
- `framework`：通用基础设施、约定与 Trace 能力
- `infra-ai`：Embedding、Rerank、LLM、Token 等 AI 基础能力
- `mcp-server`：MCP 工具服务与协议适配
- `frontend`：Web 前端与管理后台

## 快速启动

### 1. 基础环境

- JDK 17+
- Maven 3.9+
- Node.js 18+
- PostgreSQL
- Redis
- Milvus
- RocketMQ

### 2. 启动后端

```bash
./mvnw spring-boot:run -pl bootstrap
```

默认后端地址为 `http://localhost:9090/api/page-seek`。

### 3. 启动前端

```bash
cd frontend
npm install
npm run dev
```

前端开发服务器默认通过 Vite 启动，本地代理可转发到后端接口。

### 4. 准备知识库

建议按以下顺序体验：

1. 创建知识库
2. 上传文档
3. 执行分块与索引构建
4. 在问答页围绕内容发起多轮问题
5. 在后台查看 Chunk、Trace 与检索结果

