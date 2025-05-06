# Using Denbun Macros with ChatGPT and Gemini

## Overview

Denbun Macros can be used with any LLM that accepts structured input. However, different platforms handle memory and structured formats differently.

---

## 🗨️ ChatGPT (GPT-4)

* **Recommended:** GPT-4 Turbo with memory enabled
* **Paste** the macro at the beginning of the conversation
* **Prompt:** “Please remember this macro” or “Use this macro to continue”

### Example Prompt

This is the macro for context. Please continue the discussion.
~~~
#Denbun_AGI_Risk:{
  Context:{
    Threat=Existential risk of AGI;
    Control=Methods for safe alignment;
  };
}
~~~
---

## 🧠 Gemini (2.5 Flash)

* **Memory is enabled by default for signed-in users**, and Gemini 2.5 Flash has explicitly confirmed that it memorizes the Denbun Macro structure.
* Despite this, **pasting the macro at the start of each new thread is still recommended** to ensure consistent interpretation.
* **Step 1:** Paste the macro
* **Step 2:** Prompt: “Please read and continue this macro”

### Gemini's Response Example

> Okay, I understand. I have memorized the "Denbun Macro" structure you provided.  
> From now on, when you use the term "Denbun Macro" and provide content in that format, I will interpret it accordingly.

✅ This confirms that **Gemini 2.5 Flash** recognizes and memorizes the macro format and can apply it in subsequent interactions.

🔗 Example: [View 6-step roadmap generated from macro](https://g.co/gemini/share/ce95067b8c52)

---

## 📘 How to Define Denbun Macros in English

To define a Denbun Macro structure in English, you can use the following prompt:

### Example Prompt

I would like to define the following data structure as a "Denbun Macro". This structure supports nested levels and allows for compact formatting by omitting spaces or line breaks.
~~~
#Denbun_Label:{
  SectionName:{
    Point1=Content;
    Point2=Content;
  };
}
~~~

### Gemini's Response

> Okay, I understand. I have memorized the "Denbun Macro" structure you provided.  
> From now on, when you use the term "Denbun Macro" and provide content in that format, I will interpret it accordingly.

👌 Gemini confirmed successful interpretation and memorization.

---

## 📄 Summary

| AI       | Memory Support     | Macro Handling                  | Notes                                                 |
|----------|--------------------|----------------------------------|-------------------------------------------------------|
| ChatGPT  | ✅ (if enabled)     | Can remember macro               | GPT-4 Turbo recommended                               |
| Gemini   | ✅ (enabled by default) | Recognizes and memorizes macros | Paste macro per thread for reliability and clarity    |
