# 🔀 Denbun Macro Compatibility Across AI Models

This document summarizes the observed behavior of different AI models when interacting with Denbun Macros. Tests were conducted in April–May 2025.

## 🧠 Models Evaluated

| AI Model         | Version         | Memory | Macro Parsing | Notes |
|------------------|-----------------|--------|----------------|-------|
| ChatGPT          | GPT-4 Turbo     | ✅ Yes (if enabled) | ✅ Excellent | Supports memory persistence. Recommended to paste macro at the beginning and ask: "Please remember this macro." |
| Gemini           | 2.5 Flash       | ❌ No    | ✅ Excellent | Surprisingly retains macro structure across turns. May not require redefinition if macro name is reused and intent is clear. |

---

## 📌 Key Findings

### ✅ ChatGPT
- GPT-4 Turbo with memory enabled can remember Denbun Macros across threads.
- Best used by pasting macro at the start and prompting:  
  `"Please remember this macro for ongoing context."`

### ✅ Gemini 2.5 Flash
- Does not offer persistent memory.
- Still able to:
  - Recognize previously defined macro structures
  - Resume discussions based on macro name and user intent
- Displays behavior suggesting implicit short-term memory or structural recognition

> 🧪 This was verified using [examples/AGI_discussion.ja.md](../examples/AGI_discussion.ja.md) and [Gemini public result](https://g.co/gemini/share/ce95067b8c52)

---

## 📝 Recommendations

| Use Case | ChatGPT | Gemini |
|----------|---------|--------|
| Long threads | ✅ Excellent | 🔸 Partial support (macro reuse needed) |
| Reusability | ✅ Memory-based | 🔸 Structure-based |
| Minimal prompts | ✅ One-time macro | ❌ Must re-paste or reference macro name |
| High-precision parsing | ✅ | ✅ |

---

Last updated: **2025-05-04**
