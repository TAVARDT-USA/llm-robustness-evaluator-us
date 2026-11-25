# LLM Robustness Evaluator & Guardrails Stress Tester

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-5b3cf5.svg)](https://tavardt-usa.github.io/llm-robustness-evaluator-us/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

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

## Useful Links

* **Corporate Portal:** https://ag.tavardt.com/
* **Diagnostic Suite:** https://tools.tavardt.com/
* **Technical Contact:** https://ag.tavardt.com/contact/

***

### License
Released under the MIT License. See [LICENSE](LICENSE) for full details.

***

© 2026 TAVARDT. All rights reserved.
