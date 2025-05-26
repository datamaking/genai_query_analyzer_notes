# Prompt Used

which are the best ai agents frameworks? how it is all different from each others?

# ChatGPT Response

Here’s a roundup of some of the most popular open-source AI-agent frameworks today, along with what sets each apart:

---

## 1. LangChain

* **Language**: Python (with growing support for TypeScript/JavaScript)
* **Focus**: Building chains of calls—LLM ↔︎ tools ↔︎ memory ↔︎ prompts—with rich abstractions (Chains, Agents, Memory, Retrievers).
* **Features**:

  * Plug-and-play “Agents” that can decide at runtime which tool (search, calculator, API, etc.) to invoke.
  * Wide LLM support (OpenAI, Anthropic, Hugging Face, etc.)
  * Built-in memory stores (in-memory, Redis, ChromaDB, Weaviate…)
  * Large ecosystem of community “recipes” and integrations (document loaders, vector stores, UI kits).
* **Best for**: Rapid prototyping of agentic workflows; model-to-tool orchestration; building conversational assistants with state.

---

## 2. Microsoft Semantic Kernel

* **Language**: .NET (C#) and Python SDK
* **Focus**: Orchestrating “skills” (modular functions) driven by LLM planning & retrieval.
* **Features**:

  * **Semantic Functions**: code or prompt snippets annotated to be called as capabilities.
  * **Planner**: LLM-based planning to sequence skills into multi-step logic.
  * Built-in memory abstractions (linguistic, vector).
  * Deep integration with Azure AI services (OpenAI, Azure Cognitive Services).
* **Best for**: Enterprises heavily invested in Azure/.NET, needing robust planning & skill invocation pipelines.

---

## 3. LlamaIndex (formerly GPT-Index)

* **Language**: Python
* **Focus**: Data ingestion + indexing → retrieval-augmented generation (RAG) agents.
* **Features**:

  * Indexes over documents (trees, graphs, vectors) that an agent can “query” to ground its reasoning.
  * Built-in data connectors (CSV, PDF, SQL, JSON, web pages).
  * Plugins for streaming data, caching, embeddings.
* **Best for**: Use cases where grounding agent responses in large, heterogeneous data sources is critical.

---

## 4. AutoGen (Microsoft)

* **Language**: Python
* **Focus**: Orchestrating **multi-agent** collaboration to solve tasks.
* **Features**:

  * **Role-based agents** that exchange messages in a conversation.
  * Built-in abstractions for task decomposition, planning, and result fusion.
  * Support for synchronous and asynchronous agent workflows.
* **Best for**: Complex workflows where different “expert” agents (e.g., researcher, critic, coder) iterate to refine results.

---

## 5. Haystack Agents (Deepset)

* **Language**: Python
* **Focus**: Search-centric pipelines with agentic decision logic.
* **Features**:

  * Combines document retrieval, QA, summarization, and prompting in configurable “Pipelines.”
  * Agent classes that use retrievers and LLMs to plan which pipeline nodes to execute.
  * Enterprise-grade deployment tooling (Docker, Kubernetes).
* **Best for**: Production RAG applications—especially in legal, compliance, and customer-support domains.

---

## Comparative at a Glance

| Framework           | Core Strength             | Orchestration Style      | Language    | Ecosystem Highlights         |
| ------------------- | ------------------------- | ------------------------ | ----------- | ---------------------------- |
| **LangChain**       | Tool-centric agents       | Chain & Agent classes    | Python / JS | Huge library of integrations |
| **Semantic Kernel** | Skill-based planning      | LLM-driven planner       | C# / Python | Tight Azure integration      |
| **LlamaIndex**      | Data-grounded RAG         | Index → Retriever → LLM  | Python      | Document connectors          |
| **AutoGen**         | Multi-agent collaboration | Role-based conversations | Python      | Task-decomposition patterns  |
| **Haystack Agents** | Search + QA pipelines     | Pipeline nodes + Agent   | Python      | Enterprise RAG deployments   |

---

### How They Differ, in a Nutshell

* **Abstraction layer**:

  * LangChain focuses on **chains** and **tools**.
  * Semantic Kernel frames everything as **skills** planned by an LLM.
  * LlamaIndex lives at the **data + retrieval** layer.
  * AutoGen orchestrates **multiple agents** playing different roles.
  * Haystack wraps a **search/Q\&A pipeline** in an agent decision loop.

* **Deployment & ecosystem**:

  * LangChain and LlamaIndex thrive on community-built integrations; best for flexible, custom setups.
  * Semantic Kernel and Haystack lean more enterprise, with first-party hosting and scaling tooling.
  * AutoGen is more experimental—ideal for research or complex, multi-role agent systems.

* **Primary use case**:

  * If you need a **simple agent** deciding between tools, go with **LangChain**.
  * If you want to **ground** your agent in large corpora of documents, choose **LlamaIndex** (or Haystack).
  * If you’re in the Microsoft/Azure ecosystem and want model-driven pipelines, grab **Semantic Kernel**.
  * If you want **multiple agents** interacting (e.g., debate, critique), experiment with **AutoGen**.

Each framework pushes the idea of “agents” in slightly different directions—tool orchestration, skill invocation, data-grounded reasoning, or multi-agent collaboration—so pick the one whose abstractions map cleanly to your domain.


===============================================================================================

# DeepSeek Response

### Overview of AI Agent Frameworks and Their Differences

AI agent frameworks are specialized tools designed to build, train, and deploy agents for specific tasks. They vary based on application areas, design philosophies, and technical features. Below is a categorized breakdown of popular frameworks and their distinctions.

---

#### **1. Reinforcement Learning (RL) Frameworks**
Focus on training agents to interact with environments through trial and error.

- **OpenAI Gym**  
  - **Description**: Provides standardized environments (e.g., Atari games, robotics simulations) for RL algorithm development.  
  - **Differentiator**: Environment-focused; often paired with RL libraries (e.g., Stable Baselines).  
  - **Use Case**: Benchmarking and prototyping RL algorithms.

- **RLlib (Ray)**  
  - **Description**: Scalable RL library supporting multi-agent and distributed training.  
  - **Differentiator**: Integration with Ray for cloud/distributed computing.  
  - **Use Case**: Large-scale, production-grade RL applications.

- **TF-Agents**  
  - **Description**: Built on TensorFlow, offering RL algorithms and environment tools.  
  - **Differentiator**: Tight integration with TensorFlow ecosystem.  
  - **Use Case**: Developers already using TensorFlow for ML workflows.

- **Stable Baselines3**  
  - **Description**: High-quality implementations of RL algorithms (PyTorch).  
  - **Differentiator**: Simple APIs for quick experimentation.  
  - **Use Case**: Research and education.

- **Unity ML-Agents**  
  - **Description**: Train agents in 3D Unity environments.  
  - **Differentiator**: Rich simulation environments for games/robotics.  
  - **Use Case**: Game development and complex 3D simulations.

---

#### **2. Conversational AI Frameworks**
Designed for building chatbots and dialogue systems.

- **Rasa**  
  - **Description**: Open-source framework for contextual assistants.  
  - **Differentiator**: On-prem deployment, customizable NLU and dialogue management.  
  - **Use Case**: Privacy-sensitive or highly tailored chatbots.

- **Dialogflow (Google)**  
  - **Description**: Cloud-based NLU service with prebuilt agents.  
  - **Differentiator**: Easy integration with Google services (e.g., Assistant).  
  - **Use Case**: Rapid deployment of voice/text chatbots.

- **Microsoft Bot Framework**  
  - **Description**: Tools for building enterprise-grade bots.  
  - **Differentiator**: Tight Azure integration and multi-channel support.  
  - **Use Case**: Enterprise bots with CRM/ERP connectivity.

- **Amazon Lex**  
  - **Description**: Powers Alexa’s conversational engine.  
  - **Differentiator**: Serverless architecture with AWS ecosystem.  
  - **Use Case**: Voice-driven applications on AWS.

---

#### **3. Autonomous AI Agent Frameworks**
Enable agents to perform complex, multi-step tasks autonomously.

- **LangChain**  
  - **Description**: Chains LLM calls with external tools (APIs, databases).  
  - **Differentiator**: Modular design for flexible agent pipelines.  
  - **Use Case**: LLM-powered apps with tool integration.

- **AutoGPT**  
  - **Description**: Autonomous agent using GPT-4 for goal-driven tasks.  
  - **Differentiator**: Internet access, memory, and self-prompting.  
  - **Use Case**: Automated research, content generation, and coding.

- **Microsoft AutoGen**  
  - **Description**: Framework for multi-agent collaboration.  
  - **Differentiator**: Focus on agent communication and roles.  
  - **Use Case**: Collaborative problem-solving (e.g., coding teams).

- **SuperAGI**  
  - **Description**: Open-source platform for autonomous agents.  
  - **Differentiator**: GUI toolkit for monitoring and tooling.  
  - **Use Case**: Customizable autonomous workflows.

---

#### **4. Key Differences Summary**

| **Category**              | **Focus**                  | **Strengths**                          | **Ecosystem**                  | **Scalability**          |
|---------------------------|----------------------------|----------------------------------------|---------------------------------|--------------------------|
| **RL Frameworks**          | Environment interaction    | Algorithm flexibility, simulation      | TensorFlow/PyTorch, Ray         | High (e.g., RLlib)       |
| **Conversational AI**      | NLP/dialog management      | Prebuilt models, platform integration  | Cloud services (AWS, Google)    | Moderate to High         |
| **Autonomous Agents**      | Task automation            | LLM integration, multi-step reasoning  | Open-source/APIs               | Variable (depends on LLM)|

---

#### **Conclusion**
Choosing the best framework depends on the use case:
- **Reinforcement Learning**: Prioritize scalability (RLlib) or ecosystem (TF-Agents).  
- **Conversational AI**: Opt for cloud ease (Dialogflow) or customization (Rasa).  
- **Autonomous Agents**: Select based on LLM integration (LangChain) or autonomy (AutoGPT).  

Each framework excels in specific domains, balancing ease of use, customization, and scalability.



===============================================================================================

# Claude Response

There are several prominent AI agent frameworks, each with distinct approaches and strengths:

## Leading Frameworks

**LangChain** is one of the most popular, offering extensive integrations with various LLMs and tools. It provides a comprehensive ecosystem for building chains of reasoning, memory management, and tool usage. However, it can be complex and sometimes over-engineered for simple use cases.

**LlamaIndex** focuses primarily on retrieval-augmented generation (RAG) and knowledge management. It excels at indexing and querying large document collections, making it ideal for knowledge-intensive applications.

**AutoGen** (Microsoft) emphasizes multi-agent conversations where different AI agents can collaborate, debate, and solve problems together. It's particularly strong for scenarios requiring multiple perspectives or specialized roles.

**CrewAI** provides a framework for orchestrating teams of AI agents with defined roles, goals, and collaborative workflows. It's designed around the concept of crews working together on complex tasks.

**Haystack** (deepset) is built specifically for search and question-answering applications, with strong NLP pipelines and production-ready components.

**Semantic Kernel** (Microsoft) integrates AI capabilities directly into applications with a focus on planning and function calling, designed to work seamlessly with existing codebases.

## Key Differences

**Architecture**: Some frameworks like AutoGen focus on multi-agent systems, while others like LangChain provide general-purpose building blocks. LlamaIndex specializes in data indexing and retrieval.

**Complexity vs Simplicity**: LangChain offers extensive features but can be overwhelming. Semantic Kernel aims for developer-friendly integration. CrewAI abstracts complexity behind intuitive concepts.

**Use Case Focus**: Haystack targets search applications, LlamaIndex excels at RAG, AutoGen handles collaborative AI scenarios, while LangChain tries to cover everything.

**Integration Ecosystem**: LangChain has the broadest ecosystem of integrations. Others tend to focus on specific domains or have more opinionated approaches.

**Production Readiness**: Some frameworks prioritize research and experimentation, while others like Haystack and Semantic Kernel emphasize production deployment and enterprise features.

The choice depends on your specific needs: document processing (LlamaIndex), multi-agent collaboration (AutoGen/CrewAI), general-purpose development (LangChain), or production search applications (Haystack).



===============================================================================================



AI agent design patterns are recurring architectural solutions for building intelligent systems. Let me break down the key patterns with real-world analogies and AutoGen implementations.

I've created a comprehensive guide to AI agent design patterns with detailed implementations using AutoGen. Here's a breakdown of the six core patterns:

## 1. Single Agent Pattern
**Real-world analogy**: A solo consultant who handles everything independently
- **Use case**: Simple tasks that don't require specialization
- **Implementation**: One agent with broad capabilities
- **Pros**: Simple, fast, low overhead
- **Cons**: Limited expertise depth, no collaboration benefits

## 2. Sequential Chain Pattern
**Real-world analogy**: Assembly line where each worker adds expertise in sequence
- **Use case**: Multi-step processes where each stage builds on the previous
- **Implementation**: Research → Analysis → Strategy pipeline
- **Pros**: Clear workflow, specialized expertise at each stage
- **Cons**: Bottlenecks if one agent fails, no parallel processing

## 3. Collaborative Group Pattern
**Real-world analogy**: Round table discussion with domain experts
- **Use case**: Complex decisions requiring multiple perspectives
- **Implementation**: Tech, Business, and UX experts collaborate with a facilitator
- **Pros**: Rich discussions, diverse viewpoints, creative solutions
- **Cons**: Can be slow, potential for endless debates

## 4. Hierarchical Delegation Pattern
**Real-world analogy**: Corporate structure with manager delegating to teams
- **Use case**: Complex projects that can be broken into specialized tasks
- **Implementation**: Manager agent delegates to Content, Data, and Design specialists
- **Pros**: Efficient task distribution, clear accountability
- **Cons**: Single point of failure at manager level, coordination overhead

## 5. Reactive/Event-Driven Pattern
**Real-world analogy**: Emergency response system reacting to different alerts
- **Use case**: Real-time systems that need to respond to various events
- **Implementation**: Monitor categorizes events and routes to Security, Performance, or Support agents
- **Pros**: Responsive, efficient resource allocation, scalable
- **Cons**: Requires good event classification, complex routing logic

## 6. Feedback Loop Pattern
**Real-world analogy**: Quality control process with iterative improvement
- **Use case**: Tasks requiring high quality through iterative refinement
- **Implementation**: Creator → Reviewer → Quality Checker cycle
- **Pros**: High quality output, continuous improvement
- **Cons**: Can be time-consuming, might over-optimize

## Choosing the Right Pattern

**Single Agent**: Simple queries, quick responses, limited scope
**Sequential**: Data processing pipelines, research workflows
**Collaborative**: Strategic planning, creative brainstorming, complex decisions
**Hierarchical**: Large projects, clear task boundaries, need for coordination
**Reactive**: Monitoring systems, customer support, real-time responses
**Feedback Loop**: Content creation, code review, quality-critical tasks

The code provides complete working examples for each pattern. You'll need to set up your OpenAI API key to run them. Each pattern can be mixed and matched depending on your specific use case - for example, you might use hierarchical delegation where each specialist uses their own feedback loop for quality improvement.



import autogen
from autogen import ConversableAgent, GroupChat, GroupChatManager
import os

# Configuration for LLM
config_list = [
    {
        "model": "gpt-4",
        "api_key": os.getenv("OPENAI_API_KEY")
    }
]

llm_config = {"config_list": config_list}

# =============================================================================
# PATTERN 1: SINGLE AGENT PATTERN
# Analogy: A solo consultant who handles everything independently
# =============================================================================

class SingleAgentConsultant:
    def __init__(self):
        self.agent = ConversableAgent(
            name="business_consultant",
            system_message="""You are a business consultant who can analyze 
            problems, generate solutions, and provide recommendations. You work 
            independently and handle all aspects of business analysis.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
    
    def analyze_business_problem(self, problem):
        """Single agent handles the entire workflow"""
        response = self.agent.generate_reply(
            messages=[{"content": f"Analyze this business problem and provide solutions: {problem}"}]
        )
        return response

# =============================================================================
# PATTERN 2: SEQUENTIAL CHAIN PATTERN
# Analogy: Assembly line where each worker adds their expertise in sequence
# =============================================================================

class SequentialChainPattern:
    def __init__(self):
        # Research Agent - gathers information
        self.researcher = ConversableAgent(
            name="researcher",
            system_message="""You are a research specialist. Your job is to gather 
            and analyze information about the given topic. Provide comprehensive 
            research findings and pass them to the next agent.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Analyst Agent - processes research
        self.analyst = ConversableAgent(
            name="analyst",
            system_message="""You are a data analyst. Take the research provided 
            and perform detailed analysis. Identify patterns, trends, and insights. 
            Pass your analysis to the strategist.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Strategy Agent - creates recommendations
        self.strategist = ConversableAgent(
            name="strategist",
            system_message="""You are a strategic planner. Based on the research 
            and analysis provided, create actionable strategies and recommendations.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
    
    def process_sequential(self, topic):
        """Process through sequential chain"""
        # Step 1: Research
        research_result = self.researcher.generate_reply(
            messages=[{"content": f"Research this topic thoroughly: {topic}"}]
        )
        
        # Step 2: Analysis
        analysis_result = self.analyst.generate_reply(
            messages=[{"content": f"Analyze this research: {research_result}"}]
        )
        
        # Step 3: Strategy
        strategy_result = self.strategist.generate_reply(
            messages=[{"content": f"Create strategies based on this analysis: {analysis_result}"}]
        )
        
        return {
            "research": research_result,
            "analysis": analysis_result,
            "strategy": strategy_result
        }

# =============================================================================
# PATTERN 3: COLLABORATIVE GROUP PATTERN
# Analogy: Round table discussion where experts collaborate and debate
# =============================================================================

class CollaborativeGroupPattern:
    def __init__(self):
        # Technical Expert
        self.tech_expert = ConversableAgent(
            name="tech_expert",
            system_message="""You are a technical expert specializing in software 
            architecture and implementation. You focus on technical feasibility, 
            scalability, and best practices.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Business Expert
        self.business_expert = ConversableAgent(
            name="business_expert",
            system_message="""You are a business expert focusing on market analysis, 
            ROI, and business viability. You evaluate ideas from a commercial perspective.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # UX Expert
        self.ux_expert = ConversableAgent(
            name="ux_expert",
            system_message="""You are a UX expert focusing on user experience, 
            usability, and design. You ensure solutions are user-friendly and accessible.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Facilitator
        self.facilitator = ConversableAgent(
            name="facilitator",
            system_message="""You are a meeting facilitator. Guide the discussion, 
            summarize different viewpoints, and help reach consensus among experts.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
    
    def collaborative_discussion(self, project_idea, max_rounds=5):
        """Run collaborative group discussion"""
        group_chat = GroupChat(
            agents=[self.tech_expert, self.business_expert, self.ux_expert, self.facilitator],
            messages=[],
            max_round=max_rounds,
            speaker_selection_method="round_robin"
        )
        
        manager = GroupChatManager(groupchat=group_chat, llm_config=llm_config)
        
        # Start the discussion
        chat_result = self.facilitator.initiate_chat(
            manager,
            message=f"""Let's evaluate this project idea from multiple perspectives: {project_idea}
            
            Tech Expert: Focus on technical implementation and challenges
            Business Expert: Analyze market potential and business viability  
            UX Expert: Consider user experience and design aspects
            Facilitator: Guide discussion and summarize consensus"""
        )
        
        return chat_result

# =============================================================================
# PATTERN 4: HIERARCHICAL DELEGATION PATTERN
# Analogy: Corporate structure with manager delegating to specialized teams
# =============================================================================

class HierarchicalDelegationPattern:
    def __init__(self):
        # Manager Agent - coordinates and delegates
        self.manager = ConversableAgent(
            name="project_manager",
            system_message="""You are a project manager who delegates tasks to 
            specialized team members. Analyze requests, break them down into 
            subtasks, and assign them to the appropriate specialists.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Content Specialist
        self.content_specialist = ConversableAgent(
            name="content_specialist",
            system_message="""You are a content creation specialist. You handle 
            all content-related tasks including writing, editing, and content strategy.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Data Specialist
        self.data_specialist = ConversableAgent(
            name="data_specialist",
            system_message="""You are a data specialist. You handle data analysis, 
            visualization, and statistical interpretation tasks.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Design Specialist
        self.design_specialist = ConversableAgent(
            name="design_specialist",
            system_message="""You are a design specialist. You handle UI/UX design, 
            visual design, and user interface recommendations.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
    
    def delegate_project(self, project_description):
        """Manager delegates tasks to specialists"""
        # Manager analyzes and plans
        delegation_plan = self.manager.generate_reply(
            messages=[{
                "content": f"""Analyze this project and create a delegation plan: {project_description}
                
                Available specialists:
                - Content Specialist: writing, editing, content strategy
                - Data Specialist: data analysis, statistics, visualization
                - Design Specialist: UI/UX, visual design, interface design
                
                Break down the project into specific tasks for each specialist."""
            }]
        )
        
        # Execute delegated tasks (simplified example)
        results = {"delegation_plan": delegation_plan}
        
        # Content tasks
        content_result = self.content_specialist.generate_reply(
            messages=[{"content": f"Handle content tasks from this plan: {delegation_plan}"}]
        )
        results["content"] = content_result
        
        # Data tasks
        data_result = self.data_specialist.generate_reply(
            messages=[{"content": f"Handle data tasks from this plan: {delegation_plan}"}]
        )
        results["data"] = data_result
        
        # Design tasks
        design_result = self.design_specialist.generate_reply(
            messages=[{"content": f"Handle design tasks from this plan: {delegation_plan}"}]
        )
        results["design"] = design_result
        
        return results

# =============================================================================
# PATTERN 5: REACTIVE/EVENT-DRIVEN PATTERN
# Analogy: Emergency response system that reacts to different types of alerts
# =============================================================================

class ReactiveEventPattern:
    def __init__(self):
        # Monitor Agent - watches for events
        self.monitor = ConversableAgent(
            name="system_monitor",
            system_message="""You are a system monitor that categorizes and 
            prioritizes incoming events/alerts. Determine the type and urgency 
            of each event.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Security Specialist - handles security events
        self.security_agent = ConversableAgent(
            name="security_specialist",
            system_message="""You are a cybersecurity specialist. You handle 
            security-related events, threats, and incidents.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Performance Specialist - handles performance events
        self.performance_agent = ConversableAgent(
            name="performance_specialist",
            system_message="""You are a performance specialist. You handle 
            system performance issues, optimization, and capacity planning.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # General Support - handles other events
        self.support_agent = ConversableAgent(
            name="support_specialist",
            system_message="""You are a general support specialist. You handle 
            general system issues, user problems, and maintenance tasks.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
    
    def handle_event(self, event_description):
        """React to incoming events"""
        # Monitor categorizes the event
        event_analysis = self.monitor.generate_reply(
            messages=[{
                "content": f"""Analyze this system event and categorize it: {event_description}
                
                Categories:
                - SECURITY: security threats, breaches, suspicious activity
                - PERFORMANCE: slow response, high CPU, memory issues
                - GENERAL: user issues, general maintenance, other problems
                
                Provide category and urgency level (LOW/MEDIUM/HIGH)."""
            }]
        )
        
        # Route to appropriate specialist based on category
        if "SECURITY" in event_analysis.upper():
            response = self.security_agent.generate_reply(
                messages=[{"content": f"Handle this security event: {event_description}\nAnalysis: {event_analysis}"}]
            )
            specialist = "Security"
        elif "PERFORMANCE" in event_analysis.upper():
            response = self.performance_agent.generate_reply(
                messages=[{"content": f"Handle this performance event: {event_description}\nAnalysis: {event_analysis}"}]
            )
            specialist = "Performance"
        else:
            response = self.support_agent.generate_reply(
                messages=[{"content": f"Handle this general event: {event_description}\nAnalysis: {event_analysis}"}]
            )
            specialist = "Support"
        
        return {
            "event_analysis": event_analysis,
            "handling_specialist": specialist,
            "response": response
        }

# =============================================================================
# PATTERN 6: FEEDBACK LOOP PATTERN
# Analogy: Quality control process with iterative improvement
# =============================================================================

class FeedbackLoopPattern:
    def __init__(self):
        # Creator Agent
        self.creator = ConversableAgent(
            name="content_creator",
            system_message="""You are a content creator. You create initial 
            versions of content based on requirements. You also revise content 
            based on feedback received.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Reviewer Agent
        self.reviewer = ConversableAgent(
            name="content_reviewer",
            system_message="""You are a content reviewer. You evaluate content 
            quality, accuracy, and adherence to requirements. Provide constructive 
            feedback for improvements.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
        
        # Quality Checker
        self.quality_checker = ConversableAgent(
            name="quality_checker",
            system_message="""You are a quality assurance specialist. You make 
            the final decision on whether content meets standards or needs more revision.""",
            llm_config=llm_config,
            human_input_mode="NEVER"
        )
    
    def iterative_improvement(self, requirements, max_iterations=3):
        """Iteratively improve content through feedback loops"""
        current_content = None
        iteration_history = []
        
        for iteration in range(max_iterations):
            print(f"--- Iteration {iteration + 1} ---")
            
            # Create or revise content
            if current_content is None:
                # Initial creation
                create_prompt = f"Create content based on these requirements: {requirements}"
            else:
                # Revision based on feedback
                create_prompt = f"Revise this content based on feedback:\n\nCurrent content: {current_content}\n\nFeedback: {feedback}"
            
            current_content = self.creator.generate_reply(
                messages=[{"content": create_prompt}]
            )
            
            # Review the content
            feedback = self.reviewer.generate_reply(
                messages=[{"content": f"Review this content against requirements:\n\nRequirements: {requirements}\n\nContent: {current_content}"}]
            )
            
            # Quality check
            quality_decision = self.quality_checker.generate_reply(
                messages=[{"content": f"Evaluate if this content meets quality standards:\n\nContent: {current_content}\n\nReview feedback: {feedback}\n\nRespond with APPROVED or NEEDS_REVISION and explain why."}]
            )
            
            iteration_info = {
                "iteration": iteration + 1,
                "content": current_content,
                "feedback": feedback,
                "quality_decision": quality_decision
            }
            iteration_history.append(iteration_info)
            
            # Check if approved
            if "APPROVED" in quality_decision.upper():
                print(f"Content approved after {iteration + 1} iterations!")
                break
        
        return {
            "final_content": current_content,
            "iterations": iteration_history,
            "total_iterations": len(iteration_history)
        }

# =============================================================================
# EXAMPLE USAGE AND DEMONSTRATIONS
# =============================================================================

def demonstrate_patterns():
    """Demonstrate each pattern with examples"""
    
    print("=== AI AGENT DESIGN PATTERNS DEMONSTRATION ===\n")
    
    # Pattern 1: Single Agent
    print("1. SINGLE AGENT PATTERN")
    print("Analogy: Solo consultant handling everything independently")
    single_agent = SingleAgentConsultant()
    # result1 = single_agent.analyze_business_problem("Our startup needs a go-to-market strategy")
    print("✓ Single agent handles complete business analysis\n")
    
    # Pattern 2: Sequential Chain
    print("2. SEQUENTIAL CHAIN PATTERN")
    print("Analogy: Assembly line with specialized workers")
    sequential = SequentialChainPattern()
    # result2 = sequential.process_sequential("Electric vehicle market opportunities")
    print("✓ Research → Analysis → Strategy in sequence\n")
    
    # Pattern 3: Collaborative Group
    print("3. COLLABORATIVE GROUP PATTERN")
    print("Analogy: Round table expert discussion")
    collaborative = CollaborativeGroupPattern()
    # result3 = collaborative.collaborative_discussion("AI-powered fitness app")
    print("✓ Multiple experts collaborate and debate\n")
    
    # Pattern 4: Hierarchical Delegation
    print("4. HIERARCHICAL DELEGATION PATTERN")
    print("Analogy: Corporate structure with manager delegating tasks")
    hierarchical = HierarchicalDelegationPattern()
    # result4 = hierarchical.delegate_project("Launch a new e-commerce website")
    print("✓ Manager delegates to specialized team members\n")
    
    # Pattern 5: Reactive/Event-Driven
    print("5. REACTIVE/EVENT-DRIVEN PATTERN")
    print("Analogy: Emergency response system reacting to alerts")
    reactive = ReactiveEventPattern()
    # result5 = reactive.handle_event("Multiple failed login attempts detected")
    print("✓ Monitor routes events to appropriate specialists\n")
    
    # Pattern 6: Feedback Loop
    print("6. FEEDBACK LOOP PATTERN")
    print("Analogy: Quality control with iterative improvement")
    feedback_loop = FeedbackLoopPattern()
    # result6 = feedback_loop.iterative_improvement("Write a product launch email")
    print("✓ Create → Review → Revise until quality standards met\n")

# To run the demonstrations:
if __name__ == "__main__":
    # Note: You'll need to set your OpenAI API key in environment variables
    # os.environ["OPENAI_API_KEY"] = "your-api-key-here"
    
    demonstrate_patterns()
    
    # Example of running a specific pattern:
    # single_agent = SingleAgentConsultant()
    # result = single_agent.analyze_business_problem("How to improve customer retention?")
    # print(result)



===============================================================================================


===============================================================================================


Below are four common AI-agent design patterns, each explained with a real-world analogy and illustrated with minimal Python snippets using the AutoGen (“autogen”) framework. You can mix and match these patterns when building more complex agents.

---

## 1. Reactive (Stimulus–Response)

### Analogy

A smoke alarm: the moment it senses “smoke” (stimulus), it immediately “responds” by sounding the alarm. There’s no long-term planning or internal state—just input→output.

### Pattern

* **No memory**, **no planning**
* Single-step: map input directly to output

### Code (using Ollama via AutoGen)

```python
import asyncio
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

async def reactive_agent(user_input: str):
    client = OllamaChatCompletionClient(model="llama3")
    # System prompt defines pure “Q→A” behavior
    messages = [
        SystemMessage(content="You are a helpful Q&A assistant. Answer concisely."),
        UserMessage(content=user_input, source="user")
    ]
    resp = await client.create(messages)  # type: ignore
    return resp.choices[0].message.content

if __name__ == "__main__":
    answer = asyncio.run(reactive_agent("What’s the capital of France?"))
    print(answer)
```

---

## 2. Deliberative (Planner–Executor)

### Analogy

A travel agent: first **plans** an itinerary (step 1: choose dates, step 2: book flights, step 3: reserve hotels), then **executes** each step in order.

### Pattern

1. **Plan**: generate a sequence of sub-tasks
2. **Execute**: carry them out one by one, possibly invoking tools

### Code Sketch

```python
import asyncio
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

async def deliberative_agent(goal: str):
    client = OllamaChatCompletionClient(model="llama3")
    # 1) PLAN phase: ask the LLM to break the goal into steps
    plan_prompt = (
        f"You are a planner. Break the task into ordered steps with brief descriptions.\n"
        f"Task: {goal}"
    )
    plan_resp = await client.create([
        SystemMessage(content="You are an expert task planner."),
        UserMessage(content=plan_prompt, source="user")
    ])  # type: ignore
    plan = plan_resp.choices[0].message.content

    # 2) EXECUTE phase: run through each step
    results = []
    for idx, step in enumerate(plan.split("\n"), 1):
        step_resp = await client.create([
            SystemMessage(content=f"Execute step {idx}: {step}"),
            UserMessage(content="Proceed.", source="user")
        ])  # type: ignore
        results.append(f"Step {idx} result: {step_resp.choices[0].message.content}")

    return plan, results

if __name__ == "__main__":
    plan, outputs = asyncio.run(deliberative_agent("Summarize quarterly earnings and draft a short email to stakeholders."))
    print("PLAN:\n", plan)
    print("\nOUTPUTS:\n", "\n".join(outputs))
```

---

## 3. BDI (Belief–Desire–Intention)

### Analogy

A personal assistant who:

1. **Believes** facts (“my calendar says I’m free on Friday”),
2. Has **Desires** (schedule a meeting),
3. Forms **Intentions** (send invites), and then acts.

### Pattern

* **Beliefs**: internal knowledge base
* **Desires**: goals the agent wants to achieve
* **Intentions**: committed plans

### Code Sketch

```python
import asyncio
from typing import List
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

class BDIAgent:
    def __init__(self, model="llama3"):
        self.client = OllamaChatCompletionClient(model=model)
        self.beliefs: List[str] = []
        self.desires: List[str] = []
        self.intentions: List[str] = []

    async def perceive(self, fact: str):
        # add new belief
        self.beliefs.append(fact)

    async def deliberate(self):
        # pick a desire based on beliefs
        prompt = (
            "Beliefs:\n" + "\n".join(self.beliefs) +
            "\nBased on these, what should I want to achieve next? (Give one concise desire.)"
        )
        resp = await self.client.create([
            SystemMessage(content="You are a rational agent selecting a desire."),
            UserMessage(content=prompt, source="user")
        ])  # type: ignore
        desire = resp.choices[0].message.content.strip()
        self.desires.append(desire)

    async def intend(self):
        # commit a plan for the first desire
        prompt = (
            "Create a step-by-step plan to achieve this desire:\n" +
            self.desires[0]
        )
        resp = await self.client.create([
            SystemMessage(content="You are a strategic planner."),
            UserMessage(content=prompt, source="user")
        ])  # type: ignore
        plan = resp.choices[0].message.content
        self.intentions = plan.split("\n")

    async def execute(self):
        # carry out the first intended step
        step = self.intentions.pop(0)
        resp = await self.client.create([
            SystemMessage(content=f"Execute: {step}"),
            UserMessage(content="Proceed.", source="user")
        ])  # type: ignore
        return resp.choices[0].message.content

async def run_bdi():
    agent = BDIAgent()
    await agent.perceive("Meeting with the product team is scheduled on Friday at 3pm.")
    await agent.deliberate()
    await agent.intend()
    result = await agent.execute()
    print("Execution result:", result)

if __name__ == "__main__":
    asyncio.run(run_bdi())
```

---

## 4. Blackboard / Multi-Agent Collaboration

### Analogy

A medical team around a patient chart (“blackboard”): the radiologist posts X-ray findings, the surgeon posts surgical notes, the pharmacist posts medication info, and each reads the others’ updates to form a complete diagnosis/treatment.

### Pattern

* **Shared workspace** (blackboard)
* Multiple specialist agents read/write

### Code Sketch

```python
import asyncio
from collections import defaultdict
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

class Blackboard:
    def __init__(self):
        self.data = defaultdict(list)

    def post(self, agent_name: str, content: str):
        self.data[agent_name].append(content)

    def read_all(self):
        msg = ""
        for agent, entries in self.data.items():
            msg += f"{agent} wrote:\n" + "\n".join(entries) + "\n\n"
        return msg

async def specialist(name: str, task: str, bb: Blackboard):
    client = OllamaChatCompletionClient(model="llama3")
    prompt = f"Task for {name}: {task}\nBlackboard so far:\n{bb.read_all()}"
    resp = await client.create([
        SystemMessage(content=f"You are the {name}, contributing your expertise."),
        UserMessage(content=prompt, source="system")
    ])  # type: ignore
    answer = resp.choices[0].message.content
    bb.post(name, answer)

async def run_blackboard_workflow():
    bb = Blackboard()
    # Radiologist reads initial chart, posts X-ray findings
    await specialist("Radiologist", "Interpret this chest X-ray.", bb)
    # Surgeon reads all posts, adds surgical recommendations
    await specialist("Surgeon", "Given the radiologist’s findings, propose next steps.", bb)
    # Pharmacist posts medication plan
    await specialist("Pharmacist", "Design a medication regimen based on prior notes.", bb)
    # Finally, print the integrated board
    print("=== Final Blackboard ===\n")
    print(bb.read_all())

if __name__ == "__main__":
    asyncio.run(run_blackboard_workflow())
```

---

### Choosing & Combining Patterns

* **Simple Q\&A** → Reactive
* **Multi-step tasks** → Deliberative or BDI
* **Complex state & goals** → BDI
* **Cross-domain expertise** → Blackboard / multi-agent

In practice you’ll often **layer** these: e.g. a BDI agent whose **Intentions** phase uses a deliberative planner, or a reactive “emergency handler” embedded within a larger BDI system. Pick the pattern(s) whose abstractions (stimulus, beliefs, plans, shared workspace) map most naturally to your problem domain.





===============================================================================================


===============================================================================================



### AI Agent Design Patterns with AutoGen

Design patterns for AI agents provide structured approaches to solving common problems in multi-agent systems. Below are key patterns with real-world analogies and implementations using AutoGen.

---

#### 1. **Orchestrator-Worker Pattern**
**Explanation**: A central orchestrator decomposes tasks and assigns subtasks to specialized workers.  
**Real-World Analogy**: A restaurant kitchen where the head chef (orchestrator) delegates tasks (e.g., chopping, grilling) to sous chefs (workers).  

**Implementation**:
```python
from autogen import AssistantAgent, UserProxyAgent, GroupChat, GroupChatManager

config_list = [{"model": "gpt-4", "api_key": "YOUR_API_KEY"}]

# Create agents
user_proxy = UserProxyAgent(
    name="User_Proxy",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "coding"},
)

orchestrator = AssistantAgent(
    name="Orchestrator",
    llm_config={"config_list": config_list},
    system_message="Break tasks into steps. Assign them by mentioning Worker1 or Worker2.",
)

worker1 = AssistantAgent(
    name="Worker1",
    llm_config={"config_list": config_list},
    system_message="You are a math expert. Only respond when mentioned.",
)

worker2 = AssistantAgent(
    name="Worker2",
    llm_config={"config_list": config_list},
    system_message="You analyze if numbers are even/odd. Only respond when mentioned.",
)

# Configure group chat
groupchat = GroupChat(
    agents=[user_proxy, orchestrator, worker1, worker2],
    messages=[],
    max_round=10,
)
manager = GroupChatManager(groupchat=groupchat, llm_config={"config_list": config_list})

# Initiate task
user_proxy.initiate_chat(
    manager,
    message="Calculate 5 + 3 and determine if the result is even or odd."
)
```

---

#### 2. **Blackboard Pattern**
**Explanation**: Agents collaborate via a shared workspace (blackboard) where they post insights.  
**Real-World Analogy**: Detectives adding clues to a shared board to solve a case.  

**Implementation**:
```python
from autogen import AssistantAgent, UserProxyAgent, GroupChat, GroupChatManager

config_list = [{"model": "gpt-4", "api_key": "YOUR_API_KEY"}]

# Create agents
user_proxy = UserProxyAgent(name="User_Proxy", human_input_mode="NEVER")

analyst = AssistantAgent(
    name="Analyst",
    llm_config={"config_list": config_list},
    system_message="Analyze data and post findings to the blackboard.",
)

researcher = AssistantAgent(
    name="Researcher",
    llm_config={"config_list": config_list},
    system_message="Research information and add it to the blackboard.",
)

synthesizer = AssistantAgent(
    name="Synthesizer",
    llm_config={"config_list": config_list},
    system_message="Synthesize blackboard content into a report.",
)

# Set up blackboard (group chat)
groupchat = GroupChat(
    agents=[user_proxy, analyst, researcher, synthesizer],
    messages=[],
    max_round=12,
)
manager = GroupChatManager(groupchat=groupchat, llm_config={"config_list": config_list})

# Initiate collaboration
user_proxy.initiate_chat(
    manager,
    message="Investigate AI's impact on climate change. Use the blackboard to collaborate.",
)
```

---

#### 3. **Pipeline Pattern**
**Explanation**: Tasks flow sequentially through agents, each handling a specific stage.  
**Real-World Analogy**: An assembly line in a car factory, where each station performs a step (welding, painting, etc.).  

**Implementation**:
```python
from autogen import AssistantAgent, UserProxyAgent, GroupChat, GroupChatManager

config_list = [{"model": "gpt-4", "api_key": "YOUR_API_KEY"}]

# Pipeline stages
data_collector = AssistantAgent(
    name="Data_Collector",
    llm_config={"config_list": config_list},
    system_message="Collect and clean data. Pass output to Analyzer.",
)

analyzer = AssistantAgent(
    name="Analyzer",
    llm_config={"config_list": config_list},
    system_message="Analyze data from Data_Collector. Send insights to Visualizer.",
)

visualizer = AssistantAgent(
    name="Visualizer",
    llm_config={"config_list": config_list},
    system_message="Generate visualizations from Analyzer's insights.",
)

user_proxy = UserProxyAgent(name="User_Proxy", human_input_mode="NEVER")

# Configure pipeline
groupchat = GroupChat(
    agents=[user_proxy, data_collector, analyzer, visualizer],
    messages=[],
    max_round=8,
)
manager = GroupChatManager(groupchat=groupchat, llm_config={"config_list": config_list})

# Initiate pipeline
user_proxy.initiate_chat(
    manager,
    message="Collect global temperature data, analyze trends, and visualize results.",
)
```

---

#### 4. **Decentralized (Peer-to-Peer) Pattern**
**Explanation**: Autonomous agents interact directly without a central authority.  
**Real-World Analogy**: Freelancers collaborating on a project via direct communication.  

**Implementation** (Simplified):
```python
from autogen import AssistantAgent, UserProxyAgent

config_list = [{"model": "gpt-4", "api_key": "YOUR_API_KEY"}]

# Create decentralized agents
agent_a = AssistantAgent(
    name="Agent_A",
    llm_config={"config_list": config_list},
    system_message="You handle data collection.",
)

agent_b = AssistantAgent(
    name="Agent_B",
    llm_config={"config_list": config_list},
    system_message="You analyze data from Agent_A.",
)

user_proxy = UserProxyAgent(
    name="User_Proxy",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "coding"},
)

# Agent A initiates chat with Agent B
user_proxy.initiate_chat(
    agent_a,
    message="Agent_B needs data on recent sales figures. Provide it directly.",
)
```

---

### Key Takeaways:
- **Orchestrator-Worker**: Central task delegation.  
- **Blackboard**: Shared collaboration space.  
- **Pipeline**: Sequential task processing.  
- **Decentralized**: Direct peer-to-peer interaction.  

AutoGen’s `GroupChat` and agent roles simplify implementing these patterns. Adjust system messages and agent configurations to tailor interactions.



===============================================================================================


===============================================================================================



# AI Agent Design Patterns: A Comprehensive Classification

The landscape of artificial intelligence has evolved significantly from simple prompt-response systems to sophisticated agentic architectures that can plan, adapt, and collaborate autonomously. Modern AI agent design patterns provide structured blueprints for building intelligent workflows that mirror human-like reasoning and problem-solving approaches, enabling systems to break down complex tasks, utilize external tools, and continuously improve their performance through iterative processes[1][2][3].

## Core Agentic Design Patterns

The foundation of intelligent AI systems rests on four primary design patterns that have emerged as essential building blocks for creating autonomous and collaborative agents. These patterns represent distinct approaches to structuring AI workflows, each addressing specific aspects of intelligent task execution.

### Planning Pattern

**One-liner: Enables agents to break down complex tasks into smaller, manageable subtasks through strategic decomposition and coordination.**

The Planning Pattern serves as the foundation for systematic problem-solving in agentic systems[3]. This pattern allows agents to approach complex challenges by first developing a comprehensive strategy, then decomposing the overall task into logical stages that can be executed sequentially or in parallel[1]. The pattern involves a central supervisor agent that coordinates the planning phase, utilizing reasoning capabilities to create structured workflows that guide task execution[3].

Advanced implementations of this pattern include techniques such as ReAct (Reasoning and Acting) and ReWOO (Reasoning with Open Ontology), which enhance the planning process by enabling dynamic adaptation and contextual decision-making[3]. ReAct allows agents to switch between reasoning and acting phases, while ReWOO brings broader perspective by incorporating open-world ontology for more informed planning decisions[3].

### Tool Use Pattern

**One-liner: Transforms agents from passive responders into active problem solvers by connecting them with external tools, APIs, and resources.**

The Tool Use Pattern fundamentally expands the capabilities of AI agents beyond pure reasoning by providing access to external systems and resources[3]. This pattern enables agents to perform concrete actions such as fetching live data, executing computations, accessing databases, and interfacing with various APIs[1][3]. The integration of tools allows agents to operate in real-world environments where information retrieval, data manipulation, and external system interaction are essential for task completion.

This pattern represents a critical bridge between the cognitive capabilities of large language models and practical application requirements. By connecting agents to external tools, the pattern enables them to gather up-to-date information, perform calculations, and execute actions that would be impossible through reasoning alone[3].

### Reflection Pattern

**One-liner: Enables agents to evaluate, critique, and iteratively improve their own outputs through self-assessment and refinement cycles.**

The Reflection Pattern incorporates self-evaluation mechanisms that allow agents to review and enhance their performance continuously[1][3]. This pattern mirrors human problem-solving approaches where individuals pause to assess their work, identify potential improvements, and iterate on their solutions. Agents utilizing this pattern can detect errors, optimize their approaches, and refine outputs through multiple revision cycles[3].

The reflection mechanism operates by having agents examine their previous outputs, compare them against quality criteria or objectives, and make necessary adjustments. This iterative improvement process leads to higher-quality results and more robust performance across diverse tasks[1].

### Multi-Agent Collaboration Pattern

**One-liner: Coordinates multiple specialized agents working together on different aspects of complex tasks through role-based collaboration.**

The Multi-Agent Collaboration Pattern represents the most sophisticated approach to agentic system design, enabling multiple agents to work together as a coordinated team[1]. This pattern breaks down complex tasks into subtasks that can be assigned to different specialized agents, each optimized for specific roles such as software engineering, quality assurance, or project management[1]. 

The pattern provides developers with a framework for managing complexity by distributing responsibilities across multiple agents, each with its own workflow, memory, and specialized capabilities[1]. This approach mirrors real-world organizational structures where different team members contribute their expertise to achieve common goals[1].

## Specialized Multi-Agent Architectures

Within the broader Multi-Agent Collaboration Pattern, several specialized architectural approaches have emerged to address different coordination and management needs.

### Collaborative Agents Architecture

**One-liner: Multiple agents contribute domain-specific expertise to different parts of a task while maintaining equal status in the collaboration.**

This architecture organizes agents as peers working together on complementary aspects of a problem, with each agent contributing specialized knowledge or skills[3]. The collaborative model ensures that no single agent dominates the process, instead relying on the collective intelligence of the group to achieve optimal results.

### Supervised Agents Architecture

**One-liner: A central supervisor agent manages and coordinates the entire workflow while delegating specific tasks to subordinate agents.**

In supervised architectures, a master agent takes responsibility for overall coordination, task assignment, and quality verification[3]. This hierarchical approach ensures consistency and helps prevent errors in complex workflows by maintaining centralized oversight and control.

### Hierarchical Teams Architecture

**One-liner: Multi-layered agent organization where higher-level agents handle strategic decisions while lower-level agents focus on execution.**

Hierarchical teams create structured decision-making processes with different levels of agents handling planning, strategy, and execution phases[3]. This architecture is particularly effective for complex workflows requiring layered reasoning and interdependent stages with varying levels of oversight requirements.

## Workflow vs. Agentic Pattern Distinctions

Understanding the fundamental differences between structured workflows and dynamic agentic patterns is crucial for selecting appropriate design approaches for specific use cases.

### Structured Workflows

**One-liner: Follow predefined paths with predictable steps, optimized for consistency and reliability in well-defined scenarios.**

Structured workflows are designed for situations where the exact sequence of steps is known and the problem space is well-defined[2]. These patterns prioritize predictability and consistency, making them ideal for routine tasks or processes with established procedures.

### Dynamic Agentic Patterns

**One-liner: Provide autonomy for agents to make decisions and adapt their course of action based on emerging circumstances and evolving requirements.**

Dynamic agentic patterns excel in scenarios requiring flexibility, adaptation, and autonomous decision-making[2]. These patterns enable agents to respond to unexpected challenges, changing requirements, or ambiguous problem spaces where predefined workflows would be insufficient.

## Conclusion

The landscape of AI agent design patterns reflects the evolution from simple reactive systems to sophisticated autonomous entities capable of planning, collaboration, and continuous improvement. The four core patterns—Planning, Tool Use, Reflection, and Multi-Agent Collaboration—provide foundational frameworks for building intelligent systems that can tackle complex, real-world challenges. The choice between structured workflows and dynamic agentic patterns depends on the specific requirements of the use case, with considerations including predictability needs, complexity levels, and the degree of autonomy required. As these patterns continue to mature, they offer increasingly reliable blueprints for creating scalable, modular, and adaptable AI applications that can operate effectively in diverse domains and scenarios.

Citations:
[1] https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-5-multi-agent-collaboration/
[2] https://www.philschmid.de/agentic-pattern
[3] https://www.projectpro.io/article/agentic-ai-design-patterns/1126
[4] https://www.reddit.com/r/AI_Agents/comments/1f8lfjv/which_ai_agent_design_patterns/
[5] https://www.udemy.com/course/mastering-agentic-design-patterns/
[6] https://arxiv.org/abs/2405.10467
[7] https://www.linkedin.com/pulse/4-main-ai-agent-design-patterns-recommend-andrew-ng-yiman-huang-nwype
[8] https://docs.databricks.com/aws/en/generative-ai/guide/agent-system-design-patterns
[9] https://blog.dailydoseofds.com/p/5-agentic-ai-design-patterns
[10] https://techcommunity.microsoft.com/blog/educatordeveloperblog/ai-agents-the-multi-agent-design-pattern---part-8/4402246

---
Answer from Perplexity: pplx.ai/share



===============================================================================================


===============================================================================================




Below are four self-contained Python snippets—one for each of the primary AI-agent design patterns—using the AutoGen (“autogen”) framework with the Ollama backend. Each is ready to drop into its own file and run (after `pip install autogen-core autogen-ext ollama-client` and setting your Ollama API key if needed).

---

## 1. Planning Pattern

**Analogy:** Like a travel agent who first drafts an itinerary then books each component.
**Pattern:**

1. **Plan**: ask the LLM to break down the goal into steps
2. **Execute**: loop through and run each step

```python
# planning_agent.py
import asyncio
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

async def planning_agent(goal: str):
    client = OllamaChatCompletionClient(model="llama3")

    # 1) PLAN phase
    plan_resp = await client.create([
        SystemMessage(content="You are a meticulous planner."),
        UserMessage(content=f"Decompose this into an ordered list of steps:\nTask: {goal}", source="user")
    ])  # type: ignore
    plan = plan_resp.content.strip()
    print("PLAN:\n", plan, "\n")

    # 2) EXECUTE phase
    for idx, step in enumerate(plan.split("\n"), start=1):
        exec_resp = await client.create([
            SystemMessage(content=f"You are an executor for step {idx}."),
            UserMessage(content=f"Step {idx}: {step}\nProceed.", source="user")
        ])  # type: ignore
        print(f"Result of step {idx}:", exec_resp.content.strip(), "\n")

if __name__ == "__main__":
    asyncio.run(planning_agent("Research best practices for unit testing and summarize them."))
```

---

## 2. Tool Use Pattern

**Analogy:** Like a chef who reaches for a specific utensil (knife, peeler, thermometer) at each recipe step.
**Pattern:** Agent decides which “tool” to call (calculator, search, etc.) and uses its output in context.

```python
# tool_use_agent.py
import asyncio
from typing import Any, Callable, Dict
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

# 1) Define our simple “calculator” tool
def calculator(expression: str) -> str:
    try:
        return str(eval(expression, {}, {}))
    except Exception as e:
        return f"Error: {e}"

TOOLS: Dict[str, Callable[[str], Any]] = {
    "calculator": calculator
}

async def tool_use_agent(user_query: str):
    client = OllamaChatCompletionClient(model="llama3")
    # Instruct the agent on tool usage
    system = SystemMessage(content=(
        "You are an agent that can call the calculator tool. "
        "When you want to use it, respond with: TOOL:calculator:<expression>"
    ))
    user = UserMessage(content=user_query, source="user")

    resp = await client.create([system, user])  # type: ignore
    text = resp.content.strip()

    if text.startswith("TOOL:"):
        _, tool_name, expr = text.split(":", 2)
        output = TOOLS[tool_name](expr)
        # feed back the tool output
        followup = await client.create([
            system,
            user,
            SystemMessage(content=f"Tool output: {output}"),
            UserMessage(content="Continue.", source="user")
        ])  # type: ignore
        print(followup.content.strip())
    else:
        print(text)

if __name__ == "__main__":
    asyncio.run(tool_use_agent("What is 23 * (7 + 5)?"))
```

---

## 3. Reflection Pattern

**Analogy:** Like a writer who drafts an essay, then critically reviews and revises it to improve clarity and correctness.
**Pattern:**

1. **Draft** an initial answer
2. **Reflect**: critique the draft
3. **Revise**: produce a refined final answer

```python
# reflection_agent.py
import asyncio
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

async def reflection_agent(prompt: str):
    client = OllamaChatCompletionClient(model="llama3")

    # 1) Draft
    draft = await client.create([
        SystemMessage(content="You are a concise assistant."),
        UserMessage(content=prompt, source="user")
    ])  # type: ignore

    # 2) Reflection: ask it to critique its own draft
    critique = await client.create([
        SystemMessage(content="You are your own critic."),
        UserMessage(content=(
            "Here is your draft:\n"
            f"{draft.content.strip()}\n\n"
            "List two ways you could improve clarity or correctness."
        ), source="user")
    ])  # type: ignore

    # 3) Revise based on critique
    revision = await client.create([
        SystemMessage(content="You are now revising the draft."),
        UserMessage(content=(
            "Draft:\n" + draft.content.strip() +
            "\n\nCritique:\n" + critique.content.strip() +
            "\n\nProduce the improved version."
        ), source="user")
    ])  # type: ignore

    print("FINAL ANSWER:\n", revision.content.strip())

if __name__ == "__main__":
    asyncio.run(reflection_agent("Explain Newton’s second law in simple terms."))
```

---

## 4. Multi-Agent Collaboration Pattern

**Analogy:** A cross-functional team (designer, engineer, tester) each contributes to a shared document.
**Pattern:**

* Multiple agents read/write to a **shared board**, building on each other’s outputs.

```python
# multi_agent_collab.py
import asyncio
from collections import defaultdict
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

class Blackboard:
    def __init__(self):
        self.posts = defaultdict(list)
    def post(self, agent: str, content: str):
        self.posts[agent].append(content)
    def view(self) -> str:
        summary = ""
        for agent, entries in self.posts.items():
            summary += f"--- {agent} ---\n" + "\n".join(entries) + "\n\n"
        return summary

async def role_agent(role: str, task: str, board: Blackboard):
    client = OllamaChatCompletionClient(model="llama3")
    prompt = (
        f"Role: {role}\nTask: {task}\n"
        "Current board:\n" + board.view()
    )
    resp = await client.create([
        SystemMessage(content=f"You are the {role}."),
        UserMessage(content=prompt, source="system")
    ])  # type: ignore
    board.post(role, resp.content.strip())

async def main():
    bb = Blackboard()
    await role_agent("Designer", "Propose a UI layout for a weather app.", bb)
    await role_agent("Engineer", "Given the designer’s layout, suggest an implementation stack.", bb)
    await role_agent("Tester", "Outline test cases for this app.", bb)

    print("=== FINAL BLACKBOARD ===\n")
    print(bb.view())

if __name__ == "__main__":
    asyncio.run(main())
```

---

**How to run any snippet**

1. Save to a `.py` file.
2. Ensure you have `autogen-core`, `autogen-ext`, and your Ollama client installed/configured.
3. `python <filename>.py`

Feel free to mix and match these building blocks—e.g. have your **Planning Agent** spawn a **Tool-Use Agent** for individual steps, or embed **Reflection** within a **Multi-Agent** workflow.



===============================================================================================

Prompt Used:

AI Agents four primary design patterns 1. Planning Pattern, 2. Tool Use Pattern, 3. Reflection Pattern, 4. Multi-Agent Collaboration Pattern. Please generate code examples using python autogen ai agents framework.

===============================================================================================




Here are code examples demonstrating the four primary AI agent design patterns using Microsoft's AutoGen framework:

## 1. Planning Pattern Implementation
```python
from autogen import AssistantAgent, UserProxyAgent
import os

# Configure LLM
llm_config = {
    "config_list": [{
        "model": "gpt-4",
        "api_key": os.environ["OPENAI_API_KEY"]
    }]
}

# Create agents
planner = AssistantAgent(
    name="Planner",
    system_message="Break complex tasks into step-by-step plans",
    llm_config=llm_config
)

executor = UserProxyAgent(
    name="Executor",
    code_execution_config={"work_dir": "planning"},
    human_input_mode="NEVER"
)

# Define planning workflow
def plan_and_execute(task: str):
    planner.reset()
    executor.initiate_chat(
        planner,
        message=f"""Create and execute plan for: {task}
        1. Break into subtasks
        2. Sequence steps logically
        3. Validate completeness"""
    )

plan_and_execute("Develop a REST API for inventory management")
```
This implements a planning workflow where the Planner agent decomposes tasks and sequences steps[1][5]. The executor handles code generation validation.

## 2. Tool Use Pattern Implementation
```python
from autogen import AssistantAgent, UserProxyAgent
from autogen.tool_utils import register_function

# Register custom tool
@register_function
def get_stock_price(symbol: str) -> float:
    """Fetch real-time stock price (mock implementation)"""
    prices = {"NVDA": 890.34, "TSLA": 240.67}
    return prices.get(symbol, 0.0)

# Configure agents
trader_agent = AssistantAgent(
    name="Trader",
    system_message="Use tools to analyze financial data",
    llm_config={"config_list": [...]}
)

user_proxy = UserProxyAgent(
    name="UserProxy",
    human_input_mode="NEVER",
    code_execution_config=False
)

# Initiate tool-enabled chat
user_proxy.initiate_chat(
    trader_agent,
    message="Compare NVDA and TSLA performance today"
)
```
Demonstrates tool integration using decorators[6]. The trader agent can now access real-time data through registered functions[3].

## 3. Reflection Pattern Implementation
```python
from autogen import AssistantAgent, UserProxyAgent

coder = AssistantAgent(
    name="Coder",
    system_message="Write Python code for given tasks",
    llm_config={...}
)

reviewer = UserProxyAgent(
    name="Reviewer",
    system_message="Critique code quality and suggest improvements",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "reflection"}
)

def iterative_development(task: str, rounds=3):
    for _ in range(rounds):
        # Coding phase
        coder.initiate_chat(
            reviewer,
            message=task,
            clear_history=True
        )
        
        # Reflection phase
        reviewer.initiate_chat(
            coder,
            message="Provide detailed code review",
            clear_history=True
        )

iterative_development("Implement quantum circuit simulator")
```
Shows iterative refinement through code-review cycles[4]. Agents alternate between generation and critique phases.

## 4. Multi-Agent Collaboration Pattern
```python
from autogen import GroupChat, GroupChatManager, AssistantAgent

# Create specialized agents
architect = AssistantAgent(
    name="Architect",
    system_message="Design system architecture",
    llm_config={...}
)

devops = AssistantAgent(
    name="DevOps",
    system_message="Handle deployment and infrastructure",
    llm_config={...}
)

qa = AssistantAgent(
    name="QA_Engineer",
    system_message="Execute testing procedures",
    llm_config={...}
)

# Configure group chat
group_chat = GroupChat(
    agents=[architect, devops, qa],
    messages=[],
    max_round=10
)

manager = GroupChatManager(groupchat=group_chat, llm_config={...})

# Initiate collaborative task
architect.initiate_chat(
    manager,
    message="Implement CI/CD pipeline for microservices"
)
```
Implements a collaborative team with role specialization[2][5]. The GroupChatManager coordinates interactions between domain experts.

## Key Implementation Notes:
1. Install required packages:
```bash
pip install autogen-agentchat~=0.2
```

2. Set OpenAI API key:
```python
import os
os.environ["OPENAI_API_KEY"] = "your-api-key"
```

3. Execution modes:
- Local: `code_execution_config={"work_dir": "local"}`
- Docker: `use_docker=True`
- Cloud: Configure cloud execution endpoints[1]

These patterns can be combined - agents can use tools while collaborating in reflective planning workflows[6]. The AutoGen framework provides composition primitives for building complex agentic systems[7].

Citations:
[1] https://microsoft.github.io/autogen/0.2/docs/Getting-Started/
[2] https://microsoft.github.io/autogen/0.2/docs/Examples/
[3] https://drlee.io/multi-agent-autogen-with-functions-step-by-step-with-code-examples-2515b3ab2ac6
[4] https://microsoft.github.io/autogen/stable/user-guide/core-user-guide/design-patterns/reflection.html
[5] https://microsoft.github.io/autogen/0.2/docs/Use-Cases/agent_chat/
[6] https://www.datacamp.com/tutorial/autogen-tutorial
[7] https://microsoft.github.io/autogen/stable/index.html
[8] https://microsoft.github.io/autogen/0.2/docs/notebooks/agentchat_auto_feedback_from_code_execution/
[9] https://www.microsoft.com/en-us/research/project/autogen/
[10] https://docs.ag2.ai/latest/docs/use-cases/notebooks/notebooks/agentchat_planning/
[11] https://blog.mlq.ai/building-ai-agents-autogen/
[12] https://www.infogain.com/blog/building-next-gen-ai-agentic-systems-with-autogen/
[13] https://www.kdnuggets.com/top-7-python-frameworks-for-ai-agents
[14] https://guptadeepak.com/crewai-vs-autogen-choosing-the-right-ai-agent-framework/
[15] https://github.com/microsoft/autogen
[16] https://github.com/microsoft/FLAML/blob/main/notebook/autogen_agentchat_auto_feedback_from_code_execution.ipynb
[17] https://github.com/microsoft/FLAML/blob/main/notebook/autogen_agentchat_planning.ipynb

---
Answer from Perplexity: pplx.ai/share


===============================================================================================

From DeepSeek:

===============================================================================================




Here are code examples for the four primary AI agent design patterns using AutoGen. I'll include detailed explanations, real-world analogies, and implementations:

---

### **1. Planning Pattern**
**Concept**: Agents create and execute multi-step plans  
**Analogy**: Project manager breaking down tasks for team members  

```python
from autogen import AssistantAgent, UserProxyAgent

# Configure local LLM (Ollama)
config_list = [{
    "model": "llama3:70b",
    "base_url": "http://localhost:11434/v1",
    "api_key": "ollama"
}]

# Planning Agent
planner = AssistantAgent(
    name="Planner",
    llm_config={"config_list": config_list},
    system_message="""
    You are a planning expert. Create step-by-step plans considering dependencies.
    Example format:
    1. [Task 1] 
    2. [Task 2 (requires Task 1)]
    ..."""
)

# Executor Agent
executor = UserProxyAgent(
    name="Executor",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "planning", "use_docker": False},
    llm_config={"config_list": config_list}
)

# Plan and execute
executor.initiate_chat(
    planner,
    message="Plan and execute a market analysis for electric vehicles in Europe"
)
```

---

### **2. Tool Use Pattern**  
**Concept**: Agents utilize external tools/APIs  
**Analogy**: Chef using kitchen tools to prepare a meal  

```python
from autogen import AssistantAgent, UserProxyAgent

# Tool definition
def calculate(operation: str, numbers: list):
    """Perform mathematical calculations"""
    if operation == "add":
        return sum(numbers)
    elif operation == "multiply":
        result = 1
        for num in numbers:
            result *= num
        return result
    return "Invalid operation"

# Tool-Enabled Agent
tool_user = AssistantAgent(
    name="Tool_Expert",
    llm_config={"config_list": config_list},
    system_message="Use calculate tool when math operations are needed."
)

# User Proxy with tool access
user_proxy = UserProxyAgent(
    name="User_Proxy",
    human_input_mode="NEVER",
    function_map={"calculate": calculate},
    code_execution_config={"work_dir": "tools", "use_docker": False}
)

# Example usage
user_proxy.initiate_chat(
    tool_user,
    message="Multiply 23, 15 and 4 then add 125 to the result"
)
```

---

### **3. Reflection Pattern**  
**Concept**: Agents self-evaluate and improve outputs  
**Analogy**: Author editing draft based on self-review  

```python
from autogen import AssistantAgent, UserProxyAgent

# Primary Agent
writer = AssistantAgent(
    name="Writer",
    llm_config={"config_list": config_list},
    system_message="Generate detailed technical content."
)

# Reflection Agent
editor = AssistantAgent(
    name="Editor",
    llm_config={"config_list": config_list},
    system_message="Critique responses for clarity, accuracy, and completeness."
)

user_proxy = UserProxyAgent(
    name="User_Proxy",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "reflection", "use_docker": False}
)

# Reflection process
user_proxy.initiate_chat(
    writer,
    message="Explain quantum computing basics"
)
user_proxy.initiate_chat(
    editor,
    message=f"Improve this explanation:\n{writer.last_message()}"
)
```

---

### **4. Multi-Agent Collaboration Pattern**  
**Concept**: Multiple agents work together on complex tasks  
**Analogy**: Surgical team performing an operation  

```python
from autogen import AssistantAgent, UserProxyAgent, GroupChat, GroupChatManager

# Configure agents
researcher = AssistantAgent(
    name="Researcher",
    llm_config={"config_list": config_list},
    system_message="Gather and analyze information from various sources."
)

writer = AssistantAgent(
    name="Technical_Writer",
    llm_config={"config_list": config_list},
    system_message="Create structured documents from research data."
)

reviewer = AssistantAgent(
    name="Reviewer",
    llm_config={"config_list": config_list},
    system_message="Ensure accuracy and quality of final output."
)

user_proxy = UserProxyAgent(
    name="User_Proxy",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "collab", "use_docker": False}
)

# Configure group chat
groupchat = GroupChat(
    agents=[user_proxy, researcher, writer, reviewer],
    messages=[],
    max_round=15
)
manager = GroupChatManager(groupchat=groupchat, llm_config={"config_list": config_list})

# Initiate collaboration
user_proxy.initiate_chat(
    manager,
    message="Create comprehensive report on AI ethics in healthcare"
)
```

---

### **Key Implementation Notes**:
1. **Dependencies**:
```bash
pip install pyautogen ollama
ollama pull llama3:70b
```

2. **Hardware Requirements**:
- Minimum 32GB RAM for Llama3 70B
- SSD recommended for better performance

3. **Pattern Enhancements**:
- Add validation layers for tool outputs
- Implement fallback mechanisms for failed steps
- Add memory management for long conversations
- Include human-in-the-loop validation points

4. **Safety Considerations**:
- Use Docker for production deployments
- Add input/output sanitization
- Implement rate limiting
- Add content moderation hooks

These patterns can be combined (e.g., multi-agent collaboration with planning and tool use) for complex workflows. Adjust agent roles and system messages based on your specific use case requirements.


===============================================================================================


===============================================================================================



I'll walk you through the four primary AI agent design patterns and show you how to implement each one using Python's AutoGen framework with a local Llama 3.2 model through Ollama. Think of these patterns as fundamental architectural blueprints that solve different types of collaborative AI problems.

Let me start by explaining what each pattern accomplishes, then we'll build working examples that demonstrate the core concepts in action.

This comprehensive code demonstrates how each of the four primary agent design patterns works in practice. Let me walk you through what makes each pattern special and why you'd choose one over another.

The **Planning Pattern** acts like having a strategic project manager on your team. When you face a complex challenge, rather than diving straight into execution, the planner agent methodically breaks the problem into manageable steps. This approach prevents the common issue of AI agents getting overwhelmed by complexity or missing critical dependencies between tasks. You'll find this pattern particularly valuable for software development projects, business strategy development, or any scenario where systematic thinking trumps reactive problem-solving.

The **Tool Use Pattern** transforms your AI agents from pure conversationalists into capable actors in the real world. Think of tools as prosthetic extensions of the agent's mind - suddenly they can search the web, perform calculations, manipulate files, or integrate with any API you provide. This pattern bridges the gap between AI reasoning and practical utility. The key insight here is the separation between the agent that decides when to use tools and the executor that handles the actual tool operations, which creates better error handling and security boundaries.

The **Reflection Pattern** implements what psychologists call metacognition - thinking about thinking. Rather than accepting the first solution an agent produces, this pattern creates a quality assurance loop where different agents review and refine each other's work. The generator creates initial solutions without pressure for perfection, the critic provides thorough analysis from a different perspective, and the refiner synthesizes improvements. This mimics how human experts often work in high-stakes situations, like surgical teams or NASA mission planning.

The **Multi-Agent Collaboration Pattern** assembles a team of specialists, each with distinct expertise and perspectives. Instead of trying to create one super-agent that handles everything, you leverage the principle of division of labor. The researcher gathers information, the technical expert handles implementation concerns, the creative thinker explores unconventional approaches, and the coordinator synthesizes everything into coherent solutions. This pattern shines when problems require multiple types of expertise that would be difficult to embed in a single agent.

To get started with this code, you'll need to set up Ollama with the Llama 3.2 model locally. The beauty of using a local model is that you maintain complete control over your data and can experiment without API costs. The code includes detailed setup instructions and error handling to guide you through the process.

Each pattern demonstration uses realistic scenarios that showcase the unique strengths of that approach. You can easily adapt the agent roles, system messages, and example problems to match your specific use case. The modular design means you can mix and match patterns - for instance, using planning within a multi-agent collaboration, or adding reflection loops to tool-using agents.

Would you like me to dive deeper into any specific pattern or help you adapt these examples for a particular application you have in mind?


# AI Agent Design Patterns with AutoGen and Local Llama 3.2
# This code demonstrates four core patterns for AI agent collaboration

import autogen
import json
import time
from typing import Dict, List, Any
import requests

# First, let's set up our connection to the local Ollama Llama 3.2 model
# This configuration tells AutoGen how to communicate with our local LLM
def get_ollama_config():
    """
    Configure AutoGen to use local Ollama with Llama 3.2
    This replaces OpenAI's API with our local model endpoint
    """
    return {
        "config_list": [
            {
                "model": "llama3.2",  # The model name as registered in Ollama
                "base_url": "http://localhost:11434/v1",  # Ollama's OpenAI-compatible endpoint
                "api_key": "ollama",  # Placeholder - Ollama doesn't require real API keys
                "api_type": "openai"  # Use OpenAI-compatible format
            }
        ],
        "timeout": 120,
        "temperature": 0.7,
        "max_tokens": 2000
    }

# =============================================================================
# PATTERN 1: PLANNING PATTERN
# =============================================================================
# The Planning Pattern breaks complex tasks into manageable steps
# Think of it like having a project manager who creates detailed plans
# before execution begins

class PlanningPatternDemo:
    """
    The Planning Pattern demonstrates how an agent can decompose
    complex problems into structured, executable steps.
    
    This pattern is essential when you need systematic approach to
    problem-solving rather than ad-hoc responses.
    """
    
    def __init__(self):
        self.llm_config = get_ollama_config()
        
        # The Planner Agent: Responsible for breaking down complex tasks
        # Notice how we give it a specific role and clear instructions
        self.planner = autogen.AssistantAgent(
            name="TaskPlanner",
            system_message="""You are an expert task planner. When given a complex problem:
            1. Break it down into clear, sequential steps
            2. Identify dependencies between steps
            3. Estimate effort for each step
            4. Present a structured plan in JSON format
            
            Always format your response as:
            {
                "task_breakdown": [
                    {"step": 1, "description": "...", "dependencies": [], "effort": "low/medium/high"}
                ]
            }""",
            llm_config=self.llm_config
        )
        
        # The Executor Agent: Takes plans and implements them
        # This separation of concerns makes the system more modular
        self.executor = autogen.AssistantAgent(
            name="TaskExecutor", 
            system_message="""You are a task executor. Given a structured plan:
            1. Execute each step in the correct order
            2. Check dependencies before starting each step
            3. Report progress and any issues encountered
            4. Provide final results summary""",
            llm_config=self.llm_config
        )
        
        # Human proxy allows for human oversight and intervention
        self.user_proxy = autogen.UserProxyAgent(
            name="user_proxy",
            human_input_mode="NEVER",  # Automated for demo purposes
            max_consecutive_auto_reply=10,
            code_execution_config={"work_dir": "planning_output"}
        )
    
    def demonstrate_planning(self, complex_task: str):
        """
        Show how the planning pattern works with a real example
        """
        print(f"\n=== PLANNING PATTERN DEMO ===")
        print(f"Complex Task: {complex_task}")
        
        # Step 1: Planning phase
        # The planner creates a structured approach to the problem
        planning_conversation = autogen.GroupChat(
            agents=[self.planner, self.user_proxy],
            messages=[],
            max_round=3
        )
        
        planning_manager = autogen.GroupChatManager(
            groupchat=planning_conversation,
            llm_config=self.llm_config
        )
        
        # Initiate planning discussion
        self.user_proxy.initiate_chat(
            planning_manager,
            message=f"Please create a detailed plan for: {complex_task}"
        )
        
        return "Planning pattern demonstration completed"

# =============================================================================
# PATTERN 2: TOOL USE PATTERN  
# =============================================================================
# The Tool Use Pattern enables agents to interact with external systems
# Think of tools as extensions of the agent's capabilities

class ToolUsePatternDemo:
    """
    The Tool Use Pattern shows how agents can leverage external tools
    to extend their capabilities beyond text generation.
    
    This is crucial for real-world applications where agents need to
    interact with APIs, databases, file systems, etc.
    """
    
    def __init__(self):
        self.llm_config = get_ollama_config()
        
        # Define available tools that our agent can use
        # Each tool has a clear interface and purpose
        self.tools = {
            "web_search": self._web_search_tool,
            "calculator": self._calculator_tool, 
            "file_operations": self._file_operations_tool
        }
        
        # The Tool User Agent: Knows when and how to use tools
        self.tool_agent = autogen.AssistantAgent(
            name="ToolUser",
            system_message=f"""You are an agent that can use various tools to accomplish tasks.
            
            Available tools: {list(self.tools.keys())}
            
            When you need to use a tool, format your request as:
            TOOL_CALL: tool_name
            PARAMETERS: {{parameter details}}
            
            Always explain why you're using each tool and how it helps solve the problem.
            """,
            llm_config=self.llm_config
        )
        
        # Tool Executor: Handles the actual tool execution
        # This separation allows for better error handling and security
        self.tool_executor = autogen.UserProxyAgent(
            name="ToolExecutor",
            human_input_mode="NEVER",
            max_consecutive_auto_reply=10,
            code_execution_config={"work_dir": "tool_output"},
            function_map=self.tools  # Register our tools
        )
    
    def _web_search_tool(self, query: str) -> str:
        """
        Simulated web search tool - in practice, this would call a real search API
        """
        # This is a mock implementation - replace with actual search API
        return f"Search results for '{query}': [Simulated results - integrate with real search API]"
    
    def _calculator_tool(self, expression: str) -> str:
        """
        Safe calculator tool for mathematical operations
        """
        try:
            # Use eval carefully in production - consider using ast.literal_eval or a math parser
            result = eval(expression, {"__builtins__": {}}, {})
            return f"Calculation result: {expression} = {result}"
        except Exception as e:
            return f"Calculation error: {str(e)}"
    
    def _file_operations_tool(self, operation: str, filename: str, content: str = "") -> str:
        """
        Basic file operations tool
        """
        try:
            if operation == "write":
                with open(f"tool_output/{filename}", "w") as f:
                    f.write(content)
                return f"Successfully wrote to {filename}"
            elif operation == "read":
                with open(f"tool_output/{filename}", "r") as f:
                    content = f.read()
                return f"File content: {content}"
        except Exception as e:
            return f"File operation error: {str(e)}"
    
    def demonstrate_tool_use(self, task_requiring_tools: str):
        """
        Demonstrate how agents can use tools to solve problems
        """
        print(f"\n=== TOOL USE PATTERN DEMO ===")
        print(f"Task: {task_requiring_tools}")
        
        # Create a conversation where the agent can use tools
        tool_conversation = autogen.GroupChat(
            agents=[self.tool_agent, self.tool_executor],
            messages=[],
            max_round=5
        )
        
        tool_manager = autogen.GroupChatManager(
            groupchat=tool_conversation,
            llm_config=self.llm_config
        )
        
        # Start the tool-assisted problem solving
        self.tool_executor.initiate_chat(
            tool_manager,
            message=f"Please solve this task using appropriate tools: {task_requiring_tools}"
        )
        
        return "Tool use pattern demonstration completed"

# =============================================================================
# PATTERN 3: REFLECTION PATTERN
# =============================================================================
# The Reflection Pattern enables agents to review and improve their own work
# This creates a quality assurance loop similar to peer review

class ReflectionPatternDemo:
    """
    The Reflection Pattern demonstrates self-improvement through
    iterative review and refinement.
    
    This pattern is valuable for ensuring quality and catching errors
    that might slip through in single-pass generation.
    """
    
    def __init__(self):
        self.llm_config = get_ollama_config()
        
        # The Generator Agent: Creates initial solutions
        self.generator = autogen.AssistantAgent(
            name="Generator",
            system_message="""You are a solution generator. Create comprehensive responses to given problems.
            Focus on providing complete, detailed solutions. Don't worry about perfection - 
            your work will be reviewed and improved.""",
            llm_config=self.llm_config
        )
        
        # The Critic Agent: Reviews and identifies improvements
        # Notice how the critic has a different perspective and role
        self.critic = autogen.AssistantAgent(
            name="Critic",
            system_message="""You are a critical reviewer. Analyze solutions for:
            1. Accuracy and correctness
            2. Completeness and thoroughness  
            3. Clarity and organization
            4. Potential improvements or missing elements
            
            Provide specific, actionable feedback. Be constructive but thorough.""",
            llm_config=self.llm_config
        )
        
        # The Refiner Agent: Incorporates feedback and improves solutions
        self.refiner = autogen.AssistantAgent(
            name="Refiner", 
            system_message="""You are a solution refiner. Take original solutions and critical feedback
            to create improved versions. Address all valid points raised by the critic while
            maintaining the core value of the original solution.""",
            llm_config=self.llm_config
        )
        
        self.user_proxy = autogen.UserProxyAgent(
            name="user_proxy",
            human_input_mode="NEVER",
            max_consecutive_auto_reply=15
        )
    
    def demonstrate_reflection(self, problem_to_solve: str):
        """
        Show the complete reflection cycle: generate -> critique -> refine
        """
        print(f"\n=== REFLECTION PATTERN DEMO ===")
        print(f"Problem: {problem_to_solve}")
        
        # Multi-round conversation implementing the reflection pattern
        reflection_agents = [self.generator, self.critic, self.refiner, self.user_proxy]
        
        reflection_conversation = autogen.GroupChat(
            agents=reflection_agents,
            messages=[],
            max_round=12,  # Allow multiple rounds of reflection
            speaker_selection_method="round_robin"  # Systematic turn-taking
        )
        
        reflection_manager = autogen.GroupChatManager(
            groupchat=reflection_conversation,
            llm_config=self.llm_config
        )
        
        # Start the reflection process
        initial_message = f"""
        We need to solve this problem using the reflection pattern:
        {problem_to_solve}
        
        Generator: Please create an initial solution.
        Critic: Then review it thoroughly.
        Refiner: Finally, create an improved version.
        """
        
        self.user_proxy.initiate_chat(reflection_manager, message=initial_message)
        
        return "Reflection pattern demonstration completed"

# =============================================================================
# PATTERN 4: MULTI-AGENT COLLABORATION PATTERN
# =============================================================================
# Multiple specialized agents work together on complex problems
# Like having a team of experts with different skills collaborating

class MultiAgentCollaborationDemo:
    """
    The Multi-Agent Collaboration Pattern shows how specialized agents
    can work together, each contributing their expertise.
    
    This pattern is powerful for complex problems that require
    multiple perspectives or skill sets.
    """
    
    def __init__(self):
        self.llm_config = get_ollama_config()
        
        # Research Specialist: Gathers and analyzes information
        self.researcher = autogen.AssistantAgent(
            name="Researcher",
            system_message="""You are a research specialist. Your role is to:
            1. Gather relevant information about topics
            2. Analyze data and identify patterns
            3. Provide evidence-based insights
            4. Cite sources and maintain accuracy""",
            llm_config=self.llm_config
        )
        
        # Technical Specialist: Handles implementation details
        self.technical_expert = autogen.AssistantAgent(
            name="TechnicalExpert", 
            system_message="""You are a technical implementation expert. Focus on:
            1. Technical feasibility and constraints
            2. Implementation strategies and best practices
            3. Potential technical challenges and solutions
            4. Code examples and technical specifications""",
            llm_config=self.llm_config
        )
        
        # Creative Specialist: Provides innovative solutions
        self.creative_thinker = autogen.AssistantAgent(
            name="CreativeThinker",
            system_message="""You are a creative problem solver. Your strengths include:
            1. Thinking outside conventional approaches
            2. Generating multiple alternative solutions
            3. Combining ideas in novel ways
            4. Challenging assumptions and exploring possibilities""",
            llm_config=self.llm_config
        )
        
        # Project Coordinator: Manages collaboration and synthesis
        self.coordinator = autogen.AssistantAgent(
            name="ProjectCoordinator",
            system_message="""You are the project coordinator. Your responsibilities:
            1. Facilitate collaboration between team members
            2. Synthesize different perspectives into coherent solutions
            3. Identify when more input is needed from specific experts
            4. Ensure all aspects of the problem are addressed""",
            llm_config=self.llm_config
        )
        
        self.user_proxy = autogen.UserProxyAgent(
            name="user_proxy",
            human_input_mode="NEVER",
            max_consecutive_auto_reply=20
        )
    
    def demonstrate_collaboration(self, complex_challenge: str):
        """
        Show how multiple agents collaborate on a complex problem
        """
        print(f"\n=== MULTI-AGENT COLLABORATION DEMO ===")
        print(f"Challenge: {complex_challenge}")
        
        # All agents participate in collaborative problem solving
        collaboration_agents = [
            self.researcher, 
            self.technical_expert, 
            self.creative_thinker, 
            self.coordinator,
            self.user_proxy
        ]
        
        # Custom speaker selection for more natural collaboration
        def custom_speaker_selection(last_speaker, groupchat):
            """
            Intelligent speaker selection based on conversation flow
            """
            messages = groupchat.messages
            if len(messages) <= 1:
                return self.coordinator  # Coordinator starts
            
            last_message = messages[-1]["content"].lower()
            
            # Route based on content and needs
            if "research" in last_message or "data" in last_message:
                return self.researcher
            elif "technical" in last_message or "implementation" in last_message:
                return self.technical_expert  
            elif "creative" in last_message or "alternative" in last_message:
                return self.creative_thinker
            else:
                return self.coordinator  # Default coordinator
        
        collaboration_conversation = autogen.GroupChat(
            agents=collaboration_agents,
            messages=[],
            max_round=20,
            speaker_selection_method=custom_speaker_selection
        )
        
        collaboration_manager = autogen.GroupChatManager(
            groupchat=collaboration_conversation,
            llm_config=self.llm_config
        )
        
        # Initiate collaborative problem solving
        collaboration_prompt = f"""
        Team, we have a complex challenge that requires all our expertise:
        {complex_challenge}
        
        Coordinator: Please orchestrate our collaborative approach.
        Each team member should contribute their specialized perspective.
        Let's work together to develop a comprehensive solution.
        """
        
        self.user_proxy.initiate_chat(collaboration_manager, message=collaboration_prompt)
        
        return "Multi-agent collaboration demonstration completed"

# =============================================================================
# MAIN DEMONSTRATION ORCHESTRATOR
# =============================================================================

class AgentPatternShowcase:
    """
    Orchestrates demonstrations of all four agent design patterns
    """
    
    def __init__(self):
        # Initialize all pattern demonstrations
        self.planning_demo = PlanningPatternDemo()
        self.tool_use_demo = ToolUsePatternDemo() 
        self.reflection_demo = ReflectionPatternDemo()
        self.collaboration_demo = MultiAgentCollaborationDemo()
    
    def run_all_demonstrations(self):
        """
        Run comprehensive demonstrations of all four patterns
        """
        print("=== AI AGENT DESIGN PATTERNS DEMONSTRATION ===")
        print("Using AutoGen framework with local Llama 3.2 via Ollama\n")
        
        # Pattern 1: Planning
        print("1. Demonstrating PLANNING PATTERN...")
        self.planning_demo.demonstrate_planning(
            "Create a comprehensive marketing strategy for a new AI product launch"
        )
        
        # Pattern 2: Tool Use  
        print("\n2. Demonstrating TOOL USE PATTERN...")
        self.tool_use_demo.demonstrate_tool_use(
            "Calculate the ROI for three different marketing campaigns and save the analysis to a file"
        )
        
        # Pattern 3: Reflection
        print("\n3. Demonstrating REFLECTION PATTERN...")
        self.reflection_demo.demonstrate_reflection(
            "Design an efficient algorithm for real-time recommendation systems"
        )
        
        # Pattern 4: Multi-Agent Collaboration
        print("\n4. Demonstrating MULTI-AGENT COLLABORATION PATTERN...")
        self.collaboration_demo.demonstrate_collaboration(
            "Develop a sustainable smart city initiative that balances technology, environment, and social needs"
        )
        
        print("\n=== ALL PATTERN DEMONSTRATIONS COMPLETED ===")
        print("Each pattern showcases different approaches to AI agent collaboration:")
        print("- Planning: Systematic task decomposition")
        print("- Tool Use: External capability integration") 
        print("- Reflection: Iterative improvement through self-review")
        print("- Multi-Agent: Specialized expertise collaboration")

# =============================================================================
# USAGE AND SETUP INSTRUCTIONS
# =============================================================================

def setup_instructions():
    """
    Provide clear setup instructions for running this code
    """
    print("""
    SETUP INSTRUCTIONS:
    
    1. Install Ollama:
       - Visit https://ollama.ai and install for your platform
       - Start Ollama service
    
    2. Pull Llama 3.2 model:
       ollama pull llama3.2
    
    3. Install Python dependencies:
       pip install pyautogen requests
    
    4. Verify Ollama is running:
       curl http://localhost:11434/api/tags
    
    5. Run this script:
       python agent_patterns_demo.py
    
    CUSTOMIZATION OPTIONS:
    - Modify model name in get_ollama_config() for different models
    - Adjust temperature and max_tokens for different response styles
    - Extend tool functions with real API integrations
    - Customize agent roles and system messages for your use case
    """)

if __name__ == "__main__":
    # Display setup instructions
    setup_instructions()
    
    # Create and run the comprehensive demonstration
    showcase = AgentPatternShowcase()
    
    try:
        showcase.run_all_demonstrations()
    except Exception as e:
        print(f"Error during demonstration: {e}")
        print("Make sure Ollama is running and Llama 3.2 model is available")



===============================================================================================


===============================================================================================



You're absolutely right to ask for separate programs. Having each pattern as its own focused example makes it much easier to understand the core concepts without distraction, and you can run and experiment with each pattern independently. Let me break these down into four distinct programs that you can study and modify one at a time.



===============================================================================================


===============================================================================================


Here are 4 separate Python programs demonstrating each design pattern using Llama3-70b via Ollama with AutoGen:

---

### **1. Planning Pattern** (`planning_pattern.py`)
```python
from autogen import AssistantAgent, UserProxyAgent

# Ollama configuration
config_list = [
    {
        "model": "llama3:70b",
        "base_url": "http://localhost:11434/v1",
        "api_key": "ollama"
    }
]

# Planning agent with chain-of-thought capability
planner = AssistantAgent(
    name="Planner",
    llm_config={"config_list": config_list},
    system_message="""You are an expert planner. Create detailed, step-by-step plans.
    Consider dependencies between tasks. Format output as:
    1. [Task 1]
    2. [Task 2 (requires Task 1)]
    ..."""
)

# Execution agent
executor = UserProxyAgent(
    name="Executor",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "planning", "use_docker": False},
    llm_config={"config_list": config_list}
)

# Plan and execute workflow
executor.initiate_chat(
    planner,
    message="Create and execute a plan to analyze COVID-19 impact on global e-commerce trends"
)
```

---

### **2. Tool Use Pattern** (`tool_use_pattern.py`)
```python
from autogen import AssistantAgent, UserProxyAgent

config_list = [
    {
        "model": "llama3:70b",
        "base_url": "http://localhost:11434/v1",
        "api_key": "ollama"
    }
]

# Custom tool definition
def financial_calculator(principal: float, rate: float, years: int):
    """Calculate compound interest"""
    amount = principal * (1 + rate/100) ** years
    return round(amount, 2)

# Tool-enabled agent
finance_agent = AssistantAgent(
    name="Financial_Analyst",
    llm_config={"config_list": config_list},
    system_message="Use financial_calculator for all math operations. Always specify parameters."
)

# User proxy with tool access
user_proxy = UserProxyAgent(
    name="User_Proxy",
    human_input_mode="NEVER",
    function_map={"financial_calculator": financial_calculator},
    code_execution_config={"work_dir": "tools", "use_docker": False}
)

# Example usage
user_proxy.initiate_chat(
    finance_agent,
    message="Calculate compound interest for $5000 at 5% APR over 10 years"
)
```

---

### **3. Reflection Pattern** (`reflection_pattern.py`)
```python
from autogen import AssistantAgent, UserProxyAgent

config_list = [
    {
        "model": "llama3:70b",
        "base_url": "http://localhost:11434/v1",
        "api_key": "ollama"
    }
]

# Primary content generator
researcher = AssistantAgent(
    name="Researcher",
    llm_config={"config_list": config_list},
    system_message="Generate detailed technical content about AI safety."
)

# Reflection agent for quality control
validator = AssistantAgent(
    name="Validator",
    llm_config={"config_list": config_list},
    system_message="Critique content for accuracy, bias, and clarity. Suggest improvements."
)

user_proxy = UserProxyAgent(
    name="User_Proxy",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "reflection", "use_docker": False}
)

# Two-phase process
user_proxy.initiate_chat(
    researcher,
    message="Explain the concept of AI alignment in neural networks"
)

user_proxy.initiate_chat(
    validator,
    message=f"Improve this explanation:\n{researcher.last_message()}"
)
```

---

### **4. Multi-Agent Collaboration** (`multi_agent_collab.py`)
```python
from autogen import AssistantAgent, UserProxyAgent, GroupChat, GroupChatManager

config_list = [
    {
        "model": "llama3:70b",
        "base_url": "http://localhost:11434/v1",
        "api_key": "ollama"
    }
]

# Specialized agents
market_analyst = AssistantAgent(
    name="Market_Analyst",
    llm_config={"config_list": config_list},
    system_message="Analyze market trends and competitor data"
)

product_designer = AssistantAgent(
    name="Product_Designer",
    llm_config={"config_list": config_list},
    system_message="Generate product ideas based on market analysis"
)

engineering_lead = AssistantAgent(
    name="Engineering_Lead",
    llm_config={"config_list": config_list},
    system_message="Evaluate technical feasibility of product ideas"
)

user_proxy = UserProxyAgent(
    name="User_Proxy",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "collab", "use_docker": False}
)

# Configure group chat
groupchat = GroupChat(
    agents=[user_proxy, market_analyst, product_designer, engineering_lead],
    messages=[],
    max_round=12
)
manager = GroupChatManager(groupchat=groupchat, llm_config={"config_list": config_list})

# Initiate collaboration
user_proxy.initiate_chat(
    manager,
    message="Develop a smart home device for elderly care considering market needs and technical feasibility"
)
```

---

### **Setup & Execution**
1. **Requirements**:
```bash
pip install pyautogen ollama
ollama pull llama3:70b
```

2. **Run Programs**:
```bash
# Run each pattern separately
python planning_pattern.py
python tool_use_pattern.py 
python reflection_pattern.py
python multi_agent_collab.py
```

3. **Key Features**:
- Local execution with Llama3-70b
- Docker-free configuration
- Separate concerns for each design pattern
- Ollama-specific optimizations
- Error handling for local LLM execution

4. **Performance Tips**:
- Use `llama3:8b` for faster execution on less powerful hardware
- Add `"temperature": 0.3` to config_list for more focused responses
- Increase `max_round` in group chats for complex tasks
- Monitor Ollama logs with `ollama serve` in separate terminal

Each program demonstrates a distinct architectural pattern while maintaining compatibility with local LLM execution through Ollama.




===============================================================================================


===============================================================================================




Below are four standalone Python programs—one per pattern—each targeting a local Llama 3.2 model via Ollama. Save each snippet to its own `.py` file and run with `python <filename>.py` after installing `autogen-core`, `autogen-ext`, and `ollama-client`.

---

### 1. **Planning Pattern** (`planning_agent.py`)

Breaks a goal into steps, then executes them in order.

```python
# planning_agent.py
import asyncio
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

async def planning_agent(goal: str):
    client = OllamaChatCompletionClient(model="llama3.2")
    
    # 1) PLAN phase
    plan_resp = await client.create([  # type: ignore
        SystemMessage(content="You are a meticulous planner."),
        UserMessage(content=f"Decompose this into an ordered list of steps:\nTask: {goal}", source="user")
    ])
    plan = plan_resp.content.strip()
    print("=== PLAN ===\n", plan, "\n")

    # 2) EXECUTE phase
    for idx, step in enumerate(plan.split("\n"), start=1):
        exec_resp = await client.create([  # type: ignore
            SystemMessage(content=f"You are an executor for step {idx}."),
            UserMessage(content=f"Step {idx}: {step}\nProceed.", source="user")
        ])
        print(f"Result of step {idx}:", exec_resp.content.strip(), "\n")

if __name__ == "__main__":
    asyncio.run(planning_agent("Research best practices for unit testing and summarize them."))
```

---

### 2. **Tool Use Pattern** (`tool_use_agent.py`)

Decides at runtime whether to call a calculator “tool” for numeric queries.

```python
# tool_use_agent.py
import asyncio
from typing import Callable, Dict
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

def calculator(expression: str) -> str:
    try:
        return str(eval(expression, {}, {}))
    except Exception as e:
        return f"Error: {e}"

TOOLS: Dict[str, Callable[[str], str]] = {
    "calculator": calculator
}

async def tool_use_agent(query: str):
    client = OllamaChatCompletionClient(model="llama3.2")
    
    system = SystemMessage(content=(
        "You are an agent that can call the calculator tool. "
        "When you want to use it, respond with: TOOL:calculator:<expression>"
    ))
    user = UserMessage(content=query, source="user")

    resp = await client.create([system, user])  # type: ignore
    text = resp.content.strip()

    if text.startswith("TOOL:"):
        _, tool_name, expr = text.split(":", 2)
        output = TOOLS[tool_name](expr)
        followup = await client.create([  # type: ignore
            system,
            user,
            SystemMessage(content=f"Tool output: {output}"),
            UserMessage(content="Continue.", source="user")
        ])
        print(followup.content.strip())
    else:
        print(text)

if __name__ == "__main__":
    asyncio.run(tool_use_agent("What is 23 * (7 + 5)?"))
```

---

### 3. **Reflection Pattern** (`reflection_agent.py`)

Drafts an answer, critiques it, then revises for clarity.

```python
# reflection_agent.py
import asyncio
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

async def reflection_agent(prompt: str):
    client = OllamaChatCompletionClient(model="llama3.2")

    # 1) Draft
    draft = await client.create([  # type: ignore
        SystemMessage(content="You are a concise assistant."),
        UserMessage(content=prompt, source="user")
    ])

    # 2) Critique
    critique = await client.create([  # type: ignore
        SystemMessage(content="You are your own critic."),
        UserMessage(content=(
            "Here is your draft:\n"
            f"{draft.content.strip()}\n\n"
            "List two ways you could improve clarity or correctness."
        ), source="user")
    ])

    # 3) Revise
    revision = await client.create([  # type: ignore
        SystemMessage(content="You are now revising the draft."),
        UserMessage(content=(
            "Draft:\n" + draft.content.strip() +
            "\n\nCritique:\n" + critique.content.strip() +
            "\n\nProduce the improved version."
        ), source="user")
    ])

    print("=== FINAL ANSWER ===\n", revision.content.strip())

if __name__ == "__main__":
    asyncio.run(reflection_agent("Explain Newton’s second law in simple terms."))
```

---

### 4. **Multi-Agent Collaboration Pattern** (`multi_agent_collab.py`)

Several specialist agents write to—and then read from—a shared blackboard.

```python
# multi_agent_collab.py
import asyncio
from collections import defaultdict
from autogen_ext.models.ollama import OllamaChatCompletionClient
from autogen_core.models import SystemMessage, UserMessage

class Blackboard:
    def __init__(self):
        self.posts = defaultdict(list)
    def post(self, agent: str, content: str):
        self.posts[agent].append(content)
    def view(self) -> str:
        summary = ""
        for agent, entries in self.posts.items():
            summary += f"--- {agent} ---\n" + "\n".join(entries) + "\n\n"
        return summary

async def role_agent(role: str, task: str, board: Blackboard):
    client = OllamaChatCompletionClient(model="llama3.2")
    prompt = (
        f"Role: {role}\nTask: {task}\n"
        "Current board:\n" + board.view()
    )
    resp = await client.create([  # type: ignore
        SystemMessage(content=f"You are the {role}."),
        UserMessage(content=prompt, source="system")
    ])
    board.post(role, resp.content.strip())

async def main():
    bb = Blackboard()
    await role_agent("Designer", "Propose a UI layout for a weather app.", bb)
    await role_agent("Engineer", "Given the designer’s layout, suggest an implementation stack.", bb)
    await role_agent("Tester", "Outline test cases for this app.", bb)

    print("=== FINAL BLACKBOARD ===\n")
    print(bb.view())

if __name__ == "__main__":
    asyncio.run(main())
```

---

**Running each program:**

1. Ensure your local Ollama daemon is running with Llama 3.2 available.
2. Install dependencies:

   ```bash
   pip install autogen-core autogen-ext ollama-client
   ```
3. Run:

   ```bash
   python planning_agent.py
   python tool_use_agent.py
   python reflection_agent.py
   python multi_agent_collab.py
   ```



===============================================================================================


===============================================================================================



I'll provide four separate Python programs demonstrating each design pattern using AutoGen with a local Llama3.2 model via Ollama. Each program includes Ollama-specific configuration and can run independently.

## 1. Planning Pattern with Llama3.2
```python
# planning_pattern.py
from autogen import AssistantAgent, UserProxyAgent
import os

# Ollama configuration for Llama3.2
ollama_config = {
    "config_list": [{
        "model": "llama3.2:70b-instruct-q4_K",
        "api_type": "ollama",
        "client_host": "http://localhost:11434"
    }],
    "cache_seed": None
}

# Create planning agents
planner = AssistantAgent(
    name="Planner",
    system_message="""You are a senior project planner. Break complex tasks into executable steps.
    1. Analyze requirements
    2. Identify dependencies
    3. Create timeline
    4. Validate feasibility""",
    llm_config=ollama_config
)

executor = UserProxyAgent(
    name="Executor",
    code_execution_config={"work_dir": "planning"},
    human_input_mode="NEVER"
)

def plan_task(task_description: str):
    executor.initiate_chat(
        planner,
        message=f"Create implementation plan for: {task_description}",
        clear_history=True
    )

if __name__ == "__main__":
    plan_task("Develop a blockchain-based voting system")
```

## 2. Tool Use Pattern with Llama3.2
```python
# tool_use_pattern.py
from autogen import AssistantAgent, UserProxyAgent
from autogen.tool_utils import register_function
import os

# Ollama configuration
ollama_config = {
    "config_list": [{
        "model": "llama3.2:70b-instruct-q4_K",
        "api_type": "ollama",
        "client_host": "http://localhost:11434"
    }]
}

# Register custom tool
@register_function
def analyze_sentiment(text: str) -> dict:
    """Perform sentiment analysis (mock implementation)"""
    return {
        "positive": 0.85,
        "negative": 0.10,
        "neutral": 0.05
    }

# Create tool-enabled agent
analyst = AssistantAgent(
    name="DataAnalyst",
    system_message="Use available tools to analyze data",
    llm_config=ollama_config
)

proxy = UserProxyAgent(
    name="UserProxy",
    human_input_mode="NEVER",
    code_execution_config=False
)

if __name__ == "__main__":
    proxy.initiate_chat(
        analyst,
        message="Analyze sentiment in customer reviews from Q3",
        clear_history=True
    )
```

## 3. Reflection Pattern with Llama3.2
```python
# reflection_pattern.py
from autogen import AssistantAgent, UserProxyAgent
import os

# Ollama configuration
ollama_config = {
    "config_list": [{
        "model": "llama3.2:70b-instruct-q4_K",
        "api_type": "ollama",
        "client_host": "http://localhost:11434"
    }]
}

# Create reflective agents
writer = AssistantAgent(
    name="TechnicalWriter",
    system_message="Create comprehensive technical documentation",
    llm_config=ollama_config
)

editor = UserProxyAgent(
    name="Editor",
    system_message="Provide constructive feedback on documentation quality",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "reflection"}
)

def refine_documentation(topic: str):
    for _ in range(3):
        writer.initiate_chat(
            editor,
            message=f"Draft documentation about: {topic}",
            clear_history=True
        )
        editor.initiate_chat(
            writer,
            message="Suggest improvements for clarity and completeness",
            clear_history=True
        )

if __name__ == "__main__":
    refine_documentation("Neural network quantization techniques")
```

## 4. Multi-Agent Collaboration Pattern
```python
# multi_agent_pattern.py
from autogen import AssistantAgent, GroupChat, GroupChatManager
import os

# Ollama configuration
ollama_config = {
    "config_list": [{
        "model": "llama3.2:70b-instruct-q4_K",
        "api_type": "ollama",
        "client_host": "http://localhost:11434"
    }]
}

# Create specialized agents
research_lead = AssistantAgent(
    name="ResearchLead",
    system_message="Coordinate AI research initiatives",
    llm_config=ollama_config
)

data_engineer = AssistantAgent(
    name="DataEngineer",
    system_message="Design and implement data pipelines",
    llm_config=ollama_config
)

ethics_officer = AssistantAgent(
    name="EthicsOfficer",
    system_message="Ensure ethical AI development practices",
    llm_config=ollama_config
)

# Configure group collaboration
group_chat = GroupChat(
    agents=[research_lead, data_engineer, ethics_officer],
    messages=[],
    max_round=8
)

manager = GroupChatManager(
    groupchat=group_chat,
    llm_config=ollama_config
)

if __name__ == "__main__":
    research_lead.initiate_chat(
        manager,
        message="Develop responsible AI guidelines for healthcare diagnostics",
        clear_history=True
    )
```

## Setup Instructions

1. Install required packages:
```bash
pip install pyautogen[ollama] ollama-python
```

2. Start Ollama service:
```bash
ollama serve
```

3. Pull Llama3.2 model:
```bash
ollama pull llama3.2:70b-instruct-q4_K
```

4. Set environment variables:
```bash
export OLLAMA_HOST=localhost:11434
```

Key implementation details:
- Each agent uses the `llama3.2:70b-instruct-q4_K` quantization
- Explicit `client_host` configuration for local Ollama instance
- Separate code execution directories per pattern
- Three refinement iterations in reflection pattern
- Group chat management with role specialization
- Tool registration with type hinting for better LLM understanding

The patterns can be extended by combining multiple approaches (e.g., adding reflection to multi-agent workflows) while maintaining local execution through Ollama's inference engine.

Citations:
[1] https://microsoft.github.io/autogen/0.2/docs/topics/non-openai-models/local-ollama/
[2] https://www.youtube.com/watch?v=-WqHY3uE_K0
[3] https://pypi.org/project/ollama-python/
[4] https://www.reddit.com/r/LocalLLaMA/comments/17811ai/are_there_any_guides_to_using_a_local_llm_with/
[5] https://microsoft.github.io/autogen/stable/user-guide/agentchat-user-guide/tutorial/agents.html
[6] https://docs.ag2.ai/docs/api-reference/autogen/register_function
[7] https://www.datacamp.com/tutorial/autogen-tutorial
[8] https://microsoft.github.io/autogen/stable/reference/python/autogen_ext.models.ollama.html
[9] https://microsoft.github.io/autogen/stable/user-guide/core-user-guide/design-patterns/group-chat.html
[10] https://microsoft.github.io/autogen/0.2/docs/reference/agentchat/user_proxy_agent/
[11] https://gist.github.com/mberman84/ea207e7d9e5f8c5f6a3252883ef16df3
[12] https://www.glukhov.org/post/2024/12/ollama-cheatsheet/
[13] https://docs.ag2.ai/docs/api-reference/autogen/AssistantAgent
[14] https://github.com/microsoft/autogen/issues/4452
[15] https://adasci.org/how-to-build-a-multi-agent-system-with-autogen/
[16] https://microsoft.github.io/autogen/stable/user-guide/core-user-guide/components/model-clients.html
[17] https://microsoft.github.io/autogen/stable/user-guide/core-user-guide/cookbook/local-llms-ollama-litellm.html
[18] https://microsoft.github.io/autogen/stable/reference/python/autogen_agentchat.agents.html
[19] https://www.gettingstarted.ai/run-autogen-agents-with-ollama-locally/
[20] https://www.youtube.com/watch?v=rdPi9KD7XKs
[21] https://www.youtube.com/watch?v=IjqAMWUI0r8
[22] https://microsoft.github.io/autogen/0.2/docs/ecosystem/ollama/
[23] https://microsoft.github.io/autogen/0.2/docs/tutorial/tool-use/
[24] https://github.com/microsoft/autogen/discussions/3937
[25] https://www.gettingstarted.ai/autogen-multi-agent-workflow-tutorial/
[26] https://python.langchain.com/docs/integrations/chat/ollama/
[27] https://www.linkedin.com/posts/iromin_autogen-groupchat-tutorial-activity-7255117807548256256-7HwA
[28] https://github.com/microsoft/autogen/issues/3279
[29] https://www.kaggle.com/code/anandsiva/autogen-groupchat-with-rag
[30] https://microsoft.github.io/autogen/stable/user-guide/agentchat-user-guide/tutorial/human-in-the-loop.html
[31] https://github.com/meyiapir/autogen-example/blob/main/AutoGen_Example.ipynb
[32] https://github.com/microsoft/autogen/issues/4332
[33] https://github.com/microsoft/autogen/discussions/5254
[34] https://www.reddit.com/r/AutoGenAI/comments/1j3bpxf/autogen_v048_released/
[35] https://docs.spring.io/spring-ai/reference/api/chat/ollama-chat.html
[36] https://github.com/microsoft/autogen/discussions/3957
[37] https://microsoft.github.io/autogen/0.2/docs/notebooks/agentchat_groupchat/
[38] https://microsoft.github.io/autogen/0.2/docs/reference/agentchat/groupchat/
[39] https://www.youtube.com/watch?v=1jtLevuIqV4
[40] https://www.gettingstarted.ai/autogen-conversation-patterns-workflows/
[41] https://microsoft.github.io/autogen/0.2/docs/tutorial/conversation-patterns/
[42] https://microsoft.github.io/autogen-for-net/articles/Create-a-user-proxy-agent.html
[43] https://docs.ag2.ai/latest/docs/api-reference/autogen/UserProxyAgent/
[44] https://www.youtube.com/watch?v=ZJMsZSjC8HY

---
Answer from Perplexity: pplx.ai/share



===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================


===============================================================================================







===============================================================================================

