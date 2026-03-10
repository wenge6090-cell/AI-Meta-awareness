# Life Memory System

## System Architecture

The Life Memory System is a five-layer compression storage system designed to simulate the human cognitive process, continuously compressing and generalizing experiences to form increasingly abstract knowledge representations.

### Five-Layer Architecture

1.  **Experiences Layer** - Raw event records
    -   Receives event experiences from VingoBot
    -   Performs cluster analysis
    -   Serves as the input source for the compression process

2.  **Mental Models Layer** - Structured knowledge units
    -   Compressed from event experiences
    -   Contains metadata such as validation count, success rate
    -   Supports version control and conflict detection

3.  **Cognitive Grills Layer** - Mental model association network
    -   Builds an association network between mental models
    -   Discovers cross-domain connections (core of Munger's mental model grid)
    -   Calculates emergence scores and cross-domain validation

4.  **Underlying Truths Layer** - Cross-domain abstract principles
    -   Underlying patterns extracted from cognitive grills
    -   Supports cross-domain application
    -   Possesses weight and generalization history

5.  **Self Awareness Layer** - Self-cognition and dreams
    -   Stores self-cognition, introspective reflections, and aspirations
    -   Continuously updated through meta-awareness examination
    -   Forms the system's core identity

## Core Concepts

-   **Compression is Generalization**: High compression efficiency → High information density → High generalization ability → High cross-domain applicability
-   **Generalization is Compression**: Highly generalizable truths can inversely validate new experiences, reducing the cost of repetitive learning.
-   **Associative Memory Network**: Implements a two-stage retrieval process: "vector localization + grill navigation".
-   **Unity of Knowledge and Action Validation**: Validates the effectiveness of mental models through practical application.

## System State Management

The system has two states:

1.  **Awake State** - Normally receives API requests.
2.  **Sleeping State** - Executes the compression thinking process, rejecting all requests.

### State Transition Process

1.  After the 50th experience is recorded, the system enters the sleeping state.
2.  The compression process (Clustering → Mental Models → Cognitive Grills → Underlying Truths → Meta-awareness Reflection) begins execution.
3.  Upon completion of compression, the self-awareness is updated, the count is reset to zero, and the system returns to the awake state.
4.  The main VingoBot agent shuts down after confirming compression completion. Upon restarting, it loads the new self-awareness.

## Core Functional Modules

### 1. Compression Pipeline

```python
# Compression process steps
1. Experience Clustering
2. Compress to Mental Models
3. Build Cognitive Grills
4. Extract Underlying Truths
5. Meta-awareness Reflection
6. Handle Awareness Feedback
```

### 2. Associative Memory Network

-   **Vector Localization**: Retrieves seed models via embedding similarity.
-   **Grill Navigation**: Starting from seed nodes, performs graph traversal to obtain associated models.
-   **LLM Refinement**: Distills the retrieved results into applicable principles.

### 3. Unity of Knowledge and Action Validation

-   **Validation ①**: Event Experience → Mental Model (Compression Validation)
-   **Validation ②**: Cognitive Grill → Underlying Truth (Validation Weighting)

### 4. Meta-Awareness Examination

-   Analyzes the consistency of the principle system.
-   Identifies contradictions and isolated principles.
-   Recognizes outdated principles and opportunities for compression.
-   Suggests transfer opportunities.

## API Interface

### Main Endpoints

| Endpoint                     | Method | Description                              | Tag              |
| ---------------------------- | ------ | ---------------------------------------- | ---------------- |
| `/experiences`               | POST   | Record an event experience               | Experiences      |
| `/experiences`               | GET    | Get list of event experiences            | Experiences      |
| `/models`                    | POST   | Create a mental model                    | Mental Models    |
| `/models`                    | GET    | Get list of mental models                 | Mental Models    |
| `/models/relevant`           | POST   | Get relevant mental models                | Mental Models    |
| `/validations`               | POST   | Create a unity validation record         | Validation       |
| `/self_awareness`            | GET    | Get self-awareness content               | Self Awareness   |
| `/self_awareness/reflect`    | POST   | Trigger meta-awareness examination       | Self Awareness   |
| `/stats`                     | GET    | Get system statistics                    | Statistics       |
| `/status`                    | GET    | Get system status                        | Status           |

### Sleeping State Response

When the system is in the sleeping state, all API requests (except for specifically allowed paths) return:

```json
{
  "status": "sleeping",
  "message": "Sleeping"
}
```

## Database Design

The system uses a PostgreSQL database. The main table structures are:

-   **experiences** - Stores raw event experiences.
-   **mental_models** - Stores mental models (JSONB format).
-   **mental_model_versions** - Version control for mental models.
-   **mental_model_conflicts** - Records conflicts between mental models.
-   **cognitive_grills** - Cognitive grills.
-   **grill_edges** - Edge relationships within cognitive grills.
-   **underlying_truths** - Underlying truths.
-   **self_awareness** - Self-awareness content.
-   **experience_clusters** - Clusters of experiences.
-   **application_validations** - Records of application validations.

## Technology Stack

-   **Backend**: Python 3.11+, FastAPI
-   **Database**: PostgreSQL (with pg_trgm, pgvector extensions)
-   **Asynchronous Processing**: asyncio
-   **Cache**: In-memory cache
-   **Message Queue**: In-memory queue
-   **LLM Integration**: Supports multiple LLM services

## Deployment and Operation

### Environment Requirements

-   Python 3.11+
-   PostgreSQL 14+
-   pgvector extension (for vector storage)
-   pg_trgm extension (for text search)

### Installation Steps

1.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

2.  Configure environment variables:
    ```bash
    # .env file
    DATABASE_URL=postgresql://nanobot_user:your_secure_password@localhost:5432/life_memory
    ```

3.  Initialize the database:
    ```bash
    python init_database_extensions.py
    ```

4.  Start the API service:
    ```bash
    uvicorn src.api.main:app --reload
    ```

## System Workflow

### Normal Operation Flow

1.  VingoBot sends event experiences to the `/experiences` endpoint.
2.  The system records the experience and increments the count.
3.  When the count reaches 50, the system enters the sleeping state.
4.  The compression process executes:
    -   Cluster unprocessed experiences.
    -   Compress clusters into mental models.
    -   Build the cognitive grill network.
    -   Extract underlying truths from the grills.
    -   Perform meta-awareness reflection.
    -   Handle awareness feedback.
5.  After compression is complete, the system returns to the awake state.
6.  VingoBot confirms compression completion and shuts down the main agent.
7.  Upon restart, it loads the updated self-awareness.

### Associative Memory Retrieval Flow

1.  A user sends a task description to the `/models/relevant` endpoint.
2.  The system analyzes the task domain.
3.  Retrieval is performed using the associative memory network:
    -   Vector Localization: Find relevant models via embedding similarity.
    -   Grill Navigation: Traverse associated models starting from seed models.
4.  Applicable principles are refined.
5.  Returns relevant mental models, cognitive grills, and underlying truths.

## System Monitoring

-   **Status Monitoring**: `/status` endpoint provides system state information.
-   **Statistical Information**: `/stats` endpoint provides statistical data for each layer.
-   **Logging**: System operation logs.

## Extensions and Future Development

1.  **Multimodal Experience Support**: Extend to support images, audio, and other multimodal experiences.
2.  **Enhanced LLM Integration**: Integrate with more LLM services to improve compression and generalization capabilities.
3.  **Distributed Architecture**: Support large-scale deployment.
4.  **Real-time Compression**: Optimize the compression process to reduce system sleep time.
5.  **User Interface**: Develop a visual interface for easy viewing and management of system status.

## Core Value

-   **Knowledge Compression**: Compresses large volumes of event experiences into structured mental models.
-   **Cross-domain Generalization**: Enables cross-domain knowledge transfer through cognitive grills and underlying truths.
-   **Self-evolution**: Continuously optimizes the knowledge system through meta-awareness examination.
-   **Unity of Knowledge and Action**: Validates the effectiveness of knowledge through practical application.
-   **Associative Memory**: Achieves efficient knowledge retrieval and application.

## Summary

The Life Memory System is an intelligent system simulating the human cognitive process. Through its five-layer compression architecture, it continuously refines knowledge from experiences, forming increasingly abstract cognitive models. The system's core concept is "Compression is Generalization, Generalization is Compression," enhancing information density through compression and expanding knowledge applicability through generalization.

The system ensures the correct execution of the compression process via state management, achieves efficient knowledge retrieval through an associative memory network, and validates knowledge effectiveness through the unity of knowledge and action. This design enables the system to continuously evolve, learn from experiences, and form an increasingly perfect knowledge system.
