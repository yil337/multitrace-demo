[English](README.md) | [中文](README.zh.md)

# MultiTrace

**Follow an investigation from scattered evidence to a decision a human can review.**

MultiTrace is an interactive browser prototype for an AI-assisted investigation workflow, developed for the **2026 Deloitte Digital Camp**. It makes a proposed seven-agent architecture explorable through a case walkthrough, evidence graph and investigation console.

[Open the interactive demo](https://yil337.github.io/multitrace-demo/) · [Developer profile](https://github.com/yil337)

**Demo scope:** this repository runs a frontend simulation with sample data and scripted agent activity. It does not run live LLM agents or connect to enterprise systems. Timings, confidence values and case outcomes shown in the demo are illustrative, not measured production results.

## Explore the workflow

- **Twelve investigation steps.** Move from case intake and evidence preparation through cross-source analysis, hypothesis review and final reporting.
- **Seven agent roles.** Inspect the proposed responsibilities of orchestration, document intelligence, entity graphs, statistics, behavior analysis, hypothesis testing and reporting.
- **Evidence you can navigate.** Explore relationships in the interactive graph, inspect supporting records and follow references back through the example case.
- **Human review points.** The interface shows where an investigator authorizes work, reviews a hypothesis or approves a handoff.

The prototype explores a practical question: when multiple AI components contribute to an investigation, how can a person see what happened and decide whether to trust the next step?

## What is implemented here

| Implemented in the browser | Presented as system design |
| --- | --- |
| Navigable case views and investigation console | Agent orchestration and durable backend state |
| Scripted progress, logs and review interactions | Live LLM inference and enterprise connectors |
| Interactive vis-network evidence graph | Production evidence ingestion and verification |
| Sample reports and explanatory architecture panels | Deployment, compliance and performance guarantees |

The frontend uses **HTML, CSS and JavaScript**, with **vis-network** for graph visualization. The interaction logic and sample case are in `index.html`; `pdf.html` contains the companion document view.

## Run locally

With Python 3 installed:

```bash
git clone https://github.com/yil337/multitrace-demo.git
cd multitrace-demo
python3 -m http.server 8000
```

Open **http://localhost:8000**, then choose the investigation workbench or example case. An internet connection is needed to load the graph library from its CDN. No API key is required for the simulation.

The demo is primarily in Chinese. This README provides an English overview for visitors reviewing the project's design and implementation.
