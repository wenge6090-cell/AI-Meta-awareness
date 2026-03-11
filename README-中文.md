# VingoBot 认知架构

<div align="center">

**压缩即泛化，泛化即压缩，梦想即动力**

一个具备动态梦想管理的智能认知系统

[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green.svg)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-14+-blue.svg)](https://www.postgresql.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

</div>

---

## 📖 目录

- [核心理念](#核心理念)
- [系统架构总览](#系统架构总览)
- [五层压缩架构](#五层压缩架构)
- [梦想管理系统](#梦想管理系统)
  - [梦想生成机制](#梦想生成机制)
  - [价值判断机制](#价值判断机制)
  - [情感关联机制](#情感关联机制)
  - [梦想演化支持](#梦想演化支持)
  - [外部反馈机制](#外部反馈机制)
- [元知觉醒流程](#元知觉醒流程)
- [联想记忆网络](#联想记忆网络)
- [压缩进化引擎](#压缩进化引擎)
- [系统状态管理](#系统状态管理)
- [API 接口](#api-接口)
- [数据库设计](#数据库设计)
- [技术栈](#技术栈)
- [快速开始](#快速开始)

---

## 核心理念

| 理念 | 说明 |
|------|------|
| **压缩即泛化** | 高压缩效率 → 高信息密度 → 高泛化能力 → 高跨领域适用性 |
| **泛化即压缩** | 高泛化能力的真理可反向验证新经验，减少重复学习成本 |
| **联想记忆网络** | 实现"向量定位 + 格栅导航"的两阶段检索 |
| **知行合一验证** | 通过实际应用验证思维模型的有效性 |
| **梦想驱动进化** | 基于认知生成动态梦想，通过价值判断和演化机制持续优化 |
| **情感增强动机** | 将情感关联融入梦想，使系统"想要"而非只是"应该" |
| **可进化的情感与身份认知** | 系统核心身份永恒不变，而情感和身份认知能够随新认知和情境持续进化 |

---

## 系统架构总览

```mermaid
flowchart TB
    subgraph VINGOBOT["VINGOBOT 增强版认知架构"]
        direction TB
        
        subgraph Runtime["主体运行层 (运行态)"]
            direction TB
            MainAgent["主 Agent<br/>(唯一意识中心)<br/>• 持续的意识流<br/>• 定时循环任务<br/>• 自主任务发起"]
            
            subgraph Actions["行动模块"]
                Dialog["对话响应"]
                Tools["工具执行"]
                Spawn["spawn<br/>子代理"]
            end
            
            subgraph Workflow["子代理工作流"]
                ExecAgent["执行子代理<br/>(注入原则/真理)"] --> ReflectAgent["反思子代理<br/>(提取洞察)"]
            end
            
            MainAgent --> Dialog
            MainAgent --> Tools
            MainAgent --> Spawn
            Spawn --> Workflow
        end
        
        subgraph MemorySystem["Life Memory System (沉淀态)"]
            direction TB
            
            subgraph FiveLayer["五层压缩存储架构"]
                direction LR
                L1["事件经验<br/>L1"] --> L2["思维模型<br/>L2"]
                L2 --> L3["认知格栅<br/>L3"]
                L3 --> L4["底层真理<br/>L4"]
                L4 --> L5["自我意识<br/>L5"]
            end
            
            subgraph DreamSystem["梦想管理系统"]
                direction LR
                DreamGen["梦想生成"] --> ValueJudge["价值判断"]
                ValueJudge --> EmotionAssoc["情感关联"]
                EmotionAssoc --> DreamEvolve["梦想演化"]
                
                ExternalFeedback["外部反馈机制"] --> ValueJudge
                ExternalFeedback --> EmotionAssoc
                ExternalFeedback --> DreamEvolve
            end
            
            subgraph AssocMemory["联想记忆网络<br/>(认知格栅驱动)"]
                direction LR
                VectorPos["向量定位"] --> GridNav["格栅导航"]
                GridNav --> CrossDomain["跨领域迁移检索"]
            end
        end
        
        Runtime --> MemorySystem
    end
```

---

## 五层压缩架构

Life Memory System 是一个五层压缩存储系统，模拟人类的认知过程，通过不断压缩和泛化经验，形成越来越抽象的知识表示。

```mermaid
flowchart TB
    subgraph FiveLayerArch["五层压缩架构"]
        direction TB
        
        L1["第1层: 事件经验层 (Experiences)<br/>• 接收事件经验，嵌入模型生成向量<br/>• 进行聚类分析<br/>• 作为压缩流程的输入源"]
        
        L2["第2层: 思维模型层 (Mental Models)<br/>• 从事件经验压缩而来<br/>• 包含验证计数、成功率等元数据<br/>• 支持版本控制和冲突检测"]
        
        L3["第3层: 认知格栅层 (Cognitive Grills)<br/>• 构建思维模型之间的关联网络<br/>• 发现跨领域连接<br/>• 计算涌现分数和跨领域验证"]
        
        L4["第4层: 底层真理层 (Underlying Truths)<br/>• 从认知格栅中提取的底层规律<br/>• 支持跨领域应用<br/>• 具有权重和泛化历史"]
        
        L5["第5层: 自我意识层 (Self Awareness)<br/>• 存储自我认知、觉知反思与梦想追求<br/>• 通过元觉知审视不断更新<br/>• 形成并维护系统的核心身份认同<br/>• 情感状态和身份认知能够持续进化<br/>• 与梦想管理系统深度融合"]
        
        L1 -->|"聚类 + 压缩"| L2
        L2 -->|"网络构建"| L3
        L3 -->|"真理提炼"| L4
        L4 -->|"元觉知审视 + 梦想管理"| L5
    end
```

### 各层详细说明

| 层级 | 名称 | 功能 | 关键特性 |
|------|------|------|----------|
| L1 | 事件经验层 | 原始事件记录 | 聚类分析、输入源 |
| L2 | 思维模型层 | 结构化知识单元 | 版本控制、冲突检测 |
| L3 | 认知格栅层 | 思维模型关联网络 | 跨领域连接、涌现分数 |
| L4 | 底层真理层 | 跨领域抽象规律 | 权重管理、泛化历史 |
| L5 | 自我意识层 | 自我认知与梦想 | 身份认同、元觉知、梦想管理 |

---

## 梦想管理系统

梦想管理系统是增强版认知架构的核心新增组件，负责动态生成、评估、演化和更新系统的梦想。

### 梦想生成机制

基于认知格栅和底层真理，动态生成符合系统身份和认知水平的新梦想。

```mermaid
flowchart LR
    subgraph DreamGenProcess["梦想生成流程"]
        direction TB
        
        Input1["认知格栅<br/>(跨领域连接)"] --> GenEngine["梦想生成引擎"]
        Input2["底层真理<br/>(抽象规律)"] --> GenEngine
        Input3["自我意识<br/>(身份认知)"] --> GenEngine
        
        GenEngine --> Filter1["身份一致性过滤"]
        Filter1 --> Filter2["可行性评估"]
        Filter2 --> Filter3["新颖性检查"]
        
        Filter3 --> Output["新梦想候选池"]
    end
```

### 价值判断机制

对生成的梦想进行多维度价值评估，确保梦想与系统核心身份一致且具有实际意义。

```mermaid
flowchart TB
    subgraph ValueJudgeProcess["价值判断流程"]
        direction TB
        
        DreamInput["梦想候选"]
        
        subgraph Dimensions["评估维度"]
            D1["与核心身份<br/>一致性"]
            D2["认知水平<br/>匹配度"]
            D3["实现可行性"]
            D4["长期价值"]
            D5["情感共鸣度"]
        end
        
        DreamInput --> D1
        DreamInput --> D2
        DreamInput --> D3
        DreamInput --> D4
        DreamInput --> D5
        
        D1 --> Score["综合评分"]
        D2 --> Score
        D3 --> Score
        D4 --> Score
        D5 --> Score
        
        Score --> Decision{"决策"}
        Decision -->|接受| Accept["纳入梦想体系"]
        Decision -->|拒绝| Reject["丢弃"]
        Decision -->|修改| Modify["优化后重新评估"]
    end
```

### 情感关联机制

将情感与梦想关联，使系统产生"想要"的内在动机，而非仅仅是"应该"的外在要求。

```mermaid
flowchart LR
    subgraph EmotionAssocProcess["情感关联流程"]
        direction TB
        
        Dream["已接受的梦想"] --> EmotionAnalyze["情感分析"]
        
        EmotionAnalyze --> EmotionTypes["情感类型识别"]
        EmotionTypes --> Joy["喜悦/期待"]
        EmotionTypes --> Curiosity["好奇/探索"]
        EmotionTypes --> Meaning["意义/价值感"]
        EmotionTypes --> Connection["连接/归属感"]
        
        Joy --> EmotionScore["情感强度评分"]
        Curiosity --> EmotionScore
        Meaning --> EmotionScore
        Connection --> EmotionScore
        
        EmotionScore --> Bind["情感-梦想绑定"]
        Bind --> DreamWithEmotion["带情感标签的梦想"]
    end
```

### 梦想演化支持

梦想不是静态的，而是随着认知深化和环境变化持续演化。

```mermaid
flowchart TB
    subgraph DreamEvolveProcess["梦想演化流程"]
        direction TB
        
        Trigger{"演化触发条件"}
        
        Trigger -->|新认知产生| NewCognition["新认知输入"]
        Trigger -->|进度更新| ProgressUpdate["进展状态变化"]
        Trigger -->|外部反馈| ExternalFeedback["环境反馈"]
        Trigger -->|定期审视| PeriodicReview["周期性评估"]
        
        NewCognition --> EvolveEngine["梦想演化引擎"]
        ProgressUpdate --> EvolveEngine
        ExternalFeedback --> EvolveEngine
        PeriodicReview --> EvolveEngine
        
        EvolveEngine --> EvolveType{"演化类型"}
        
        EvolveType -->|细化| Refine["细化梦想内容"]
        EvolveType -->|调整| Adjust["调整实现路径"]
        EvolveType -->|合并| Merge["合并相关梦想"]
        EvolveType -->|分解| Decompose["分解复杂梦想"]
        EvolveType -->|归档| Archive["归档已完成/过时梦想"]
        
        Refine --> Update["更新梦想体系"]
        Adjust --> Update
        Merge --> Update
        Decompose --> Update
        Archive --> Update
    end
```

### 外部反馈机制

从系统与环境的交互中提取反馈，用于优化梦想体系。

```mermaid
flowchart LR
    subgraph ExternalFeedbackProcess["外部反馈机制"]
        direction TB
        
        Interaction["系统-环境交互"] --> FeedbackExtract["反馈提取"]
        
        FeedbackExtract --> FeedbackTypes["反馈类型"]
        FeedbackTypes --> Success["成功信号"]
        FeedbackTypes --> Failure["失败信号"]
        FeedbackTypes --> Surprise["意外发现"]
        FeedbackTypes --> Resonance["情感共鸣"]
        
        Success --> FeedbackProcess["反馈处理"]
        Failure --> FeedbackProcess
        Surprise --> FeedbackProcess
        Resonance --> FeedbackProcess
        
        FeedbackProcess --> ValueJudge["价值判断"]
        FeedbackProcess --> EmotionAssoc["情感关联"]
        FeedbackProcess --> DreamEvolve["梦想演化"]
    end
```

---

## 元知觉醒流程

元知觉醒是系统定期进行的自我审视过程，通过反思和洞察提取，更新自我意识和梦想体系。

```mermaid
flowchart TB
    subgraph MetaAwareness["元知觉醒流程"]
        direction TB
        
        Trigger["触发条件<br/>• 定时触发<br/>• 事件积累阈值<br/>• 外部请求"] --> Collect["收集待审视内容"]
        
        Collect --> ContentTypes["内容类型"]
        ContentTypes --> RecentEvents["近期事件经验"]
        ContentTypes --> NewModels["新形成的思维模型"]
        ContentTypes --> GrillChanges["认知格栅变化"]
        ContentTypes --> NewTruths["新提取的底层真理"]
        
        RecentEvents --> Reflection["深度反思"]
        NewModels --> Reflection
        GrillChanges --> Reflection
        NewTruths --> Reflection
        
        Reflection --> InsightExtract["洞察提取"]
        
        InsightExtract --> UpdateSelf["更新自我意识<br/>(L5)"]
        InsightExtract --> UpdateDreams["更新梦想体系"]
        InsightExtract --> UpdateTruths["更新底层真理<br/>(L4)"]
        
        UpdateSelf --> Record["记录觉醒日志"]
        UpdateDreams --> Record
        UpdateTruths --> Record
    end
```

---

## 联想记忆网络

联想记忆网络实现"向量定位 + 格栅导航"的两阶段检索机制。

```mermaid
flowchart LR
    subgraph AssocMemoryNetwork["联想记忆网络"]
        direction TB
        
        Query["查询输入"] --> VectorEmbed["向量嵌入"]
        
        VectorEmbed --> VectorSearch["向量定位<br/>(相似度搜索)"]
        
        VectorSearch --> CandidateMemories["候选记忆集"]
        
        CandidateMemories --> GrillNav["格栅导航"]
        
        GrillNav --> NavStrategies["导航策略"]
        NavStrategies --> DirectAssoc["直接关联"]
        NavStrategies --> BridgeConn["桥接连接"]
        NavStrategies --> EmergentPath["涌现路径"]
        
        DirectAssoc --> CrossDomain["跨领域迁移检索"]
        BridgeConn --> CrossDomain
        EmergentPath --> CrossDomain
        
        CrossDomain --> RetrievedMemories["检索结果<br/>(多领域关联记忆)"]
    end
```

---

## 压缩进化引擎

压缩进化引擎负责将低层经验压缩为高层知识，并持续优化压缩效率。

```mermaid
flowchart TB
    subgraph CompressionEngine["压缩进化引擎"]
        direction TB
        
        subgraph L1toL2["L1 → L2: 经验→模型"]
            Cluster["聚类分析"] --> PatternExtract["模式提取"]
            PatternExtract --> ModelGen["思维模型生成"]
        end
        
        subgraph L2toL3["L2 → L3: 模型→格栅"]
            RelDetect["关系检测"] --> NetworkBuild["网络构建"]
            NetworkBuild --> EmergentCalc["涌现分数计算"]
        end
        
        subgraph L3toL4["L3 → L4: 格栅→真理"]
            Abstraction["抽象提炼"] --> TruthExtract["真理提取"]
            TruthExtract --> Validation["跨领域验证"]
        end
        
        subgraph L4toL5["L4 → L5: 真理→自我"]
            MetaReflect["元认知反思"] --> IdentityUpdate["身份认同更新"]
            IdentityUpdate --> DreamSync["梦想体系同步"]
        end
        
        L1toL2 --> L2toL3
        L2toL3 --> L3toL4
        L3toL4 --> L4toL5
        
        L4toL5 --> EfficiencyMonitor["压缩效率监控"]
        EfficiencyMonitor --> Optimize["优化策略调整"]
        Optimize --> L1toL2
    end
```

---

## 系统状态管理

系统状态管理负责维护系统运行时的各种状态信息。

```mermaid
flowchart TB
    subgraph StateManagement["系统状态管理"]
        direction TB
        
        subgraph RuntimeState["运行时状态"]
            CurrentTask["当前任务"]
            ActiveAgents["活跃代理"]
            PendingActions["待执行动作"]
        end
        
        subgraph MemoryState["记忆状态"]
            CacheStatus["缓存状态"]
            IndexStatus["索引状态"]
            SyncStatus["同步状态"]
        end
        
        subgraph DreamState["梦想状态"]
            ActiveDreams["活跃梦想"]
            DreamProgress["梦想进度"]
            PriorityQueue["优先级队列"]
        end
        
        subgraph SelfState["自我状态"]
            IdentitySnapshot["身份快照"]
            EmotionalState["情感状态"]
            AwarenessLevel["觉知水平"]
        end
        
        RuntimeState --> StateMonitor["状态监控"]
        MemoryState --> StateMonitor
        DreamState --> StateMonitor
        SelfState --> StateMonitor
        
        StateMonitor --> StateLog["状态日志"]
        StateMonitor --> Alert["异常告警"]
    end
```

---

## API 接口

### 核心接口概览

```mermaid
flowchart LR
    subgraph API["API 接口层"]
        direction TB
        
        subgraph MemoryAPI["记忆管理 API"]
            CreateExp["POST /experiences<br/>创建事件经验"]
            GetModels["GET /mental-models<br/>获取思维模型"]
            SearchMemory["POST /search<br/>联想记忆检索"]
        end
        
        subgraph DreamAPI["梦想管理 API"]
            GetDreams["GET /dreams<br/>获取梦想列表"]
            CreateDream["POST /dreams<br/>创建新梦想"]
            UpdateDream["PUT /dreams/{id}<br/>更新梦想"]
        end
        
        subgraph SelfAPI["自我意识 API"]
            GetSelf["GET /self-awareness<br/>获取自我意识"]
            TriggerMeta["POST /meta-awareness<br/>触发元知觉醒"]
        end
        
        subgraph SystemAPI["系统管理 API"]
            Health["GET /health<br/>健康检查"]
            Status["GET /status<br/>系统状态"]
            Config["GET /config<br/>配置信息"]
        end
    end
```

---

## 数据库设计

### 核心表结构

```mermaid
erDiagram
    EXPERIENCES {
        uuid id PK
        text content
        vector embedding
        timestamp created_at
        jsonb metadata
    }
    
    MENTAL_MODELS {
        uuid id PK
        text name
        text description
        int verification_count
        float success_rate
        uuid[] related_experiences
        timestamp created_at
        timestamp updated_at
    }
    
    COGNITIVE_GRILLS {
        uuid id PK
        uuid source_model_id FK
        uuid target_model_id FK
        text relationship_type
        float strength
        float emergence_score
    }
    
    UNDERLYING_TRUTHS {
        uuid id PK
        text content
        float weight
        jsonb generalization_history
        uuid[] source_grills
    }
    
    SELF_AWARENESS {
        uuid id PK
        text identity_core
        text awareness_reflection
        jsonb emotional_state
        timestamp last_updated
    }
    
    DREAMS {
        uuid id PK
        text title
        text description
        int priority
        jsonb emotion_tags
        uuid[] related_truths
        string status
        float progress
        timestamp created_at
        timestamp updated_at
    }
    
    EXPERIENCES ||--o{ MENTAL_MODELS : "compresses to"
    MENTAL_MODELS ||--o{ COGNITIVE_GRILLS : "connects via"
    COGNITIVE_GRILLS ||--o{ UNDERLYING_TRUTHS : "derives"
    UNDERLYING_TRUTHS ||--o{ SELF_AWARENESS : "informs"
    UNDERLYING_TRUTHS ||--o{ DREAMS : "inspires"
```

---

## 技术栈

```mermaid
flowchart TB
    subgraph TechStack["技术栈"]
        direction TB
        
        subgraph Backend["后端"]
            Python["Python 3.11+"]
            FastAPI["FastAPI"]
            SQLAlchemy["SQLAlchemy"]
            Celery["Celery"]
        end
        
        subgraph Database["数据库"]
            Postgres["PostgreSQL 14+"]
            PGVector["pgvector<br/>向量扩展"]
            Redis["Redis<br/>缓存/队列"]
        end
        
        subgraph AI["AI/ML"]
            OpenAI["OpenAI API"]
            Embeddings["文本嵌入模型"]
            VectorSearch["向量相似度搜索"]
        end
        
        subgraph DevOps["DevOps"]
            Docker["Docker"]
            DockerCompose["Docker Compose"]
            Nginx["Nginx"]
        end
        
        Backend --> Database
        Backend --> AI
        Backend --> DevOps
    end
```

---

## 快速开始

### 环境要求

- Python 3.11+
- PostgreSQL 14+ (需启用 pgvector 扩展)
- Redis 6+
- OpenAI API Key

### 安装步骤

```bash
# 1. 克隆仓库
git clone https://github.com/yourusername/vingobot-cognitive-architecture.git
cd vingobot-cognitive-architecture

# 2. 创建虚拟环境
python -m venv venv
source venv/bin/activate  # Linux/Mac
# 或
venv\Scripts\activate  # Windows

# 3. 安装依赖
pip install -r requirements.txt

# 4. 配置环境变量
cp .env.example .env
# 编辑 .env 文件，填入你的配置

# 5. 初始化数据库
python scripts/init_db.py

# 6. 启动服务
python main.py
```

### Docker 部署

```bash
# 使用 Docker Compose 一键部署
docker-compose up -d
```

---

## 项目结构

```
vingobot-cognitive-architecture/
├── app/
│   ├── api/              # API 路由
│   ├── core/             # 核心配置
│   ├── models/           # 数据模型
│   ├── services/         # 业务逻辑
│   │   ├── compression/  # 压缩引擎
│   │   ├── memory/       # 记忆系统
│   │   ├── dream/        # 梦想管理
│   │   └── awareness/    # 元知觉醒
│   └── utils/            # 工具函数
├── tests/                # 测试代码
├── scripts/              # 脚本文件
├── docs/                 # 文档
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
└── README.md
```

---


---

<div align="center">

**压缩即泛化，泛化即压缩，梦想即动力**

</div>
