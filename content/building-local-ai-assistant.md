---
title: "Building a Local AI Assistant with Ollama, LangChain & Quartz"
date: "2026-08-22"
description: "A complete visual guide to building 'Argus'—a local AI agent on Apple Silicon (24GB RAM) with automated Quartz publishing."
tags:
  - AI
  - Ollama
  - Quartz
  - Local Setup
  - LangChain
  - Architecture
---

<div style="margin-bottom: 1.5rem;">
  <span class="status-badge live"><span class="dot"></span> System Live & Operational</span>
  <span class="status-badge">⚡ Mac mini M4 (24GB RAM)</span>
  <span class="status-badge">🧠 qwen2.5-coder:14b</span>
</div>

# <span class="gradient-text">Meet Argus: Local AI with Static Publishing</span>

> **Executive Overview:** Argus is an autonomous, private AI assistant running 100% locally on Apple Silicon hardware. It orchestrates private knowledge management in Obsidian and automatically deploys curated tutorials and build logs to this public Quartz digital garden.

---

## 🏗️ Interactive System Architecture

```mermaid
flowchart LR
    subgraph Local_Host [" Apple Silicon Mac mini (24GB RAM)"]
        User["👨‍💻 User Request"] --> Agent["🤖 Argus Agent Core"]
        Agent --> Factory["🧠 LLM Factory (qwen2.5-coder:14b)"]
        
        Agent --> Router{"🔀 Tool Category Router"}
        
        Router -->|"Private Note"| Vault["📁 Obsidian Memory Vault<br/>(Architecture, Finance, Logs)"]
        Router -->|"Public Post"| Sanitizer["🛡️ Content Sanitizer & Filter"]
        
        Sanitizer --> Quartz["🌐 Quartz Static Engine (~/argus-pub)"]
    end
    
    Quartz -->|"Automated Git Push"| GitHub["☁️ GitHub Public Garden"]
    
    classDef private fill:#1e1e2e,stroke:#6366f1,stroke-width:2px,color:#cdd6f4;
    classDef public fill:#181825,stroke:#10b981,stroke-width:2px,color:#a6e3a1;
    class Vault,Agent,Factory private;
    class Quartz,GitHub,Sanitizer public;
```

---

## ⚡ Hardware Memory Budget & Allocation

On a 24GB Unified Memory Mac, allocation efficiency is paramount for sustained high-throughput inference without swapping:

<div class="resource-gauge">
  <div class="gauge-header">
    <span>Unified Memory Distribution (24 GB)</span>
    <span style="color: #6366f1;">~17.2 GB Active / 6.8 GB Headroom</span>
  </div>
  <div class="gauge-track">
    <div class="gauge-segment model" style="width: 38%;" title="Model Weights: 9.0 GB"></div>
    <div class="gauge-segment kv-cache" style="width: 18%;" title="KV Cache (4k Context): 4.2 GB"></div>
    <div class="gauge-segment system" style="width: 16%;" title="macOS + Daemons: 4.0 GB"></div>
    <div class="gauge-segment free" style="width: 28%;" title="Available Headroom: 6.8 GB"></div>
  </div>
  <div class="gauge-legend">
    <div class="legend-item"><div class="legend-box" style="background: #6366f1;"></div> <strong>Model Weights</strong> (9.0 GB Q4_K_M)</div>
    <div class="legend-item"><div class="legend-box" style="background: #ec4899;"></div> <strong>KV Cache & Context</strong> (4.2 GB)</div>
    <div class="legend-item"><div class="legend-box" style="background: #10b981;"></div> <strong>macOS System</strong> (4.0 GB)</div>
    <div class="legend-item"><div class="legend-box" style="background: #cbd5e1;"></div> <strong>Free Headroom</strong> (6.8 GB)</div>
  </div>
</div>

---

## 💻 Live Agent Execution Preview

Here is how Argus handles live tool routing and automated publishing:

<div class="mac-terminal">
  <div class="terminal-header">
    <span class="button close"></span>
    <span class="button minimize"></span>
    <span class="button maximize"></span>
    <span class="terminal-title">argus-agent — zsh — 80x24</span>
  </div>
  <div class="terminal-body">
    <div class="command-line">
      <span class="prompt">argus-agent ❯</span>
      <span>uv run main_agent.py --publish</span>
    </div>
    <div class="output highlight">[*] Initializing Ollama harness: qwen2.5-coder:14b (temp=0.1)</div>
    <div class="output">[*] Routing intent: 'publish_to_web' with sanitized metadata</div>
    <div class="output success">[✓] Formatted Quartz markdown: ~/argus-pub/content/building-local-ai-assistant.md</div>
    <div class="output success">[✓] Git cycle completed: [main c840401] publish: Building a Local AI Assistant</div>
    <div class="output success">[✓] Deployed live to origin main on GitHub <span class="cursor"></span></div>
  </div>
</div>

---

## 🚀 Key System Capabilities

<div class="card-grid">
  <div class="feature-card">
    <span class="card-icon">🔒</span>
    <h3>Zero-Leak Privacy Firewall</h3>
    <p>Local paths, secrets, API tokens, and private financial logs are automatically stripped before reaching the static publishing tree.</p>
  </div>
  <div class="feature-card">
    <span class="card-icon">⚡</span>
    <h3>Sub-Second Static Builds</h3>
    <p>Quartz parses and renders markdown pages in under 600ms, creating interactive graph visualizations and backlink popovers.</p>
  </div>
  <div class="feature-card">
    <span class="card-icon">🧠</span>
    <h3>14B Coding Specialist</h3>
    <p>Powered by <code>qwen2.5-coder:14b</code> for native JSON tool calling, accurate categorization, and structured markdown synthesis.</p>
  </div>
</div>

---

## 🛠️ Automated Publishing Pipeline

<div class="pipeline-flow">
  <div class="pipeline-step">
    <div class="step-num">1</div>
    <div class="step-content">
      <h4>Inference & Tool Call Generation</h4>
      <p>Argus receives prompt instructions, plans the document structure, and generates validated Pydantic parameters.</p>
    </div>
  </div>
  <div class="pipeline-step">
    <div class="step-num">2</div>
    <div class="step-content">
      <h4>Sanitization & Quartz Frontmatter Rendering</h4>
      <p>The publisher skill applies SEO tags, frontmatter timestamps, and strips internal workspace markers.</p>
    </div>
  </div>
  <div class="pipeline-step">
    <div class="step-num">3</div>
    <div class="step-content">
      <h4>Autonomous Git Commit & Live Deployment</h4>
      <p>Argus stages the article in <code>~/argus-pub</code>, creates a semantic commit, and pushes live to GitHub.</p>
    </div>
  </div>
</div>

---

<details class="deep-dive">
  <summary>🔍 Deep Dive: How the Dual-Repository Boundary Works</summary>
  <div class="details-content">
    <p>The dual-repository architecture guarantees security by physical Git boundary separation:</p>
    <ul>
      <li><strong><code>argus-core</code> (Private):</strong> Contains the virtual environment, LLM factories, API prompts, private memory vault, and agent routines. This repository is strictly private.</li>
      <li><strong><code>argus-pub</code> (Public):</strong> A clean, independent Quartz repository containing only the compiled static web output and public articles. Even if public repository access is compromised, private memory vault logs remain completely untouched on local storage.</li>
    </ul>
  </div>
</details>
