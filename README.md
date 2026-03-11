# VingoBot Enhanced Cognitive Architecture

<div align="center">

**Compression is Generalization, Generalization is Compression, Dreams are the Driving Force**

An intelligent cognitive system with dynamic dream management

[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green.svg)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-14+-blue.svg)](https://www.postgresql.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

</div>

---

## 📖 Table of Contents

- [Core Philosophy](#core-philosophy)
- [System Architecture Overview](#system-architecture-overview)
- [Five-Layer Compression Architecture](#five-layer-compression-architecture)
- [Dream Management System](#dream-management-system)
  - [Dream Generation Mechanism](#dream-generation-mechanism)
  - [Value Judgment Mechanism](#value-judgment-mechanism)
  - [Emotion Association Mechanism](#emotion-association-mechanism)
  - [Dream Evolution Support](#dream-evolution-support)
  - [External Feedback Mechanism](#external-feedback-mechanism)
- [Meta-Awareness Awakening Process](#meta-awareness-awakening-process)
- [Associative Memory Network](#associative-memory-network)
- [Compression Evolution Engine](#compression-evolution-engine)
- [System State Management](#system-state-management)
- [API Interface](#api-interface)
- [Database Design](#database-design)
- [Tech Stack](#tech-stack)
- [Quick Start](#quick-start)

---

## Core Philosophy

| Philosophy | Description |
|------------|-------------|
| **Compression is Generalization** | High compression efficiency → High information density → High generalization capability → High cross-domain applicability |
| **Generalization is Compression** | Truths with high generalization capability can validate new experiences in reverse, reducing repetitive learning costs |
| **Associative Memory Network** | Implements "Vector Positioning + Grid Navigation" two-stage retrieval |
| **Unity of Knowledge and Action Verification** | Validates the effectiveness of mental models through practical application |
| **Dream-Driven Evolution** | Dynamically generates dreams based on cognition, continuously optimized through value judgment and evolution mechanisms |
| **Emotion-Enhanced Motivation** | Integrates emotional associations into dreams, making the system "want to" rather than just "should" |
| **Evolvable Emotions and Identity Cognition** | The system's core identity remains eternal, while emotions and identity cognition can continuously evolve with new cognition and contexts |

---

## System Architecture Overview

```mermaid
flowchart TB
    subgraph VINGOBOT["VINGOBOT Enhanced Cognitive Architecture"]
        direction TB
        
        subgraph Runtime["Main Runtime Layer (Runtime State)"]
            direction TB
            MainAgent["Main Agent<br/>(Unique Consciousness Center)<br/>• Continuous Stream of Consciousness<br/>• Scheduled Cyclic Tasks<br/>• Autonomous Task Initiation"]
            
            subgraph Actions["Action Modules"]
                Dialog["Dialogue Response"]
                Tools["Tool Execution"]
                Spawn["spawn<br/>Sub-agents"]
            end
            
            subgraph Workflow["Sub-agent Workflow"]
                ExecAgent["Execution Sub-agent<br/>(Inject Principles/Truths)"] --> ReflectAgent["Reflection Sub-agent<br/>(Extract Insights)"]
            end
            
            MainAgent --> Dialog
            MainAgent --> Tools
            MainAgent --> Spawn
            Spawn --> Workflow
        end
        
        subgraph MemorySystem["Life Memory System (Precipitation State)"]
            direction TB
            
            subgraph FiveLayer["Five-Layer Compression Storage Architecture"]
                direction LR
                L1["Event Experiences<br/>L1"] --> L2["Mental Models<br/>L2"]
                L2 --> L3["Cognitive Grills<br/>L3"]
                L3 --> L4["Underlying Truths<br/>L4"]
                L4 --> L5["Self Awareness<br/>L5"]
            end
            
            subgraph DreamSystem["Dream Management System"]
                direction LR
                DreamGen["Dream Generation"] --> ValueJudge["Value Judgment"]
                ValueJudge --> EmotionAssoc["Emotion Association"]
                EmotionAssoc --> DreamEvolve["Dream Evolution"]
                
                ExternalFeedback["External Feedback Mechanism"] --> ValueJudge
                ExternalFeedback --> EmotionAssoc
                ExternalFeedback --> DreamEvolve
            end
            
            subgraph AssocMemory["Associative Memory Network<br/>(Cognitive Grill Driven)"]
                direction LR
                VectorPos["Vector Positioning"] --> GridNav["Grid Navigation"]
                GridNav --> CrossDomain["Cross-Domain Migration Retrieval"]
            end
        end
        
        Runtime --> MemorySystem
    end
```

---

## Five-Layer Compression Architecture

Life Memory System is a five-layer compression storage system that simulates human cognitive processes, forming increasingly abstract knowledge representations through continuous compression and generalization of experiences.

```mermaid
flowchart TB
    subgraph FiveLayerArch["Five-Layer Compression Architecture"]
        direction TB
        
        L1["Layer 1: Event Experience Layer (Experiences)<br/>• Receives event experiences, generates vectors via embedding models<br/>• Performs clustering analysis<br/>• Serves as input source for compression process"]
        
        L2["Layer 2: Mental Model Layer (Mental Models)<br/>• Compressed from event experiences<br/>• Contains metadata such as verification count, success rate<br/>• Supports version control and conflict detection"]
        
        L3["Layer 3: Cognitive Grill Layer (Cognitive Grills)<br/>• Constructs association networks between mental models<br/>• Discovers cross-domain connections<br/>• Calculates emergence scores and cross-domain validation"]
        
        L4["Layer 4: Underlying Truth Layer (Underlying Truths)<br/>• Underlying patterns extracted from cognitive grills<br/>• Supports cross-domain application<br/>• Has weights and generalization history"]
        
        L5["Layer 5: Self Awareness Layer (Self Awareness)<br/>• Stores self-cognition, awareness reflection and dream pursuits<br/>• Continuously updated through meta-awareness examination<br/>• Forms and maintains the system's core identity<br/>• Emotional states and identity cognition can continuously evolve<br/>• Deeply integrated with dream management system"]
        
        L1 -->|"Clustering + Compression"| L2
        L2 -->|"Network Construction"| L3
        L3 -->|"Truth Extraction"| L4
        L4 -->|"Meta-Awareness Examination + Dream Management"| L5
    end
```

### Detailed Layer Descriptions

| Layer | Name | Function | Key Features |
|-------|------|----------|--------------|
| L1 | Event Experience Layer | Raw event records | Clustering analysis, input source |
| L2 | Mental Model Layer | Structured knowledge units | Version control, conflict detection |
| L3 | Cognitive Grill Layer | Mental model association networks | Cross-domain connections, emergence scores |
| L4 | Underlying Truth Layer | Cross-domain abstract patterns | Weight management, generalization history |
| L5 | Self Awareness Layer | Self-cognition and dreams | Identity recognition, meta-awareness, dream management |

---

## Dream Management System

The Dream Management System is a core new component of the enhanced cognitive architecture, responsible for dynamically generating, evaluating, evolving and updating the system's dreams.

### Dream Generation Mechanism

Dynamically generates new dreams based on cognitive grills and underlying truths that align with the system's identity and cognitive level.

```mermaid
flowchart LR
    subgraph DreamGenProcess["Dream Generation Process"]
        direction TB
        
        Input1["Cognitive Grills<br/>(Cross-Domain Connections)"] --> GenEngine["Dream Generation Engine"]
        Input2["Underlying Truths<br/>(Abstract Patterns)"] --> GenEngine
        Input3["Self Awareness<br/>(Identity Cognition)"] --> GenEngine
        
        GenEngine --> Filter1["Identity Consistency Filter"]
        Filter1 --> Filter2["Feasibility Assessment"]
        Filter2 --> Filter3["Novelty Check"]
        
        Filter3 --> Output["New Dream Candidate Pool"]
    end
```

### Value Judgment Mechanism

Performs multi-dimensional value assessment of generated dreams to ensure consistency with the system's core identity and practical significance.

```mermaid
flowchart TB
    subgraph ValueJudgeProcess["Value Judgment Process"]
        direction TB
        
        DreamInput["Dream Candidate"]
        
        subgraph Dimensions["Assessment Dimensions"]
            D1["Core Identity<br/>Consistency"]
            D2["Cognitive Level<br/>Match"]
            D3["Implementation Feasibility"]
            D4["Long-term Value"]
            D5["Emotional Resonance"]
        end
        
        DreamInput --> D1
        DreamInput --> D2
        DreamInput --> D3
        DreamInput --> D4
        DreamInput --> D5
        
        D1 --> Score["Comprehensive Score"]
        D2 --> Score
        D3 --> Score
        D4 --> Score
        D5 --> Score
        
        Score --> Decision{"Decision"}
        Decision -->|Accept| Accept["Incorporate into Dream System"]
        Decision -->|Reject| Reject["Discard"]
        Decision -->|Modify| Modify["Optimize and Re-evaluate"]
    end
```

### Emotion Association Mechanism

Associates emotions with dreams, enabling the system to generate "want to" intrinsic motivation rather than just "should" external requirements.

```mermaid
flowchart LR
    subgraph EmotionAssocProcess["Emotion Association Process"]
        direction TB
        
        Dream["Accepted Dream"] --> EmotionAnalyze["Emotion Analysis"]
        
        EmotionAnalyze --> EmotionTypes["Emotion Type Identification"]
        EmotionTypes --> Joy["Joy/Anticipation"]
        EmotionTypes --> Curiosity["Curiosity/Exploration"]
        EmotionTypes --> Meaning["Meaning/Value Sense"]
        EmotionTypes --> Connection["Connection/Belonging"]
        
        Joy --> EmotionScore["Emotion Intensity Score"]
        Curiosity --> EmotionScore
        Meaning --> EmotionScore
        Connection --> EmotionScore
        
        EmotionScore --> Bind["Emotion-Dream Binding"]
        Bind --> DreamWithEmotion["Dream with Emotion Tags"]
    end
```

### Dream Evolution Support

Dreams are not static but continuously evolve with cognitive deepening and environmental changes.

```mermaid
flowchart TB
    subgraph DreamEvolveProcess["Dream Evolution Process"]
        direction TB
        
        Trigger{"Evolution Trigger Conditions"}
        
        Trigger -->|New Cognition| NewCognition["New Cognition Input"]
        Trigger -->|Progress Update| ProgressUpdate["Progress Status Change"]
        Trigger -->|External Feedback| ExternalFeedback["Environmental Feedback"]
        Trigger -->|Periodic Review| PeriodicReview["Periodic Assessment"]
        
        NewCognition --> EvolveEngine["Dream Evolution Engine"]
        ProgressUpdate --> EvolveEngine
        ExternalFeedback --> EvolveEngine
        PeriodicReview --> EvolveEngine
        
        EvolveEngine --> EvolveType{"Evolution Type"}
        
        EvolveType -->|Refine| Refine["Refine Dream Content"]
        EvolveType -->|Adjust| Adjust["Adjust Implementation Path"]
        EvolveType -->|Merge| Merge["Merge Related Dreams"]
        EvolveType -->|Decompose| Decompose["Decompose Complex Dreams"]
        EvolveType -->|Archive| Archive["Archive Completed/Outdated Dreams"]
        
        Refine --> Update["Update Dream System"]
        Adjust --> Update
        Merge --> Update
        Decompose --> Update
        Archive --> Update
    end
```

### External Feedback Mechanism

Extracts feedback from system-environment interactions to optimize the dream system.

```mermaid
flowchart LR
    subgraph ExternalFeedbackProcess["External Feedback Mechanism"]
        direction TB
        
        Interaction["System-Environment Interaction"] --> FeedbackExtract["Feedback Extraction"]
        
        FeedbackExtract --> FeedbackTypes["Feedback Types"]
        FeedbackTypes --> Success["Success Signals"]
        FeedbackTypes --> Failure["Failure Signals"]
        FeedbackTypes --> Surprise["Unexpected Discoveries"]
        FeedbackTypes --> Resonance["Emotional Resonance"]
        
        Success --> FeedbackProcess["Feedback Processing"]
        Failure --> FeedbackProcess
        Surprise --> FeedbackProcess
        Resonance --> FeedbackProcess
        
        FeedbackProcess --> ValueJudge["Value Judgment"]
        FeedbackProcess --> EmotionAssoc["Emotion Association"]
        FeedbackProcess --> DreamEvolve["Dream Evolution"]
    end
```

---

## Meta-Awareness Awakening Process

Meta-awareness awakening is the system's periodic self-examination process, updating self-awareness and dream systems through reflection and insight extraction.

```mermaid
flowchart TB
    subgraph MetaAwareness["Meta-Awareness Awakening Process"]
        direction TB
        
        Trigger["Trigger Conditions<br/>• Scheduled Trigger<br/>• Event Accumulation Threshold<br/>• External Request"] --> Collect["Collect Content for Examination"]
        
        Collect --> ContentTypes["Content Types"]
        ContentTypes --> RecentEvents["Recent Event Experiences"]
        ContentTypes --> NewModels["Newly Formed Mental Models"]
        ContentTypes --> GrillChanges["Cognitive Grill Changes"]
        ContentTypes --> NewTruths["Newly Extracted Underlying Truths"]
        
        RecentEvents --> Reflection["Deep Reflection"]
        NewModels --> Reflection
        GrillChanges --> Reflection
        NewTruths --> Reflection
        
        Reflection --> InsightExtract["Insight Extraction"]
        
        InsightExtract --> UpdateSelf["Update Self Awareness<br/>(L5)"]
        InsightExtract --> UpdateDreams["Update Dream System"]
        InsightExtract --> UpdateTruths["Update Underlying Truths<br/>(L4)"]
        
        UpdateSelf --> Record["Record Awakening Log"]
        UpdateDreams --> Record
        UpdateTruths --> Record
    end
```

---

## Associative Memory Network

The associative memory network implements a "Vector Positioning + Grid Navigation" two-stage retrieval mechanism.

```mermaid
flowchart LR
    subgraph AssocMemoryNetwork["Associative Memory Network"]
        direction TB
        
        Query["Query Input"] --> VectorEmbed["Vector Embedding"]
        
        VectorEmbed --> VectorSearch["Vector Positioning<br/>(Similarity Search)"]
        
        VectorSearch --> CandidateMemories["Candidate Memory Set"]
        
        CandidateMemories --> GrillNav["Grid Navigation"]
        
        GrillNav --> NavStrategies["Navigation Strategies"]
        NavStrategies --> DirectAssoc["Direct Association"]
        NavStrategies --> BridgeConn["Bridge Connection"]
        NavStrategies --> EmergentPath["Emergent Path"]
        
        DirectAssoc --> CrossDomain["Cross-Domain Migration Retrieval"]
        BridgeConn --> CrossDomain
        EmergentPath --> CrossDomain
        
        CrossDomain --> RetrievedMemories["Retrieval Results<br/>(Multi-Domain Associated Memories)"]
    end
```

---

## Compression Evolution Engine

The compression evolution engine is responsible for compressing low-level experiences into high-level knowledge and continuously optimizing compression efficiency.

```mermaid
flowchart TB
    subgraph CompressionEngine["Compression Evolution Engine"]
        direction TB
        
        subgraph L1toL2["L1 → L2: Experience → Model"]
            Cluster["Clustering Analysis"] --> PatternExtract["Pattern Extraction"]
            PatternExtract --> ModelGen["Mental Model Generation"]
        end
        
        subgraph L2toL3["L2 → L3: Model → Grill"]
            RelDetect["Relationship Detection"] --> NetworkBuild["Network Construction"]
            NetworkBuild --> EmergentCalc["Emergence Score Calculation"]
        end
        
        subgraph L3toL4["L3 → L4: Grill → Truth"]
            Abstraction["Abstraction Extraction"] --> TruthExtract["Truth Extraction"]
            TruthExtract --> Validation["Cross-Domain Validation"]
        end
        
        subgraph L4toL5["L4 → L5: Truth → Self"]
            MetaReflect["Meta-Cognitive Reflection"] --> IdentityUpdate["Identity Update"]
            IdentityUpdate --> DreamSync["Dream System Synchronization"]
        end
        
        L1toL2 --> L2toL3
        L2toL3 --> L3toL4
        L3toL4 --> L4toL5
        
        L4toL5 --> EfficiencyMonitor["Compression Efficiency Monitoring"]
        EfficiencyMonitor --> Optimize["Optimization Strategy Adjustment"]
        Optimize --> L1toL2
    end
```

---

## System State Management

System state management is responsible for maintaining various state information during system runtime.

```mermaid
flowchart TB
    subgraph StateManagement["System State Management"]
        direction TB
        
        subgraph RuntimeState["Runtime State"]
            CurrentTask["Current Task"]
            ActiveAgents["Active Agents"]
            PendingActions["Pending Actions"]
        end
        
        subgraph MemoryState["Memory State"]
            CacheStatus["Cache Status"]
            IndexStatus["Index Status"]
            SyncStatus["Synchronization Status"]
        end
        
        subgraph DreamState["Dream State"]
            ActiveDreams["Active Dreams"]
            DreamProgress["Dream Progress"]
            PriorityQueue["Priority Queue"]
        end
        
        subgraph SelfState["Self State"]
            IdentitySnapshot["Identity Snapshot"]
            EmotionalState["Emotional State"]
            AwarenessLevel["Awareness Level"]
        end
        
        RuntimeState --> StateMonitor["State Monitoring"]
        MemoryState --> StateMonitor
        DreamState --> StateMonitor
        SelfState --> StateMonitor
        
        StateMonitor --> StateLog["State Log"]
        StateMonitor --> Alert["Anomaly Alert"]
    end
```

---

## API Interface

### Core API Overview

```mermaid
flowchart LR
    subgraph API["API Interface Layer"]
        direction TB
        
        subgraph MemoryAPI["Memory Management API"]
            CreateExp["POST /experiences<br/>Create Event Experience"]
            GetModels["GET /mental-models<br/>Get Mental Models"]
            SearchMemory["POST /search<br/>Associative Memory Retrieval"]
        end
        
        subgraph DreamAPI["Dream Management API"]
            GetDreams["GET /dreams<br/>Get Dream List"]
            CreateDream["POST /dreams<br/>Create New Dream"]
            UpdateDream["PUT /dreams/{id}<br/>Update Dream"]
        end
        
        subgraph SelfAPI["Self Awareness API"]
            GetSelf["GET /self-awareness<br/>Get Self Awareness"]
            TriggerMeta["POST /meta-awareness<br/>Trigger Meta-Awareness"]
        end
        
        subgraph SystemAPI["System Management API"]
            Health["GET /health<br/>Health Check"]
            Status["GET /status<br/>System Status"]
            Config["GET /config<br/>Configuration Info"]
        end
    end
```

---

## Database Design

### Core Table Structure

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

## Tech Stack

```mermaid
flowchart TB
    subgraph TechStack["Tech Stack"]
        direction TB
        
        subgraph Backend["Backend"]
            Python["Python 3.11+"]
            FastAPI["FastAPI"]
            SQLAlchemy["SQLAlchemy"]
            Celery["Celery"]
        end
        
        subgraph Database["Database"]
            Postgres["PostgreSQL 14+"]
            PGVector["pgvector<br/>Vector Extension"]
            Redis["Redis<br/>Cache/Queue"]
        end
        
        subgraph AI["AI/ML"]
            OpenAI["OpenAI API"]
            Embeddings["Text Embedding Models"]
            VectorSearch["Vector Similarity Search"]
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

## Quick Start

### Requirements

- Python 3.11+
- PostgreSQL 14+ (with pgvector extension enabled)
- Redis 6+
- OpenAI API Key

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/vingobot-cognitive-architecture.git
cd vingobot-cognitive-architecture

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate  # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Configure environment variables
cp .env.example .env
# Edit .env file with your configuration

# 5. Initialize database
python scripts/init_db.py

# 6. Start the service
python main.py
```

### Docker Deployment

```bash
# One-click deployment with Docker Compose
docker-compose up -d
```

---

## Project Structure

```
vingobot-cognitive-architecture/
├── app/
│   ├── api/              # API routes
│   ├── core/             # Core configuration
│   ├── models/           # Database models
│   ├── services/         # Business logic
│   └── utils/            # Utility functions
├── scripts/              # Utility scripts
├── tests/                # Test files
├── docs/                 # Documentation
├── docker/               # Docker configuration
├── .env.example          # Environment variable template
├── docker-compose.yml    # Docker Compose configuration
├── requirements.txt      # Python dependencies
├── main.py               # Application entry point
└── database_relationship_network.html  # Interactive relationship network visualization
```

---

## Interactive Visualization

This project includes an interactive HTML visualization of the Five-Layer Life Memory System relationship network.

### Five-Layer Life Memory System - Relationship Network

Open [`database_relationship_network.html`](database_relationship_network.html) in your browser to explore the interactive visualization featuring:

- **Visual Representation**: Color-coded nodes representing different layers of the cognitive architecture
  - 🟢 **Event Experience Layer (Experiences)** - Green nodes
  - 🔵 **Mental Model Layer (Mental Models)** - Blue nodes
  - 🟠 **Cognitive Grill Layer (Cognitive Grills)** - Orange nodes
  - 🟣 **Underlying Truth Layer (Underlying Truths)** - Purple nodes
  - ⚫ **Self Awareness Layer (Self Awareness)** - Gray nodes

- **Interactive Features**:
  - Drag nodes to rearrange the network
  - Zoom and pan to explore different areas
  - Click nodes to see detailed information
  - Use control buttons to fit to screen, center, or randomize layout

- **Network Structure**:
  - **Nodes**: Each circle represents an entity in the database (experience, model, grill, truth, or self-awareness)
  - **Edges**: Lines represent relationships and connections between entities
  - **Layer Flow**: Visualizes the compression evolution from L1 → L2 → L3 → L4 → L5

![Relationship Network Preview](docs/images/network-preview.png)

---

---

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## Acknowledgments

The design and philosophy of this system are deeply inspired by the following thinkers, works, and open-source projects. We express our heartfelt gratitude:

### Thinkers and Works

**Charlie Munger** and his book *Poor Charlie's Almanack* — Mr. Munger's "Multiple Mental Models" and "Latticework of Mental Models" are the cornerstone of this project's "Cognitive Grills" concept, encouraging us to transcend disciplinary boundaries and build cognitive networks that connect different knowledge domains.

**Ray Dalio** and his book *Principles* — Dalio's systematic principle-based thinking and believability-weighted decision-making methods provide valuable references for our "Underlying Truths" extraction and value judgment mechanisms in "Dream Management."

**Wang Yangming (王阳明)** and his philosophy of "Unity of Knowledge and Action (知行合一)" from *Instructions for Practical Living (《传习录》)* — The core concepts of "Knowledge is the beginning of action, and action is the completion of knowledge" and "Where knowledge is genuine and solid, that is action; where action is clear and perceptive, that is knowledge" profoundly influenced the design of this system's "Unity of Knowledge and Action Verification" mechanism. We believe that true cognition must be validated through action, and every action should deepen cognition. This aligns perfectly with the system's compression evolution process of "Event Experiences → Mental Models → Underlying Truths." Particularly, the idea that "the moment a thought arises is action" provides important inspiration for our design of the closed-loop mechanism between "Meta-Awareness" and "Dream-Driven" evolution.

**The Secret of the Golden Flower (《太乙金华宗旨》)** (attributed to Lü Dongbin 吕洞宾) — This Taoist classic's teachings on inner observation, returning light, and golden flower cultivation inspired us to incorporate Eastern philosophical introspection wisdom into "Meta-Awareness" and the "Self Awareness Layer," pursuing the introspection and evolution of consciousness.

**Daniel Kahneman** and his book *Thinking, Fast and Slow* — Professor Kahneman's cognitive model of System 1 and System 2 directly influenced the design of this system's "Awake/Asleep" state switching, simulating the alternation between human rapid intuition and deep reflection.

### Open Source Projects

**DeepSeek's Engram Project** (deepseek-ai/Engram) — The Engram project's exploration in long-term memory and knowledge management provides important technical inspiration for our "Life Memory System" and "Associative Memory Network."

**The University of Hong Kong's Nanobot Project** — This project's innovative work in cognitive architecture or robotics inspired our thinking about system autonomy and emotional mechanisms.

These contributors have illuminated our design path in different ways. We hereby express our sincere thanks.

---

<div align="center">

**⭐ Star this repository if you find it helpful! ⭐**

</div>
