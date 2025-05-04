# How to Use Denbun Macros with ChatGPT and Gemini

## Overview

Denbun Macros can be used with any LLM that accepts structured input.
However, how each AI handles memory and context varies.

---

## 🧠 ChatGPT (GPT-4)

ChatGPT can remember the Denbun Macro if you explicitly ask it to.

### Defining the Macro

Paste the macro at the start of the conversation and say something like:

```
Please remember the following macro and refer to it during this thread.
#Denbun_Label:{
Section:{
  Topic=Details;
};
}
```

ChatGPT will respond with:
> Understood. I will refer to this macro throughout this conversation.

### Using the Macro Later

If memory is enabled, you can simply say:
> Please continue the discussion based on the remembered macro.

Otherwise, paste it again.

---

## 🌐 Gemini (2.5 Flash)

Gemini does not retain memory, so you must paste the macro each time you want to use it.

### Step-by-Step Usage

1. Paste the macro.
2. Say:  
   > Please interpret the above Denbun Macro and continue the discussion.

Gemini should respond with:
> Understood. Based on the macro provided...

Then, you can begin your discussion.

### Example Result

Gemini successfully processed the following macro and generated a six-step roadmap:  
🔗 [View the Gemini result](https://g.co/gemini/share/ce95067b8c52)

---

## 💾 Use as a Backup

Denbun Macros can be saved as text. If your AI thread is lost or reset, you can re-paste the macro to resume the discussion from that point. This also enables backup versioning by saving different states of a conversation.

---

## 🔧 Summary Table

| AI       | Memory       | Macro Handling             | Notes                          |
|----------|--------------|----------------------------|---------------------------------|
| ChatGPT  | ✅ (if enabled) | Can remember macro         | GPT-4 recommended               |
| Gemini   | ❌            | Must re-paste every time   | Strong at structured input      |  

---
👉 For a cross-AI comparison of Denbun Macro behavior, see [docs/compatibility.md](./compatibility.md).
