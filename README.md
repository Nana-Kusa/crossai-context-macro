# Denbun Macro

Japanese version available: [README.ja.md](./README.ja.md)

## Overview
**Denbun Macro** is a format for recording discussion histories in a structure that is readable by both humans and AIs.  
It aims to enable the sharing and continuation of context and history across multiple AIs, such as ChatGPT, Gemini, and Claude.  
Currently, this method works reliably only on ChatGPT-4 Turbo and higher versions, which are available to ChatGPT Plus subscribers.

## Purpose
- Share and reuse discussion context across different AIs
- Facilitate fact-checking and multi-perspective comparison
- Evaluate and enhance the context understanding capability of large language models (LLMs)
- Serve as a manual backup when a thread is interrupted  
  For ChatGPT: if you register a Denbun Macro in memory, you can easily back up the conversation with the prompt: "Save the conversation so far as a Denbun Macro."
- Users can store versioned backups of Denbun Macros, making it easy to resume discussions from any past point  
  Since Denbun Macros are simple text, backup is easy and, even if an AI hallucinates, restoration is possible
- Between ChatGPT threads, you can move context across threads and even across different ChatGPT versions

## Directory Structure
- `format_spec/` : Templates in Markdown / JSON / YAML
- `examples/` : Real-world Denbun Macro examples
- `LICENSE` : License info (MIT)

## How to Start Using Denbun Macro in ChatGPT
At the beginning of a new thread, enter the following structure to define Denbun Macros for ChatGPT (nested layers are supported):

~~~markdown
#Denbun_LABEL:{
  SectionName:{
    Point1=Content;
    Point2=Content;
  };
}
~~~

You **must** input this at the start of a new thread.  
ChatGPT refers to such threads as “definition threads”.

### ⚠️ Differences in Usage Across AIs
📘 For detailed usage in ChatGPT and Gemini:  
→ [docs/usage.md](./docs/usage.md)

- **ChatGPT (GPT-4)**
  - Paste the Denbun Macro at the start or into memory
  - Optionally, instruct "Please save this Denbun Macro into memory"

- **Gemini (tested with 2.5 Flash)**
  - The fastest method is to register the Denbun Macro in “Information you requested Gemini to save” under “Settings & Help.”
  - For details, refer to the above link.

Example of use:  
[Gemini Output Example (Shared Link)](https://g.co/gemini/share/ce95067b8c52)

## Who Can Use Denbun Macro?

Anyone using ChatGPT (especially GPT-4 Turbo) can use Denbun Macro by pasting it into prompts.

If you’ve already registered the Denbun Macro definition in ChatGPT memory, you can prompt like this to summarize the conversation:

~~~markdown
Summarize this thread as a Denbun Macro.
~~~

It’s that simple!

For backup purposes, just copy the outputted Denbun Macro to a text editor and continue your interaction as usual.

If ChatGPT hallucinates and the thread becomes unusable, start a new thread, paste the backed-up Denbun Macro, and prompt “I want to continue this topic,” and the conversation can resume from where it left off.  
To check ChatGPT’s understanding, prompt, “Show me what you understand from this Denbun Macro.”  

You can also paste this data structure (Denbun Macro) into other threads with prompts like:

- "Continue this Denbun Macro"
- "Extract only the main points"
- "Organize another topic in this structure"

Once you’ve defined the Denbun Macro, you can always back up a thread by prompting "Save this thread as a Denbun Macro."  
[Example 1: AGI discussion Denbun Macro](./examples/AGI_discussion.md)  
[Example 2: CAN Invader defense discussion Denbun Macro](./examples/canbus_security.ja.md)  
[Example 3: Comparing answers from ChatGPT, Gemini, and Claude (Fact Check Example)](./examples/factcheck_example.ja.md)  

Even if a thread is interrupted due to hallucination or other issues, as long as you save the Macro, you can reproduce the discussion in a new thread.

### Creating Parent-Child Thread Structure is Simple

1. In the parent thread, focus only on the main topic.
2. When a subtopic arises, request a Denbun Macro summarizing the discussion so far.
3. In the child thread, start by pasting the Denbun Macro and continue the discussion.
4. When finished, generate a Denbun Macro summarizing the child thread and paste it back into the parent thread.

This allows you to clearly connect parent and child threads using Denbun Macros.

- You can create as many child threads as needed.
- Grandchild and further nested threads are also possible.

## Future Goal: Compatibility with Other AIs
In the future, the goal is for Denbun Macros to enable resuming past threads and inheriting context simply by pasting them at the start of prompts on Gemini, Claude, and other AI chatbots.  
If realized, this will make cross-AI discussion and fact-checking much easier.

## 🚀 Progress in Cross-AI Support

As of May 2025, **Gemini 2.5 Flash** has been confirmed to correctly interpret and utilize Denbun Macros. Verified abilities include:

- Accurate parsing of Denbun Macro structure
- Summarizing content for human readers
- Providing step-by-step roadmaps aligned with discussion points

Example Denbun Macro used:  
📄 [examples/AGI_discussion.md](./examples/AGI_discussion.md)

Check actual Gemini output here:  
🌐 [Gemini 2.5 Flash Output Example (Shared Link)](https://g.co/gemini/share/ce95067b8c52)

This confirms the **CrossAI** concept works in practice.

🧠 Further testing in May 2025 showed that Gemini 2.5 Flash can read and write Denbun Macros to its internal memory, enabling structured discussions to resume across sessions.

⚠ Note: Gemini sometimes replies "Saved," but this may not always mean truly persistent memory across sessions.
For certainty, register Denbun Macros in “Information you requested Gemini to save” under "Settings & Help." (Added May 15, 2025)

## Contribution & License
This project is free to use, modify, and redistribute.  
License: MIT License
