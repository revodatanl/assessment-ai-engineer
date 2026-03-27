# RevoData's Technical Assessment

- [RevoData's Technical Assessment](#revodatas-technical-assessment)
  - [Introduction](#introduction)
    - [The Scenario](#the-scenario)
    - [Goal](#goal)
  - [Choose Your Pathway](#choose-your-pathway)
    - [🅰️ Pathway: Databricks AI Engineer](#️-pathway-databricks-ai-engineer)
      - [Core Deliverables](#core-deliverables)
      - [What We're Looking For](#what-were-looking-for)
      - [Recommended Tools \& References](#recommended-tools--references)
    - [🅱️ Pathway: AI Engineer (GenAI)](#️-pathway-ai-engineer-genai)
      - [Core Deliverables](#core-deliverables-1)
      - [What We're Looking For](#what-were-looking-for-1)
      - [You Are Free to Use](#you-are-free-to-use)
  - [Deliverables (Both Pathways)](#deliverables-both-pathways)
  - [Review](#review)

## Introduction

This assessment is an opportunity to show us how you think about and build GenAI applications. There are no trick questions and no single correct answer — we want to see how you approach a real-world problem, make trade-offs, and communicate your decisions.

### The Scenario

Imagine you are an AI engineer at a company that has obtained a large collection of public-domain books from [Project Gutenberg](https://www.gutenberg.org/). Leadership wants you to explore how to unlock the value of this literary catalogue using GenAI. There are no constraints on what you build — whether that's a retrieval-augmented system, an agentic workflow, a structured extraction pipeline, or something we haven't thought of. Pick whatever approach lets you best demonstrate how you think and build.

You have been given a way to get the data which you can find in `data/starter.ipynb`.

### Goal

Build a GenAI application — or the key components of one — that demonstrates your ability to turn raw text data into a useful, production-oriented AI system. Think of it as a proof-of-concept that you would demo to a technical stakeholder.

**Examples of what your application could do** (pick one, combine several, or think of your own):

- Answer questions about the content of the books
- Recommend books based on a reader's description of what they are looking for
- Summarize or compare books, themes, or authors
- Extract structured information (characters, locations, themes) from unstructured text
- Any other creative idea — surprise us

---

## Choose Your Pathway

This assessment has **two pathways**. Pick the one that matches the role you are applying for. The core problem is the same; what differs is the tooling and platform emphasis.

---

### 🅰️ Pathway: Databricks AI Engineer

_For candidates applying to the **Databricks AI Engineer** role._

Your focus is on building within the **Databricks Data Intelligence Platform**, leveraging its native GenAI capabilities.

#### Core Deliverables

Build a GenAI application (or its key components) that demonstrates your ability to work with the Databricks AI stack. Depending on your chosen approach, we expect to see several of the following:

1. **Ingest & prepare** the book data for use in a GenAI context (chunking, parsing, storage in Unity Catalog)
2. **Enable retrieval** over the book content using Vector Search
3. **Build an AI-powered component** using the Agent Framework, or a compatible framework like LangGraph / LangChain via `databricks-langchain`
4. **Serve a foundation model** through Foundation Model APIs or AI Gateway
5. **Log and evaluate** your application using MLflow (tracing, evaluation metrics, or AI-assisted judges)

#### What We're Looking For

- Familiarity with the Databricks GenAI ecosystem: Unity Catalog, Vector Search, Agent Framework, Model Serving, MLflow
- Clean, well-structured notebooks and/or Python modules
- Thoughtful design decisions — we care more about **why** you chose an approach than whether it is the most complex one
- Evidence that you tested or evaluated your system (even a small eval set counts)

#### Recommended Tools & References

- [Agent Framework tutorial](https://docs.databricks.com/aws/en/generative-ai/tutorials/agent-framework-notebook)
- [GenAI capabilities overview](https://docs.databricks.com/aws/en/generative-ai/guide/mosaic-ai-gen-ai-capabilities)
- [RAG on Databricks](https://docs.databricks.com/aws/en/generative-ai/retrieval-augmented-generation)
- [Databricks Free Edition](https://www.databricks.com/learn/free-edition)

---

### 🅱️ Pathway: AI Engineer (GenAI)

_For candidates applying to the **AI Engineer** role._

Your focus is on **GenAI techniques and engineering practices**, using whatever tools and frameworks you are most productive with.

#### Core Deliverables

Build a GenAI application (or its key components) that demonstrates your ability to design and implement GenAI systems. Depending on your chosen approach, we expect to see several of the following:

1. **Ingest & prepare** the book data for use in a GenAI context (chunking strategy, embedding, storage in a vector store of your choice)
2. **Implement a retrieval pipeline** (RAG, semantic search, or hybrid) that can find relevant passages from the books
3. **Build an LLM-powered component** — this could be a conversational agent, a chain, an extraction pipeline, or something else entirely
4. **Evaluate** your system in some way — even a handful of test cases with expected outputs counts

#### What We're Looking For

- Clean, well-structured notebooks and/or Python modules
- Understanding of GenAI fundamentals: embeddings, retrieval, prompting, evaluation
- Thoughtful design decisions — we care more about **why** you chose an approach than whether it is the most complex one
- Bonus points for agentic patterns (tool use, multi-step reasoning), structured output, or creative applications

#### You Are Free to Use

- Any LLM provider (OpenAI, Anthropic, local models, etc.)
- Any framework (LangChain, LangGraph, LlamaIndex, Haystack, Pydantic AI, OpenAI Agents SDK, or plain Python)
- Any vector store (Chroma, FAISS, Pinecone, Weaviate, Qdrant, or anything else)
- Any evaluation approach (custom scripts, RAGAS, MLflow, DeepEval, etc.)

## Deliverables (Both Pathways)

Save everything in a **private Git repository** and share it with us. We expect to find:

| What | Where | Notes |
|------|-------|-------|
| Exploratory work / scratch notebooks | `./scratch/` | Show us your thinking process |
| Main application code | `./src/` or `./notebooks/` | Whichever fits your approach |
| Documentation | `README.md` and optionally `./docs/` | Explain the **why**, not the how |
| Tests (if applicable) | `./tests/` | Even a few assertions go a long way |
| Data & outputs | `./data/` | Include the input data and any generated artifacts |
| Requirements / environment | `requirements.txt`, `pyproject.toml`, or equivalent | We need to be able to reproduce your setup |

**Deliver a clean repository.** Remove any redundant files, replace the default README with your own, and provide clear instructions for building and running your project.

We expect you to spend **3–4 hours** on this assessment. Apply your best judgment when prioritizing — a focused, well-documented solution is far more valuable than a sprawling, half-finished one.

## Review

As a note on using AI tools (Claude Code, Cursor, Copilot, etc.), we encourage you to use these tools to enhance your productivity, and we are very curious towards your setup. However, please remember that you are 100% responsible for the code you submit. You need to be able to explain how the code works and discuss the pros and cons of your implementations.

Please do **not** use AI assistants in any way during the interview. We want to assess your technical skills, problem-solving abilities, and communication skills. Additionally, we want to evaluate your ability to clearly and concisely explain your thoughts.

**Good luck, and see you on the other side!**
