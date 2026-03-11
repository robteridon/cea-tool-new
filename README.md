# GiveWell-Style Cost-Effectiveness Analysis Tool

A web-based tool for conducting rigorous cost-effectiveness analyses (CEAs) following GiveWell's methodology. Built by IDinsight, it uses a multi-agent AI pipeline to evaluate development interventions and produce quantitative results with policy-relevant narratives.

## What It Does

You describe an intervention (e.g. a malaria bednet program, a deworming initiative), and the tool runs an automated pipeline that:

1. **Scopes the intervention** - Conversational AI asks clarifying questions about the program, target population, delivery context, and outcome pathways
2. **Researches the evidence** - Finds and extracts key parameters from academic literature (effect sizes, baseline rates, costs, duration)
3. **Evaluates study quality** - Assesses internal validity of key studies using GiveWell's framework (randomization, identification strategy, causal inference)
4. **Estimates counterfactuals** - Models what would happen without the intervention (displacement, substitution effects)
5. **Calculates cost-effectiveness** - Produces a full CEA with three scenarios (low, base, high), sensitivity analysis, and a cost-effectiveness multiple benchmarked against GiveWell's 8x threshold

Results are displayed in an interactive dashboard with summary cards, parameter tables, sensitivity charts, and a narrative brief.

## How to Use It

1. Open `index.html` in a modern browser
2. Enter your Anthropic Claude API key in the sidebar
3. Describe the intervention you want to analyze
4. Answer the scoping questions
5. Wait for the pipeline to complete (~2-5 minutes)
6. Review results in the dashboard
7. Export to Excel or Word

No build step, no dependencies to install. It's a single HTML file that makes direct API calls to Claude.

## Features

- **Multi-agent pipeline** - Six specialized AI agents handle different stages of the analysis
- **Three-scenario modeling** - Low, base, and high estimates for all parameters
- **Sensitivity analysis** - Interactive chart showing which parameters drive uncertainty
- **GBD disability weight lookup** - Search 2,256 Global Burden of Disease entries for health outcome mapping
- **Excel export** - Professional workbooks with color-coded scenarios, categorized parameters, and proper formatting
- **Word export** - Formatted documents with tables and narrative sections
- **Streaming responses** - Real-time text display with thinking indicators

## Tech Stack

- **Frontend:** Vanilla HTML/CSS/JavaScript (single-file architecture)
- **AI:** Anthropic Claude API (streaming, multi-turn)
- **Charts:** Chart.js
- **Excel:** ExcelJS
- **Word:** DOCX.js
- **Data:** Embedded GBD disability weights database

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection
- Anthropic Claude API key
