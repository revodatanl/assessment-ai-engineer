# RevoData's Technical Assessment

- [RevoData's Technical Assessment](#revodatas-technical-assessment)
  - [Introduction](#introduction)
    - [The Scenario](#the-scenario)
    - [Goal](#goal)
  - [Assessment Pathway](#assessment-pathway)
      - [Core Deliverables](#core-deliverables)
      - [What We're Looking For](#what-were-looking-for)
      - [Project Constraints](#project-constraints)
  - [Deliverables](#deliverables)
  - [Review](#review)

## Introduction

This assessment is an opportunity to show us how you think about and build GenAI applications. There are no trick questions and no single correct answer — we want to see how you approach a real-world problem, make trade-offs, and communicate your decisions.

### The Scenario

Imagine you are an AI engineer at a company that has obtained a large collection of public-domain books from [Project Gutenberg](https://www.gutenberg.org/). Leadership wants you to explore how to unlock the value of this literary catalogue using GenAI. There are no constraints on what you build — whether that's a retrieval-augmented system, an agentic workflow, a structured extraction pipeline, or something we haven't thought of. Pick whatever approach lets you best demonstrate how you think and build.

You have been given a way to get the data which you can find in `notebooks/sample.ipynb`.

### Goal

Build a GenAI application — or the key components of one — that demonstrates your ability to turn raw text data into a useful, production-oriented AI system. Think of it as a proof-of-concept that you would demo to a technical stakeholder.

**Examples of what your application could do** (pick one, combine several, or think of your own):

- Answer questions about the content of the books
- Recommend books based on a reader's description of what they are looking for
- Summarize or compare books, themes, or authors
- Extract structured information (characters, locations, themes) from unstructured text
- Any other creative idea — surprise us

---

## Assessment Pathway

_For candidates applying to the **AI Engineer** role._

Your focus is on **GenAI techniques and engineering practices**, using whatever tools and frameworks you are most productive with. If you use Databricks components for your solution, that is a plus, but it is not required for this assessment.

#### Core Deliverables

Build a GenAI application (or its key components) that demonstrates your ability to design and implement GenAI systems. Depending on your chosen approach, we expect to see several of the following:

1. **Ingest & prepare** the book data for use in a GenAI context (chunking strategy, embedding, optional local vector storage)
2. **Implement a retrieval pipeline** (RAG, semantic search, or hybrid) that can find relevant passages from the books
3. **Build an LLM-powered component** — this could be a conversational agent, a chain, an extraction pipeline, or something else entirely
4. **Evaluate** your system in some way — even a handful of test cases with expected outputs counts

#### What We're Looking For

- Clean, well-structured notebooks and/or Python modules
- Understanding of GenAI fundamentals: embeddings, retrieval, prompting, evaluation
- Thoughtful design decisions — we care more about **why** you chose an approach than whether it is the most complex one
- A solution that is locally reproducible and easy for us to run
- Bonus points for agentic patterns (tool use, multi-step reasoning), structured output, or creative applications

#### Project Constraints

- The only external API providers your project may require are **Anthropic**, **OpenAI**, or **Mistral** for inference.
- The full project must be reproducible and runnable locally, apart from the chosen inference provider.
- If you use a vector database or other dependencies, it must run locally and be included as a Docker container in the repository setup.
- Prefer simple, self-contained architectures. **Less is more**.
- You may use any framework or evaluation approach that fits these constraints.

## Deliverables

Save everything in a **private Git repository** and share it with us. We expect to find:

| What                                 | Where                                                                                   | Notes                                                                                                                   |
| ------------------------------------ | --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Exploratory work / scratch notebooks | `./scratch/`                                                                            | Show us your thinking process                                                                                           |
| Main application code                | `./src/` or `./notebooks/`                                                              | Whichever fits your approach                                                                                            |
| Documentation                        | `README.md` and optionally `./docs/`                                                    | Your `README.md` should explain what the project does, which problem it solves, how it works, and how to run it locally |
| Tests (if applicable)                | `./tests/`                                                                              | Even a few assertions go a long way                                                                                     |
| Data & outputs                       | `./data/`                                                                               | Include the input data and any generated artifacts                                                                      |
| Requirements / environment           | `requirements.txt`, `pyproject.toml`, `Dockerfile`, `docker-compose.yml`, or equivalent | We need to be able to reproduce your setup locally                                                                      |

**Deliver a clean repository.** Remove any redundant files, replace the default README with your own, and provide clear instructions for building and running your project locally.

Your submission `README.md` should make it easy for a reviewer to understand the problem you chose, what the project does, how it works, and the exact steps needed to run it.

**Less is more.** Aim for a focused solution of roughly **2048 lines of code or less** this only includes code files such as `.py/.ipynb/etc.` but not configuration files such as `.env/.docker/.yml/.md/etc.`. We care far more about clear thinking, good trade-offs, and a polished end-to-end demo than about breadth for its own sake.

We expect you to spend **~6 hours** on this assessment. Apply your best judgment when prioritizing — a focused, well-documented solution is far more valuable than a sprawling, half-finished one.

**During the interview, you will be expected to demo your solution live and walk the interviewer through it.** Be prepared to explain your design decisions, show how the application works, and discuss what you would do differently with more time.

## Review

As a note on using AI tools (Claude Code, Cursor, Copilot, etc.), we encourage you to use these tools to enhance your productivity, and we are very curious towards your setup. However, please remember that you are 100% responsible for the code you submit. You need to be able to explain how the code works and discuss the pros and cons of your implementations. please include your `agents.md/.agents/.cursor/.claude/etc.` in your repository.

Please do **not** use AI assistants in any way during the interview. We want to assess your technical skills, problem-solving abilities, and communication skills. Additionally, we want to evaluate your ability to clearly and concisely explain your thoughts.

**Good luck, and see you on the other side!**
