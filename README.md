# crossai-context-macro  

Japanese version available: [README.ja.md](./README.ja.md)


## Overview
`crossai-context-macro` is an open-source format and methodology for managing structured conversation memory across multiple AI systems.

It uses a concept called a **Denbun Macro**, a human-readable, AI-interpretable block of structured text that summarizes a thread and enables:
- Context preservation across sessions and platforms
- Fact-checking across multiple AIs
- Restarting stopped threads using backups
- Thread branching, nesting, and resuming discussions at any point

---

## 🧠 Purpose

Many AI models (e.g., Gemini, Claude, Perplexity) do not retain memory. Even in ChatGPT, conversations are bound to single threads unless memory is explicitly referenced. Denbun Macro solves this by making the context **portable**.

---

## ✅ Benefits

- Structure thread content explicitly
- Switch between AI platforms while preserving context
- Perform fact-checking by comparing macro interpretations
- Rewind discussions from previous points if they go off-track

---

## 🧰 How to Use with ChatGPT

Paste a macro like this into your prompt:

~~~
#Denbun_Label:{
Section:{
  Topic1=Summary;
  Topic2=Details;
};
}
~~~

And follow it with:

- "Please continue this thread"
- "Summarize the macro"
- "Analyze and expand on each section"

---

## 🌱 Can Anyone Use Denbun Macro?

Yes. Anyone using ChatGPT (especially GPT-4) can use Denbun Macro formatting.  

When you want to save a ChatGPT conversation using Denbun Macro for the first time, use the following prompt:  
~~~
We define the following data structure as "Denbun Macro." Using this Denbun Macro, please summarize the content of this thread in the Denbun Macro format.

#Denbun_Label:{
  Section:{
    Topic1=Summary;
    Topic2=Details;
  };
}
~~~  
Even if a thread ends or resets, pasting the saved macro will restore it.

Note: GPT-3.5 may struggle with complex structures. GPT-4 is recommended.

---

## 🧬 Thread Tree Structure

You can build parent-child thread structures easily using Denbun Macros.

1. Keep the main topic in the parent thread.
2. Save a Denbun Macro in the parent thread when you want to branch out.
3. Start a new thread with the macro — this becomes the child thread.
4. When the child finishes, create a macro summarizing it and paste it back into the parent.

You can make:
- Multiple child threads
- Grandchild threads
- Great-grandchild threads, and more

---

## 📂 Example

- [Example: AGI and Existential Risks](./examples/AGI_discussion.md)

---

## 📖 Glossary

| Term | Meaning |
|------|---------|
| Denbun | Short for "Denbun Macro", a structured context memory format |
| Macro | A reusable block of instruction or context |
| CrossAI | Using multiple AIs in one workflow |

---

## 🔓 License

MIT License (See LICENSE file)

---

## 🤝 Contribution

Issues and PRs welcome! See:
- [Code of Conduct](./CODE_OF_CONDUCT.md)
- [Contributing Guide](./CONTRIBUTING.md)
