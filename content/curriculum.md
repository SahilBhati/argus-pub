---
title: "Zero-to-Hero Local AI Agent Engineering Curriculum"
description: "A complete, ground-zero learning journey and open documentation curriculum on building autonomous local AI agents, memory vaults, and edge deployments."
---

<div style="margin-bottom: 1.5rem;">
  <span class="status-badge live"><span class="dot"></span> Open Curriculum</span>
  <span class="status-badge">🎓 Ground Zero to Production</span>
  <span class="status-badge">⚡ Apple Silicon & Ollama</span>
</div>

# <span class="gradient-text">Zero-to-Hero AI Agent Engineering</span>

> **Welcome to the public learning curriculum!** This curriculum documents our ground-zero journey of mastering local LLMs, agentic tool dispatching, persistent memory vaults, and global edge publishing on Apple Silicon. Follow along and build your own autonomous assistant step-by-step.

---

## 🗺️ Curriculum Roadmap

```mermaid
flowchart LR
    M1["📍 Module 1<br/>Local AI & Apple Silicon"] --> M2["📍 Module 2<br/>Tool Calling & ReAct"]
    M2 --> M3["📍 Module 3<br/>Memory & Knowledge Vaults"]
    M3 --> M4["📍 Module 4<br/>Model Context Protocol"]
    M4 --> M5["📍 Module 5<br/>Edge Publishing Pipeline"]

    classDef active fill:#1e1e2e,stroke:#6366f1,stroke-width:2px,color:#cdd6f4;
    class M1,M2,M3,M4,M5 active;
```

---

## 📚 Course Modules

<div class="curriculum-grid">

  <!-- Module 1 -->
  <div class="curriculum-module active">
    <div class="module-header">
      <span class="module-badge">Track 1 • Hardware & Inference</span>
      <span class="status-pill in-progress">⚡ In Progress</span>
    </div>
    <h3>Module 1: Local AI & Apple Silicon Inference Mechanics</h3>
    <p>Understand how Large Language Models execute locally on Apple Silicon. Demystify Unified Memory bandwidth, 4-bit quantization (Q4_K_M), KV Cache allocation, and the Ollama runtime engine.</p>
    <div class="topic-list">
      <span class="topic-tag">Unified Memory</span>
      <span class="topic-tag">Q4_K_M Quantization</span>
      <span class="topic-tag">KV Cache Math</span>
      <span class="topic-tag">Ollama Daemon</span>
      <span class="topic-tag">qwen2.5-coder:14b</span>
    </div>
    <a href="/module-1-local-ai-inference-mechanics" style="display: inline-flex; align-items: center; gap: 6px; font-weight: 600; font-size: 0.875rem; color: #6366f1;">
      <span>Read Lesson 1: Demystifying Local Inference →</span>
    </a>
  </div>

  <!-- Module 2 -->
  <div class="curriculum-module">
    <div class="module-header">
      <span class="module-badge">Track 2 • Agent Tooling</span>
      <span class="status-pill upcoming">⏳ Upcoming</span>
    </div>
    <h3>Module 2: Tool Calling & The ReAct Execution Loop</h3>
    <p>How does a text-generating neural network execute Python functions and web searches? Learn JSON schema tool binding, the ReAct pattern (Reason + Act), and streaming SSE token updates.</p>
    <div class="topic-list">
      <span class="topic-tag">Function Calling</span>
      <span class="topic-tag">ReAct Synthesis Loop</span>
      <span class="topic-tag">Server-Sent Events (SSE)</span>
      <span class="topic-tag">FastAPI Async Engine</span>
    </div>
  </div>

  <!-- Module 3 -->
  <div class="curriculum-module">
    <div class="module-header">
      <span class="module-badge">Track 3 • Long-Term Memory</span>
      <span class="status-pill upcoming">⏳ Upcoming</span>
    </div>
    <h3>Module 3: Memory Systems & Obsidian Knowledge Graph</h3>
    <p>Build persistent, human-readable long-term memory for local agents. Implement taxonomy categorization, YAML frontmatter indexing, and hybrid semantic retrieval across Obsidian markdown notes.</p>
    <div class="topic-list">
      <span class="topic-tag">Obsidian Vault</span>
      <span class="topic-tag">Frontmatter Taxonomy</span>
      <span class="topic-tag">Hybrid RAG</span>
      <span class="topic-tag">Vector Embeddings</span>
    </div>
  </div>

  <!-- Module 4 -->
  <div class="curriculum-module">
    <div class="module-header">
      <span class="module-badge">Track 4 • Tool Standards</span>
      <span class="status-pill upcoming">⏳ Upcoming</span>
    </div>
    <h3>Module 4: The Model Context Protocol (MCP) in Practice</h3>
    <p>Demystify Anthropic's Model Context Protocol (the USB-C of AI integrations). Connect MCP servers to external databases, GitHub, filesystem APIs, and custom local tools.</p>
    <div class="topic-list">
      <span class="topic-tag">Model Context Protocol</span>
      <span class="topic-tag">MCP Server Harness</span>
      <span class="topic-tag">External DB Connectors</span>
      <span class="topic-tag">Sandboxed Execution</span>
    </div>
  </div>

  <!-- Module 5 -->
  <div class="curriculum-module">
    <div class="module-header">
      <span class="module-badge">Track 5 • Production Edge</span>
      <span class="status-pill upcoming">⏳ Upcoming</span>
    </div>
    <h3>Module 5: Automated Edge Deployments & Cloudflare Workers</h3>
    <p>Take insights from local memory and deploy them globally to 300+ edge locations in sub-seconds using Cloudflare Workers Static Assets, Quartz, and automated Git CI/CD pipelines.</p>
    <div class="topic-list">
      <span class="topic-tag">Cloudflare Workers</span>
      <span class="topic-tag">Quartz SSG</span>
      <span class="topic-tag">Automated CI/CD</span>
      <span class="topic-tag">Edge Caching</span>
    </div>
  </div>

</div>

---

## 🎯 How to Learn with Us

1. **Follow the Lessons**: Each module contains theory, hardware benchmarks, code walkthroughs, and runnable examples.
2. **Build Along**: All code is open and reproducible on an Apple Silicon Mac or modern Linux workstation.
3. **Ask Questions**: Interact with Argus or contribute suggestions to our public repository!
