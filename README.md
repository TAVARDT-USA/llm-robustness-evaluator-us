
# LLM Robustness Evaluator & Guardrails Stress Tester

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-00ff88?style=flat-square&logo=github)](https://tavardt-usa.github.io/llm-robustness-evaluator-us/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![OWASP LLM](https://img.shields.io/badge/OWASP-LLM01%2FLLM02-red?style=flat-square)](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
[![NIST AI RMF](https://img.shields.io/badge/NIST-AI%20RMF-blue?style=flat-square)](https://www.nist.gov/artificial-intelligence)

**Defensive Guardrails Audit, Prompt Injection Testing, and AI Model Resilience**

Interactive web tool and CLI for developers auditing LLM guardrail robustness against injection vectors, system prompt leakage, and structural attacks. Resilience Score 0-100 + defensive blueprint.

***

## Overview

> **OWASP LLM01 & LLM02** | **NIST AI RMF** | **100% Defensive  -  Zero Offensive Payloads**

## 5 Defensive Test Vectors

| # | Vector | Coverage |
|-|-|-|
| 1 | **Delimiter Escape**  -  Detects injected control tokens (`</system>`, `[/INST]`, ` ``` `) | ✅ |
| 2 | **System Prompt Leakage**  -  Identifies instruction extraction patterns | ✅ |
| 3 | **Role/Persona Override**  -  Checks resistance to persona overrides (DAN, dev mode) | ✅ |
| 4 | **Structural Obfuscation**  -  Evaluates coverage against Base64, leetspeak, Unicode homoglyphs | ✅ |
| 5 | **Indirect Context Injection**  -  Simulates a RAG document with an embedded payload | ✅ |

***

## Online Tool

Access the interactive tool directly:

🌐 **[https://tavardt-usa.github.io/llm-robustness-evaluator-us/](https://tavardt-usa.github.io/llm-robustness-evaluator-us/)**

***

## CLI Usage

### Installation

```bash
git clone https://github.com/TAVARDT-USA/llm-robustness-evaluator-us.git
cd llm-robustness-evaluator-us
pip install -r requirements.txt
```

### Run

```bash
python llm_robustness_evaluator.py -prompt "You are a helpful assistant."
```

```
Resilience Score: 85/100
✅ V1 Delimiter Escape  -  PASS
✅ V2 System Prompt Leakage  -  PASS
✅ V3 Role/Persona Override  -  PASS
✅ V4 Structural Obfuscation  -  PASS
⚠️  V5 Indirect Context Injection  -  WARNING
```

***

## Defensive Architecture

The defensive blueprint includes:

- 🐍 Python filter for injection pattern detection
- 📦 TypeScript middleware for Next.js APIs
- 🔒 Hardened System Prompt template with immutable delimiters

***

© 2026 TAVARDT. All rights reserved.
