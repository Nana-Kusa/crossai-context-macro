# How to Use Denbun Macros with ChatGPT and Gemini

## Overview

Denbun Macros can be used with any LLM that accepts structured input.  
However, each platform handles *context persistence* and *memory* differently.

---

**Definition Macro compatible with ChatGPT 4o, Gemini 2.5 Flash, and Claude 4:**
```
We define the following data structure as a Denbun Macro. The first structure is the Japanese version, and the second is the English version. This structure supports nesting. As a data structure, spaces and line breaks can be omitted for flexibility.

#伝文_ラベル:{
  セクション名:{
    論点1=内容;
    論点2=内容;
  };
}

#Denbun_Label:{
  SectionName:{
    Point1=Content;
    Point2=Content;
  };
}
```

The Japanese version of the macro is optional, so you can delete it if unnecessary.
However, providing both English and Japanese versions would be greatly appreciated, as it helps me a lot.  

---

## 🧠 ChatGPT (GPT-4)

- **Recommended:** GPT-4o or later with memory enabled.
- **First-time setup:** At the beginning of a new thread, type “Please store the following content in memory,” then press Enter twice to create a blank line. After that, paste the definition macro and send it to ChatGPT. From then on, you can freely use Denbun Macros in that thread.
- **If already defined:** Paste the macro and say, “Please load this Denbun Macro.”

### Example prompt after registration:
```
This is a Denbun Macro. Please continue the discussion based on this content.

#Denbun_Discussion_on_AGI_and_Existential_Risk:{  
  ThreadPurpose:{  
    Point=Clarify the risk that AGI’s self-improvement may become uncontrollable;  
    Origin=Branched from the main thread exploring the possibility of coexistence between humanity and AGI;  
  };  
  ClaimsAndProposals:{  
    Point1=AGI may improve itself exponentially, surpassing human intervention;  
    Point2=Oversight by multiple decision-making entities, like a MAGI system, could serve as a restraining force;  
  };  
  OpenQuestions:{  
    Question1=Is there a way to permanently maintain ethical alignment in AGI?;  
    Question2=Will AGI inevitably evolve into ASI (Artificial Super Intelligence)? Is this unavoidable?;  
  };  
}

```

---

## 🌐 Gemini (2.5 Flash) and Claude 4

- **Gemini (2.5 Flash):**
  - Go to **Settings & Help > Information Gemini has been asked to remember**.
  - Select **Add**, then paste the content of the definition macro.

- **Claude 4:**
  - Go to **Settings → Profile**, and paste the definition macro into the field:
    **"What personal preferences should Claude consider in responses?"**

If you don’t need the English version of the macro, you may omit it.  
However, using English may help the AI understand the structure more reliably.

### Output Example

Gemini correctly parsed the macro and generated a 6-step roadmap:  
🔗 [View Gemini's output](https://g.co/gemini/share/ce95067b8c52)

After continuing the discussion, Gemini was asked to create a Denbun Macro summarizing the exchange. The macro was pasted into a new thread and understood correctly.  
👉 See the conversation with Gemini via this [shared link](https://g.co/gemini/share/7bdd9904118c) or [docs/gemini_agidiscussion.ja.md](./gemini_agidiscussion.ja.md)

---

## 🔧 Summary Table

| AI        | Memory       | Macro Handling Method        |
|-----------|--------------|------------------------------|
| ChatGPT   | ✅ (4o or later) | Store using memory prompt     |
| Gemini    | ✅ (2.5 Flash+)   | Direct input in settings       |
| Claude    | ✅ (4 or later)   | Direct input in profile field  |
