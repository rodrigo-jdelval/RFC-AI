-----

## RFC-AI 0002: Taxonomy of Agents and Multi-Agent Systems

Internet-Draft AI-RFC Initiative Steering Group
Intended Status: Informational July 9, 2025
Expires: January 9, 2026

### Abstract

This document establishes a **fundamental taxonomy** for classifying and describing different types of **agents** and **multi-agent systems (MAS)** within the context of Artificial Intelligence. With the rapid advancement of AI technologies, especially Large Language Models (LLMs) and their integration into autonomous agent architectures, a critical need arises for a common reference framework for terminology and understanding of these complex systems. This RFC-AI aims to provide clear and consensual definitions for agent categories and MAS structures, facilitating communication, design, development, evaluation, and future standardization in this domain. It serves as an *informational* document, complementing RFC-AI 0001 (Fundamental Glossary).

### Status of This Memo

This Internet-Draft is a work in progress and does not represent the standard of any organization. It is being distributed for review and consideration by the community interested in the standardization of Artificial Intelligence and Agent technologies. Comments on this draft should be sent to the RFC-AI Initiative mailing list (mailing\_list\_address@example.com) or to the Steering Group.

Internet-Drafts are working documents of the Internet Engineering Task Force (IETF), its areas, and its working groups. Please note that other groups may also distribute working documents as Internet-Drafts. Internet-Drafts are draft documents valid for a maximum of six months and may be updated, replaced, or obsoleted by other documents at any time. It is inappropriate to use Internet-Drafts as reference material or to cite them other than as "work in progress."

### Table of Contents

1.  Introduction
2.  Definition of Agent (Review and Expansion)
3.  Classification of Agents by Architecture and Behavior
    3.1. Simple Reflex Agents
    3.2. Model-based Reflex Agents
    3.3. Goal-based Agents
    3.4. Utility-based Agents
    3.5. Learning Agents
    3.6. Hybrid Agents
    3.7. LLM-based Agents
4.  Classification of Multi-Agent Systems (MAS)
    4.1. Cooperative MAS
    4.2. Competitive MAS
    4.3. Hybrid/Coexisting MAS
    4.4. Hierarchical MAS
    4.5. Distributed MAS
5.  Agent Interactions and Communication (Brief Mention)
6.  Security Considerations
7.  Privacy Considerations
8.  AI-Specific Considerations
9.  References
10. Author's Address

-----

### 1\. Introduction

The concept of an "agent" has been fundamental in Artificial Intelligence since its inception, providing a conceptual framework for designing autonomous systems capable of perceiving, reasoning, and acting in complex environments. With the advent of Large Language Models (LLMs) and their increasing integration as core components of agents (the "LLM-based Agents"), as well as the interest in orchestrating multiple such agents into **multi-agent systems (MAS)** to solve complex problems, the diversity of agent architectures and behaviors has proliferated.

While this diversity is a driver of innovation, it also introduces challenges in communication and standardization. The lack of a clear and consensual taxonomy can lead to ambiguities, hinder system comparison, and impede collaborative efforts.

The goal of this RFC-AI 0002 is to provide a classificatory framework for agents and multi-agent systems, building upon fundamental concepts from agent theory and extending them to include emerging architectures. This document is **informational** and aims to offer a common language for describing these systems, which is essential for future RFC-AIs that will address more technical aspects of interoperability, security, and evaluation. It complements RFC-AI 0001 [RFC-AI.0001], which defines the fundamental glossary.

-----

### 2\. Definition of Agent (Review and Expansion)

In the context of this document and the RFC-AI Initiative, an **Agent** is defined as:

An autonomous entity that perceives its **environment** through **sensors** and acts upon that environment through **actuators**, over time, to achieve specific **goals** or **tasks**, exhibiting some degree of **autonomy** and, in many cases, **intelligence**.

**Key Components of an Agent:**

  * **Sensors:** Mechanisms through which the agent receives information from its environment (e.g., cameras, microphones, APIs, data streams).
  * **Actuators:** Mechanisms through which the agent performs actions in its environment (e.g., motors, user interfaces, function calls, code execution).
  * **Environment:** The context or space in which the agent operates and interacts. It can be physical (a robot in a room) or digital (a software agent on a network, an LLM interacting with a database).
  * **Autonomy:** The ability of an agent to operate without constant human intervention, making decisions and executing actions independently within a predefined framework or rules.
  * **Goals/Tasks:** The desired outcomes or actions that the agent is programmed to achieve or perform.

This definition is broad to encompass a variety of implementations, from robotic agents to LLM-based software agents.

-----

### 3\. Classification of Agents by Architecture and Behavior

Agents can be classified according to their internal complexity, reasoning capabilities, and how they make decisions.

#### 3.1. Simple Reflex Agents

  * **Description:** Agents that make decisions purely based on the current perception of the environment, following a set of predefined condition-action rules. They have no internal memory of past perceptions or the effects of their actions.
  * **Characteristics:** Deterministic behavior, fast, stateless, suitable for fully observable environments and clear rules.
  * **Examples:** Thermostat, basic vacuum cleaner agent (turns if it hits something), simple alarm system.

#### 3.2. Model-based Reflex Agents

  * **Description:** Extend simple reflex agents by maintaining an internal state (a "model" of the world) that allows them to track unobservable parts of the environment or remember past perceptions. They use both the current perception and this internal state to make decisions.
  * **Characteristics:** Have memory, can operate in partially observable environments, but still rely on condition-action rules.
  * **Examples:** Navigation agent that remembers a map of an area, traffic control system that tracks vehicle flow.

#### 3.3. Goal-based Agents

  * **Description:** In addition to maintaining a world model, these agents have **goals** they attempt to reach. They use this model and their goals to plan sequences of actions that lead them from the current state to a target state. They require a search or planning capability.
  * **Characteristics:** Goal-directed behavior, planning capability, can explore different action sequences.
  * **Examples:** Route planning agent, chess-playing agent aiming for checkmate, industrial automation system seeking to complete an assembly task.

#### 3.4. Utility-based Agents

  * **Description:** Similar to goal-based agents, but they add a **utility function** that assigns a numerical value to different world states or action sequences. The agent seeks to maximize this utility, allowing it to choose between multiple ways to achieve a goal or weigh conflicting goals. Useful in uncertain environments or with multiple desirable/undesirable outcomes.
  * **Characteristics:** Rationality based on utility optimization, decision-making in uncertain environments, handling tradeoffs.
  * **Examples:** Financial investment agent, medical diagnostic agent weighing risks and benefits, robot control system with limited resource management.

#### 3.5. Learning Agents

  * **Description:** Any agent that improves its performance with experience. They contain a **learning element** (which makes improvements), a **performance element** (which selects external actions), a **critic** (which provides feedback to the learning element on performance), and a **problem generator** (which suggests new actions to explore and learn from).
  * **Characteristics:** Adaptive, capable of improving over time, can discover new rules or strategies.
  * **Examples:** Game-playing agent that improves its strategy, recommendation systems, autonomous vehicles learning to navigate. Can be combined with any of the previous architectures (reflex with learning, goal-based with learning, etc.).

#### 3.6. Hybrid Agents

  * **Description:** Agents that combine two or more of the previous architectures to leverage their strengths. For example, an agent that uses a reactive component for fast actions and a goal-based component for long-term planning.
  * **Characteristics:** Flexible, robust, optimized for different levels of abstraction.
  * **Examples:** A robot that uses reactive rules for immediate obstacle avoidance but plans its route with a global objective, a virtual assistant combining reactive NLU with complex task planning.

#### 3.7. LLM-based Agents

  * **Description:** Agents that utilize one or more Large Language Models (LLMs) as their core reasoning component or "brain." The LLM can be responsible for planning, interpreting perceptions, decision-making, action generation, or interacting with the environment. Often, these agents combine the LLM with other tools (APIs, databases, web search) to extend their capabilities beyond pure text processing.
  * **Characteristics:** Advanced linguistic reasoning capability, flexibility in understanding tasks, adaptability to new instructions, often require mechanisms to prevent hallucinations and manage context. They can exhibit characteristics of goal-based, utility-based, or learning agents, depending on how the LLM and auxiliary tools are used.
  * **Examples:** LLM-powered task automation agents, autonomous research agents, advanced conversational virtual assistants that can use tools.

-----

### 4\. Classification of Multi-Agent Systems (MAS)

A **Multi-Agent System (MAS)** is defined as a system consisting of multiple **agents** that interact with each other (and sometimes with non-agent entities) in a shared **environment** to achieve goals, which can be individual, collective, or a combination.

MAS can be classified according to the nature of agent interaction and organization.

#### 4.1. Cooperative MAS

  * **Description:** Agents in these systems have a common goal and work together to achieve it. They share information, coordinate actions, and may depend on each other.
  * **Characteristics:** Common goal, explicit or implicit coordination, high communication and collaboration.
  * **Examples:** Drone swarms for mapping, collaborative robots on an assembly line, software agents solving a distributed optimization problem.

#### 4.2. Competitive MAS

  * **Description:** Agents in these systems have individual goals that are conflicting or mutually exclusive. They compete for resources, information, or to achieve their own goals before others. Often studied using game theory tools.
  * **Characteristics:** Divergent goals, resource competition, strategic interactions.
  * **Examples:** Trading agents in financial markets, strategic game-playing agents (e.g., chess against another agent), ecological simulations with predator/prey agents.

#### 4.3. Hybrid/Coexisting MAS

  * **Description:** Systems where some agents may cooperate for certain sub-goals, while others compete, or where agents simply coexist and pursue their own goals with minimal or indirect interaction.
  * **Characteristics:** Mix of cooperation and competition, or relative independence.
  * **Examples:** Simulation of a market economy, traffic management systems with autonomous and human-driven vehicles, social simulations.

#### 4.4. Hierarchical MAS

  * **Description:** Interaction and control within the MAS are structured in levels. There are "leader" or "supervising" agents that direct or assign tasks to "subordinate" agents, which in turn may have their own subordinates.
  * **Characteristics:** Tree-like or hierarchical structure, centralized or semi-centralized control, well-defined roles.
  * **Examples:** Fleet control system where a central agent assigns routes to individual vehicle agents, a factory management system with a primary coordinating agent.

#### 4.5. Distributed MAS

  * **Description:** Agents operate more independently, without strong centralized control. Decisions and processing are distributed among agents, who primarily interact peer-to-peer or through a shared environment.
  * **Characteristics:** No single point of failure, robustness, scalability, emergent coordination based on local rules.
  * **Examples:** Distributed sensor networks, grid/cloud computing systems with autonomous task allocation, leaderless robot swarms.

-----

### 5\. Agent Interactions and Communication (Brief Mention)

While this document focuses on taxonomy, it's important to highlight that communication and interaction are pillars of multi-agent systems. Future RFC-AIs will delve into:

  * **Agent Communication Languages (ACLs):** Standardized formats and protocols for agents to exchange messages (e.g., FIPA ACL, KQML).
  * **Coordination Mechanisms:** Methods and algorithms that agents use to coordinate their actions and resolve conflicts.
  * **Negotiation and Agreements:** Processes by which agents reach pacts or contracts regarding tasks or resources.

These topics will be covered in detail in specific RFC-AIs under the "Interoperability Standards" category.

-----

### 6\. Security Considerations

A clear taxonomy is essential for the security of agent and multi-agent systems. Understanding the type of agent or MAS (reactive vs. goal-based, cooperative vs. competitive) is crucial for identifying its specific vulnerabilities. For example, LLM-based agents may be susceptible to "prompt injection" (RFC-AI 0008), while cooperative MAS may be vulnerable to malicious agents subverting coordination. Future RFC-AIs on security will refer to this taxonomy to contextualize threats and countermeasures. Terminological clarity also reduces the risk of design errors that could introduce vulnerabilities.

-----

### 7\. Privacy Considerations

Taxonomy impacts privacy primarily in how agents perceive, process, and share information. Agents with memory (model-based reflex, goal-based, etc.) may retain sensitive data, requiring privacy considerations in their design and lifecycle. In MAS, the way cooperative agents share information could create privacy risks if not managed properly. Identifying the agent and MAS type will facilitate the application of privacy standards (e.g., RFC-AI 0010, RFC-AI 0012) to protect data handled by these systems.

-----

### 8\. AI-Specific Considerations

This taxonomy is fundamental for addressing AI-specific aspects such as **reliability**, **auditability**, and **explainability** in agents and MAS. Different agent types have varying degrees of complexity in their decision-making, which affects their explainability. A simple reflex agent is easier to audit than an LLM-based agent that reasons in a complex manner. This classification helps set realistic expectations for transparency and accountability. Furthermore, understanding the type of interaction in an MAS is vital for ensuring that the emergence of collective behaviors is predictable and controllable.

-----

### 9\. References

  * [1] Russell, S. J., & Norvig, P. (2020). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson. (Foundational reference for traditional agent architectures).
  * [2] Wooldridge, M. (2009). *An Introduction to MultiAgent Systems* (2nd ed.). John Wiley & Sons. (Key reference for MAS).
  * [3] RFC-AI 0000: Statement of Purpose and Introduction to the RFC-AI Standardization Initiative.
  * [4] RFC-AI 0001: Fundamental Glossary of AI/ML/LLM/Agents.
  * [5] RFC-AI 0008: Definition and Classification of Vulnerabilities in LLMs and Agents.
  * [6] RFC-AI 0010: Technical Guide for Training Data Documentation.
  * [7] RFC-AI 0012: Basic Formats for Reporting Model Uncertainty or Confidence.
  * [8] Example Mailing List / Website (Hypothetical). [http://www.example.com/rfc-ai-initiative](https://www.google.com/search?q=http://www.example.com/rfc-ai-initiative)

-----

### 10\. Author's Address

AI-RFC Initiative Steering Group
Mailing Address: mailing\_list\_address@example.com
URI: [http://www.example.com/rfc-ai-initiative](https://www.google.com/search?q=http://www.example.com/rfc-ai-initiative)

-----
