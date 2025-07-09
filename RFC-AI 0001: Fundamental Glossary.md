-----

## RFC-AI 0001: Fundamental Glossary of AI/ML/LLM/Agents

Internet-Draft AI-RFC Initiative Steering Group
Intended Status: Informational May 3, 2025
Expires: November 3, 2025

### Abstract

This document establishes a **fundamental glossary of key terms** related to Artificial Intelligence (AI), Machine Learning (ML), Large Language Models (LLMs), and Multi-Agent Systems (MAS). The primary goal is to provide clear, concise, and consensual definitions to facilitate precise communication and reduce ambiguity in the development, deployment, and standardization of these technologies. This glossary serves as an informational document that lays the groundwork for future RFC-AIs, ensuring that all participants in the RFC-AI Initiative and the broader community use a common, understood language.

### Status of This Memo

This Internet-Draft is a work in progress and does not represent the standard of any organization. It is being distributed for review and consideration by the community interested in the standardization of AI, LLM, and Agent technologies. Comments on this draft should be sent to the RFC-AI Initiative mailing list (mailing\_list\_address@example.com) or to the Steering Group.

Internet-Drafts are working documents of the Internet Engineering Task Force (IETF), its areas, and its working groups. Note that other groups may also distribute working documents as Internet-Drafts. Internet-Drafts are draft documents valid for a maximum of six months and may be updated, replaced, or obsoleted by other documents at any time. It is inappropriate to use Internet-Drafts as reference material or to cite them other than as "work in progress."

### Table of Contents

1.  Introduction
2.  General AI Terms
3.  Machine Learning (ML) Terms
4.  Large Language Model (LLM) Terms
5.  Agent and Multi-Agent System Terms
6.  AI Security and Accountability Terms
7.  Security Considerations
8.  Privacy Considerations
9.  AI-Specific Considerations
10. References
11. Author's Address

-----

### 1\. Introduction

The field of Artificial Intelligence and its subfields, such as Machine Learning and Large Language Models, are evolving at a dizzying pace. This rapid evolution has led to a proliferation of terminology, often used inconsistently or ambiguously among different researchers, developers, regulators, and the general public. This lack of a common language hinders effective communication, impedes interoperability, and creates barriers to understanding and standardization.

The purpose of this RFC-AI 0001 is to establish a **fundamental glossary** of key terms, providing clear, concise, and consensual definitions. This document is *informational* in nature and aims to be a basic reference for all subsequent RFC-AI documents, as well as for anyone working with or interested in the field. By agreeing on standard terminology, we can build a solid foundation for future standardization efforts in areas such as AI interoperability, security, accountability, and evaluation.

The definitions presented here aim to be technologically neutral where possible, focusing on the concept rather than a specific implementation, and are subject to revision as the field evolves.

-----

### 2\. General AI Terms

  * **Artificial Intelligence (AI):** A field of computer science dedicated to creating systems or machines that can perform tasks typically requiring human intelligence, such as learning, problem-solving, perception, language understanding, and decision-making.
  * **AI Algorithm:** A set of computational rules or instructions designed to perform a specific task within an AI system, often by learning from data.
  * **AI Model:** The representation of knowledge or patterns learned by an AI algorithm from data. It's the output of the training process and is used to make predictions or decisions.
  * **AI System:** A system comprising an AI model, the data feeding it (input), the infrastructure supporting it, and the mechanisms for its deployment and operation, which interacts with an environment to achieve objectives.
  * **Agent (in AI):** An autonomous entity that perceives its environment through sensors and acts upon that environment through actuators, to achieve specific goals or tasks.
  * **Autonomous Agent:** An agent that operates without continuous human intervention, making decisions and executing actions independently within a predefined framework or rules.
  * **Inference (in AI):** The process of using an already trained AI model to make predictions, decisions, or generate outputs from new input data.
  * **Training (in AI):** The process of feeding an AI algorithm with data to adjust the internal parameters of a model, enabling it to learn patterns, make predictions, or perform a specific task.
  * **Prompt Engineering:** The process of designing and refining text inputs (prompts) for AI systems, especially LLMs, in order to guide their behavior and obtain desired outputs.
  * **Bias (in AI Models):** A systematic and reproducible tendency in an AI model that leads to unfair, inaccurate, or discriminatory outcomes for certain groups or cases, often due to biases in the training data or algorithm design.
  * **Explainable AI (XAI):** The ability of an AI system to explain its behavior, decisions, or predictions in a human-understandable manner.

-----

### 3\. Machine Learning (ML) Terms

  * **Machine Learning (ML):** A subfield of AI focused on developing algorithms that enable systems to learn from data, identify patterns, and make decisions with minimal human intervention.
  * **Dataset:** A structured collection of data used for training, validating, or testing Machine Learning models.
  * **Supervised Learning:** A type of ML where the model learns from input data that is paired with correct output results or labels.
  * **Unsupervised Learning:** A type of ML where the model seeks hidden patterns or structures in input data without predefined labels.
  * **Reinforcement Learning:** A type of ML where an agent learns to make decisions by interacting with an environment, receiving rewards or penalties for its actions.
  * **Cross-validation:** A technique for evaluating the performance of an ML model by dividing the dataset into multiple subsets for iterative training and testing.
  * **Overfitting:** A phenomenon where an ML model learns the training data too specifically, including noise, resulting in poor performance on new, unseen data.
  * **Underfitting:** A phenomenon where an ML model is too simple to capture the underlying patterns in the data, leading to poor performance on both training and new data.

-----

### 4\. Large Language Model (LLM) Terms

  * **Large Language Model (LLM):** A type of AI model based on deep neural networks (often Transformer architectures) trained on vast amounts of text and code data, capable of understanding, generating, and manipulating human language.
  * **Token:** The basic unit of text that an LLM processes. It can be a whole word, part of a word, or even a character, depending on the tokenizer.
  * **Hallucination (in LLMs):** A phenomenon where an LLM generates information that appears plausible but is incorrect, fabricated, or not supported by its training data or the provided context.
  * **Context (in LLMs):** The preceding input information (prompts, conversation history) that an LLM uses to generate its response. The length of the context is usually limited by the model's context window.
  * **Context Window:** The maximum number of tokens (input and/or output) that an LLM can process or consider in a single interaction or conversation "turn."
  * **Fine-tuning:** The process of further training a pre-trained LLM on a smaller, specific dataset to adapt its capabilities to a particular task or domain.
  * **Natural Language Generation (NLG):** The ability of an AI system to produce coherent and grammatically correct text from structured data or a given context.
  * **Natural Language Understanding (NLU):** The ability of an AI system to interpret and derive meaning from human language.

-----

### 5\. Agent and Multi-Agent System Terms

  * **Multi-Agent System (MAS):** A system composed of multiple autonomous agents that interact with each other and their environment to achieve individual or collective goals.
  * **Agent Coordination:** The process by which multiple agents work together, managing their interactions to achieve a shared goal or avoid conflicts.
  * **Agent Negotiation:** A communication process between agents to reach an agreement on a plan of action or the distribution of resources.
  * **Agent Environment:** The space or context in which an agent operates, interacting with it through perceptions and actions. It can be physical or digital.
  * **Agent Perception:** The information an agent receives from its environment through its sensors.
  * **Agent Action:** An operation an agent can perform in its environment through its actuators.

-----

### 6\. AI Security and Accountability Terms

  * **Adversarial Attack:** A deliberate attempt to trick an AI model by introducing small, imperceptible perturbations to the input data, causing the model to generate an incorrect output.
  * **Prompt Injection:** A type of adversarial attack on LLMs where malicious inputs in the prompt manipulate the model to ignore prior instructions or perform unintended actions.
  * **Jailbreaking (in LLMs):** Techniques used to bypass an LLM's safety guardrails or filters, inducing it to generate content it would normally refuse (e.g., harmful, biased, or dangerous information).
  * **Differential Privacy:** A framework and set of techniques for sharing information about a dataset while protecting the privacy of individuals within that dataset.
  * **Model Stealing/Extraction:** An attack where an adversary infers or reconstructs an AI model, or its properties, by querying the target model via an API.
  * **Data Poisoning:** An attack where malicious data is injected into an AI model's training set to degrade its performance or induce specific unwanted behaviors.
  * **Accountability (in AI):** The ability to attribute and hold individuals or organizations responsible for the outcomes and impact of AI systems, including the ability to audit and trace system decisions.
  * **AI Audit:** The systematic process of evaluating an AI system to verify its compliance with certain standards, policies, or principles, including fairness, transparency, and performance.

-----

### 7\. Security Considerations

This document, being a glossary, does not directly introduce new security vulnerabilities. However, **clear terminology** is fundamental for discussing and addressing security concerns in AI. Ambiguity in terms can lead to misunderstandings in identifying and mitigating risks. The RFC-AI Initiative will consider security as a cross-cutting principle in all future documents defining protocols or architectures.

-----

### 8\. Privacy Considerations

Similar to security, this glossary has no direct privacy implications. Nonetheless, **privacy** is a paramount concern in AI, especially when dealing with personal data. Precise definitions of terms such as "training data," "sensitive data," or "differential privacy" are crucial for developing standards that adequately protect private information.

-----

### 9\. AI-Specific Considerations

This glossary directly addresses many of the key AI-specific considerations, such as **bias/fairness**, **explainability**, and **robustness**, by providing standardized definitions for these concepts. A common understanding of these terms is essential for developing responsible and reliable AI systems. Future RFC-AIs will delve into the technical aspects of how to measure, mitigate, or implement solutions related to these concepts.

-----

### 10\. References

  * [1] ISO/IEC JTC 1/SC 42 Artificial intelligence. [https://www.iso.org/committee/6794461.html](https://www.google.com/search?q=https://www.iso.org/committee/6794461.html)
  * [2] IEEE Standards Association. [https://standards.ieee.org/](https://standards.ieee.org/)
  * [3] National Institute of Standards and Technology (NIST) Artificial Intelligence. [https://www.nist.gov/artificial-intelligence](https://www.nist.gov/artificial-intelligence)
  * [4] RFC-AI 0000: Statement of Purpose and Introduction to the RFC-AI Standardization Initiative. (See link in the repository README).
  * [5] Example Mailing List / Website (Hypothetical). [http://www.example.com/rfc-ai-initiative](https://www.google.com/search?q=http://www.example.com/rfc-ai-initiative)

-----

### 11\. Author's Address

AI-RFC Initiative Steering Group
Mailing Address: mailing\_list\_address@example.com
URI: [http://www.example.com/rfc-ai-initiative](https://www.google.com/search?q=http://www.example.com/rfc-ai-initiative)

-----
