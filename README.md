<div align="center">
  <h1>StudySolo</h1>
  <p>AI 学习工作流编排平台 - 个人学习版</p>
</div>

---

> **基于 [AIMFllys/StudySolo](https://github.com/AIMFllys/StudySolo) 二次开发**
>
> 原项目为华科 AI 智能体大赛参赛作品，本仓库为其个人学习与定制版本。

---

## 项目简介

StudySolo 是一个面向学习场景的 AI 工作流编排平台。通过自然语言描述学习目标，系统自动生成多节点工作流，支持可视化编辑、流式执行和社区共享。

**核心能力：**
- 自然语言驱动工作流生成
- 可视化节点画布拖拽编辑
- 18 种专业学习节点
- 多平台 AI 模型路由
- SSE 流式执行追踪

## 技术栈

| 层级 | 技术 |
| :--- | :--- |
| 前端 | Next.js 16 + React 19 + TypeScript |
| 画布 | @xyflow/react (React Flow) |
| 后端 | Python 3.11 + FastAPI |
| 数据库 | Supabase (PostgreSQL) |
| 部署 | 阿里云 ECS + Nginx + PM2 |

## 快速开始

### 前端

```bash
cd frontend
pnpm install
cp .env.example .env.local
pnpm dev
# http://localhost:2037
```

### 后端

```bash
cd backend
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
uvicorn app.main:app --reload --port 2038
```

## 仓库结构

```
StudySolo-Dev/
├── frontend/          # Next.js 前端
├── backend/           # FastAPI 后端
├── agents/            # Agent 微服务
├── introduce/         # 产品介绍页
├── shared/            # 共享模块
├── supabase/          # 数据库迁移
└── docs/              # 文档
```

## 开发说明

本仓库用于个人学习和二次开发，将持续根据自己的理解进行定制和优化。

---

## 致谢

原项目由 [AIMFllys](https://github.com/AIMFllys) 团队开发，本项目在其基础上进行学习和定制。

## License

[MIT License](./LICENSE) - 保留原作者署名
