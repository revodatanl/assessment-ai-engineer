# RevoData's Technical Assessment

- [RevoData's Technical Assessment](#revodatas-technical-assessment)
  - [Introduction](#introduction)
    - [The Scenario](#the-scenario)
    - [Goal](#goal)
  - [Assessment](#assessment)
    - [Core Deliverables](#core-deliverables)
    - [What We're Looking For](#what-were-looking-for)
    - [Project Constraints](#project-constraints)
  - [Deliverables](#deliverables)
  - [Review](#review)

## Introduction

This assessment is an opportunity to show us how you think about and build GenAI applications. There are no trick questions and no single correct answer — we want to see how you approach a real-world problem, make trade-offs, and communicate your decisions.

### The Scenario

Imagine you are an AI engineer at a company that has obtained a large collection of public-domain books from [Project Gutenberg](https://www.gutenberg.org/). Leadership wants you to explore how to unlock the value of this literary catalogue using GenAI. There are no constraints on what you build, whether that's a retrieval-augmented system, an agentic workflow, a structured extraction pipeline, or something we haven't thought of. Pick whatever approach lets you best demonstrate how you think and build.

You have been given a way to get the data which you can find in `notebooks/sample.ipynb`.

### Goal

Build a **proof-of-concept** GenAI application on top of the book data, then show how you make it **measurably better**. The heart of this assessment is not the size of what you build; it is your ability to **establish a baseline, evaluate it, iterate, and demonstrate improvement with numbers**.

Think of it as a proof-of-concept you would demo to a technical stakeholder: small, runnable, and backed by evidence that your changes actually helped. The [Core Deliverables](#core-deliverables) below break this down into one tight build → evaluate → iterate loop.

**Examples of a use case you could build** (pick one, combine several, or think of your own):

- Answer questions about the content of the books
- Recommend books based on a reader's description of what they are looking for
- Summarize or compare books, themes, or authors
- Extract structured information (characters, locations, themes) from unstructured text
- Any other creative idea; surprise us!

---

## Assessment

Your focus is on **GenAI techniques and engineering practices**, using whatever tools and frameworks you are most productive with.

If you choose to use Databricks components (e.g. for data processing, vector search, model serving, or experiment tracking), that can be a **plus**, but it is **not required**. We care most about a focused, runnable proof-of-concept with clear reasoning and a credible evaluation.

#### Core Deliverables

Your submission should walk us through the full loop below. Keep each step small, **less is more**. The point is not breadth; it is a clean baseline-evaluate-iterate cycle.

1. **Build a proof-of-concept GenAI use case.** Pick one focused task on the book data (e.g. Q&A, recommendation, summarization, structured extraction) and implement just enough to run it end to end. Whatever the approach (RAG, an agent, a chain, an extraction pipeline, …), keep it lean.
2. **Create a baseline evaluation.** Define a benchmark, a set of test cases with expected outputs and one or more metrics; and run it against your first version to establish a baseline score.
3. **Iterate and re-benchmark.** Make at least one deliberate improvement (better prompt, retrieval, chunking, model choice, parameters, …), then **re-run the same benchmark** and report the before/after results.

The deliverable we care about most is the **before → after comparison**: a reproducible benchmark showing that your iteration moved the numbers in the right direction, together with your reasoning about *why* it helped.

#### What We're Looking For

- A **runnable proof-of-concept** GenAI use case, not a sprawling system
- A **credible baseline evaluation**: sensible metric(s), representative test cases, and an honest read of the results
- Clear evidence of **iteration**: a hypothesis, a change, and a **re-run benchmark** that quantifies the impact
- Thoughtful design decisions, we care more about **why** you chose an approach (and what your numbers told you) than about complexity
- Clean, well-structured notebooks and/or Python modules that are easy for us to reproduce locally
- Bonus points for thoughtful metric design, ablations comparing alternatives, agentic patterns, or creative use cases

#### Project Constraints

- The only external API providers your project may require are **Anthropic**, **OpenAI**, **Mistral** or Ollama for local inference. Note that Mistral has a [free API key tier](https://docs.mistral.ai/getting-started/quickstarts/studio/activate-and-generate-api-key) (no credit card required).
- The full project must be reproducible and runnable locally, apart from the chosen inference provider.
- If you use a vector database or other dependencies, it must run locally and be included as a Docker container in the repository setup.
- Prefer simple, self-contained architectures. **Less is more**.
- You may use any framework or evaluation approach that fits these constraints.

## Deliverables

Save everything in a **private Git repository** and share it with us. We expect to find:


| What                                 | Where                                                                                   | Notes                                                                                                                                                                                                                                                          |
| ------------------------------------ | --------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Exploratory work / scratch notebooks | `./scratch/`                                                                            | Show us your thinking process                                                                                                                                                                                                                                  |
| Main application code                | `./src/` or `./notebooks/`                                                              | Whichever fits your approach                                                                                                                                                                                                                                   |
| Evaluation & benchmark               | wherever fits your approach (e.g. `./evals/` or a notebook)                             | The benchmark, baseline scores, and the **before → after** comparison from your iteration                                                                                                                                                                      |
| Documentation                        | `README.md` plus `Architecture.md` (or `./docs/architecture.md`)                        | `README.md` should explain what the project does, which problem it solves, and how to run it locally; `Architecture.md` should give a short architecture overview (boundaries, main components, and data flow — a C4-style context + container view is enough) |
| Tests (if applicable)                | `./tests/`                                                                              | Even a few assertions go a long way                                                                                                                                                                                                                            |
| Data & outputs                       | `./data/`                                                                               | Include the input data and any generated artifacts                                                                                                                                                                                                             |
| Requirements / environment           | `requirements.txt`, `pyproject.toml`, `Dockerfile`, `docker-compose.yml`, or equivalent | We need to be able to reproduce your setup locally                                                                                                                                                                                                             |


**Deliver a clean repository.** Remove any redundant files, replace the default README with your own, and provide clear instructions for building and running your project locally.

Your submission `README.md` should make it easy for a reviewer to understand the problem you chose, what the project does, how it works, and the exact steps needed to run it.

**Less is more.** Aim for a focused solution of roughly **2048 lines of code or less** this only includes code files such as `.py/.ipynb/etc.` but not configuration files such as `.env/.docker/.yml/.md/etc.`. We care far more about clear thinking, good trade-offs, and a polished end-to-end demo than about breadth for its own sake.

We expect you to spend **~6 hours** on this assessment. Apply your best judgment when prioritizing, a focused, well-documented solution is far more valuable than a sprawling, half-finished one.

**During the interview, you will be expected to demo your solution live and walk the interviewer through it.** Be prepared to explain your design decisions, show how the application works, and discuss what you would do differently with more time.

## Review

As a note on using AI tools (Claude Code, Cursor, Copilot, etc.), we encourage you to use these tools to enhance your productivity, and we are very curious towards your setup. However, please remember that you are 100% responsible for the code you submit. You need to be able to explain how the code works and discuss the pros and cons of your implementations. please include your `agents.md/.agents/.cursor/.claude/etc.` in your repository.

Please do **not** use AI assistants in any way during the interview. We want to assess your technical skills, problem-solving abilities, and communication skills. Additionally, we want to evaluate your ability to clearly and concisely explain your thoughts.

**Good luck, and see you on the other side!**
