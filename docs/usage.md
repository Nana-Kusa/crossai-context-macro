# Using Denbun Macros with ChatGPT and Gemini

## Overview

Denbun Macros can be used with any LLM that accepts structured input.
However, some platforms behave differently in how they retain context or
handle memory.

---

## 🧠 ChatGPT (GPT-4)

- Recommended: GPT-4 Turbo with memory enabled
- Paste the macro at the start of the conversation
- Prompt: “Please remember this macro” or “Use this macro to continue”

### Example Prompt

This is the macro for context. Please continue the discussion.

#Denbun_AGI_Risk:{
Context:{
  Threat=Existential risk of AGI;
  Control=Methods for safe alignment;
};
}

---

## 🌐 Gemini (2.5 Flash)

- Does **not retain memory** between prompts
- You must **paste the macro every time**
- Step 1: Paste macro
- Step 2: Prompt: “Please read and continue this macro”

### Example Output

Gemini successfully analyzed this macro and generated a 6-step roadmap:  
🔗 [View result](https://g.co/gemini/share/ce95067b8c52)

---

## 🔧 Summary Table

| AI       | Memory     | Macro Handling         | Notes                    |
|----------|------------|------------------------|--------------------------|
| ChatGPT  | ✅ (enabled) | Can remember macro     | GPT-4 recommended        |
| Gemini   | ❌          | Must re-paste each time| Handles structure well   |
