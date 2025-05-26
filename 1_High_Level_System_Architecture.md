# GenAI Query Analyzer - Project Architecture

## 1. High-Level System Architecture

```mermaid
graph TB
    subgraph "Frontend Layer"
        UI["Web Interface (Bootstrap + AJAX)"]
        JS["JavaScript Client"]
    end
    
    subgraph "Django Application Layer"
        Views["Django Views"]
        URLs["URL Routing"]
        Forms["Django Forms"]
        Auth["Authentication System"]
    end
    
    subgraph "Business Logic Layer"
        LLM["LLM Connectors"]
        DB["Database Connectors"]
        OPT["SQL Optimizer"]
        QH["Query History"]
    end
    
    subgraph "External Services"
        Ollama["Ollama (Llama)"]
        OpenAI["OpenAI API"]
        DeepSeek["DeepSeek API"]
        Gemini["Gemini API"]
    end
    
    subgraph "Data Sources"
        SQLite["SQLite"]
        PostgreSQL["PostgreSQL"]
        MySQL["MySQL"]
        Hive["Apache Hive"]
        Dremio["Dremio"]
        Spark["Apache Spark"]
    end
    
    UI --> JS
    JS --> Views
    Views --> URLs
    Views --> Forms
    Views --> Auth
    Views --> LLM
    Views --> DB
    Views --> OPT
    Views --> QH
    
    LLM --> Ollama
    LLM --> OpenAI
    LLM --> DeepSeek
    LLM --> Gemini
    
    DB --> SQLite
    DB --> PostgreSQL
    DB --> MySQL
    DB --> Hive
    DB --> Dremio
    DB --> Spark