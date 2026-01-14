# Code Scalpel: The Deterministic Engine for AI Agents

**Coming January 2026 | v1.0 Public Release Preview** **License:** MIT (Community)

Code Scalpel is the bridge between **Stochastic AI** (LLMs) and **Reliable Software Engineering**.

It is an **MCP (Model Context Protocol) server** designed to be the primary toolset for AI agents (like Claude, GitHub Copilot, and Cursor). It gives them "Surgical Hands"—replacing probabilistic guesswork with deterministic, graph-based precision.

## The "Day 3" Problem: Why AI Needs our Scalpel

Most companies are stuck on **Day 1** ("Look, it writes code!").
But **Day 3** is coming: **Governance, Security, and Compliance.**

Today's agents treat code as **text**. They read files like a novel, guess line numbers, and "vibe code." In a regulated environment, this leads to:

* **The "Black Box" Risk:** Regulators ask *why* the agent made a decision, and you can't explain it because it was a probabilistic guess.
* **The "Hallucination" Risk:** The agent hallucinates a closing parenthesis `)` or a dependency, breaking the build.
* **The "Blind Spot" Risk:** Generating SQL injection vulnerabilities because the agent can't see data flow across files.

**Code Scalpel is the Adult in the Room.**
It wraps your stochastic agent in a deterministic "Glass Box."

## The Solution: Tools, Not Text

Code Scalpel treats code as a **Mathematical Graph** (AST + PDG). It gives AI agents deterministic tools:

* **Don't read the file** → `extract_code` (Surgical AST Extraction)
* **Don't guess the line** → `update_symbol` (AST-Validated Patching)
* **Don't guess the flow** → `security_scan` (PDG Taint Analysis)
* **Don't guess the logic** → `symbolic_execute` (Z3 Theorem Proving)

---

## The Four Pillars Goal for Code Scalpel

### 1. Governable AI: The Invisible Audit Trail

Compliance isn't sexy, but it's required. Code Scalpel creates a `.code-scalpel/audit.jsonl` trail for every operation.

* **Provenance:** We log the *decision path* (Graph Trace), not just the output.
* **Integrity:** Our `verify_policy_integrity` tool cryptographically ensures your AI follows your security rules without drift.

### 2. Accurate AI: The End of Hallucination

When Code Scalpel says "This function has 3 callers," it is a **Graph Fact**, not an LLM guess.

* **Symbolic Execution:** We use the Z3 solver to mathematically explore edge cases that humans (and LLMs) miss.

### 3. Safer AI: The Syntax-Aware Gatekeeper

We verified this in our recent **[Community Tier Report](./docs/reports/community_tier_report.md)**: Code Scalpel tool use parses every AI edit *before* writing to disk.

* **Scenario:** Agent hallucinates a missing parenthesis `)`.
* **Standard Tool:** Writes file → **Build Breaks.**
* **Code Scalpel:** AST Parser fails → **Edit Rejected & Logged.**

### 4. Cheaper AI: 99% Context Reduction

Instead of feeding 10 full files (15k tokens) to an LLM, Code Scalpel’s **PDG Engine** surgically extracts only the relevant function and its dependencies.

* **Result:** You send 200 tokens instead of 15,000. You save money, and the model focuses better.

---

## Key Capabilities (v1.0) | Jan 2026

Code Scalpel will include **22 specialized tools** divided into five surgical disciplines. All tools are fully operational in the Community Edition.

### 1. Surgical Extraction & Analysis (6 Tools)

*Stop grepping. Start understanding.*

* **`extract_code`**: Surgically extract functions/classes by name (AST-based).
* **`analyze_code`**: Parse structure, complexity, imports, and definitions.
* **`get_project_map`**: Instant high-level topology of the project structure.
* **`get_call_graph`**: Trace execution flow across files.
* **`get_symbol_references`**: Find usages of a symbol across the project.
* **`get_file_context`**: Get surrounding context and metadata.

### 2. Taint-Based Security (6 Tools)

*Real security analysis, not just regex matching.*

* **`security_scan`**: Trace data flow from user input to dangerous sinks (12+ CWEs).
* **`unified_sink_detect`**: Polyglot detection of dangerous sinks.
* **`cross_file_security_scan`**: Track dirty data flow across multiple modules/files.
* **`scan_dependencies`**: Check package dependencies against OSV database.
* **`type_evaporation_scan`**: Detect TypeScript type vulnerabilities at API boundaries.
* **`get_graph_neighborhood`**: Extract k-hop security context around nodes.

### 3. Safe Modification (4 Tools)

* **`update_symbol`**: Atomic replacement with **Syntax Rollback Protection**.
* **`rename_symbol`**: Project-wide refactoring.
* **`simulate_refactor`**: "Dry run" verification before application.
* **`validate_paths`**: Pre-flight path validation (Docker-aware).

### 4. Verification & Testing (4 Tools)

*Trust, but verify.*

* **`symbolic_execute`**: **Provably correct** path exploration using Z3.
* **`generate_unit_tests`**: Auto-create tests from symbolic paths.
* **`crawl_project`**: Project-wide metrics analysis.
* **`verify_policy_integrity`**: Cryptographic policy signature verification.

### 5. Advanced Analysis (2 Tools)

* **`get_cross_file_dependencies`**: Deep dependency chains.
* **`code_policy_check`**: Compliance evaluation (OWASP/SOC2 mapping).

---

## How We're Different

### Code Scalpel vs Python `scalpel` Library

Code Scalpel is NOT a wrapper. It is a completely independent, production-grade MCP server.

| Feature | Code Scalpel | Python `scalpel` |
| :--- | :--- | :--- |
| **Interface** | MCP server (primary) | CLI tool only |
| **Security Scanning** | **PDG Taint Analysis** (Cross-File) | Basic pattern matching |
| **Symbolic Execution** | **Z3-Powered** | Not supported |
| **Safe Refactoring** | **AST-Validated** with Rollback | Manual verification |
| **Auditing** | **Cryptographic Audit Trail** | N/A |

### Code Scalpel vs Other Static Analysis

Most tools are designed for Humans (Linters). Code Scalpel is designed for **Agents**.

| Feature | Code Scalpel | Ruff/Pylint | Semgrep |
| :--- | :--- | :--- | :--- |
| **Primary Use** | **Agent Actuator** | Human Linter | Security Linter |
| **Speed** | 50ms (Deep Analysis) | <10ms (Syntax) | Varies |
| **Depth** | **Cross-File Data Flow** | File-Local | Pattern/Taint |
| **Actionable?** | **Yes (Can Edit Code)** | No (Read Only) | No (Read Only) |
| **Governance** | **Audit Trail + Policy** | Config File | Rules File |

---

## Release Information

**Launch Date**: January 2026
**Version**: v1.0.0
**License**: MIT (Community) | Enterprise (Available)

Code Scalpel is built for the new era of **Agentic Engineering**.
It is the difference between an AI that *guesses* and an AI that *knows*.

*(Installation and usage documentation will be available upon release)*
For more Information reach out to me at time@3dtechsolutions.us or on [LinkedIn](https://www.linkedin.com/in/tescolopio/)
