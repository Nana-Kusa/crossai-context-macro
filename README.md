# crossai-context-macro  

Japanese version available: [README.ja.md](./README.ja.md)


## Overview
**crossai-context-macro** is a structured discussion-log format called *Denbun Macro*, designed to be readable by both humans and AI.  
This project aims to enable shared context and continuity across multiple AI systems such as ChatGPT, Gemini, and Claude.

## Purpose
- Share and reuse discussion context across different AI platforms
- Facilitate fact-checking and multi-perspective comparison
- Evaluate and enhance the contextual understanding capabilities of large language models (LLMs)
- Acts as a manual backup in case a conversation thread is interrupted
- Users can maintain versioned backups and roll back to any previous point in the discussion
- Enables context transfer between different ChatGPT threads or even across ChatGPT versions

## Directory Structure
- `format_spec/` : Format templates in Markdown, JSON, and YAML
- `examples/` : Real-world examples of Denbun Macros used in AI conversations
- `LICENSE` : License information (MIT)

## How to Use with ChatGPT
Copy and paste the following format into your ChatGPT prompt:
~~~
Please continue the discussion based on the following Denbun Macro:

#Denbun_Label:{
  SectionName:{
    Topic1=Content;
    Topic2=Content;
  };
}
~~~

## Can Anyone Use Denbun Macro?

Yes! Anyone using ChatGPT (especially GPT-4 or GPT-4 Turbo) can use the Denbun Macro format in their prompts.

Just paste a macro like this at the beginning or end of your prompt:

~~~
#Denbun_Label:{
  SectionName:{
    Topic1=Content;
    Topic2=Content;
  };
}
~~~

And follow it with a request like:

- "Please continue this thread"
- "Summarize this macro"
- "Extract key points from this"  
 [exsample: AGI and Existential Risks](.examples/AGI_discussion.md)  

Even if the conversation thread has ended, you can restart it by pasting a saved Denbun Macro in a new session.

Note: GPT-3.5 may not understand complex macros well. GPT-4 is recommended.

## Future Goal: Cross-AI Compatibility
We aim to make this format usable across various AI platforms.  
By placing Denbun Macros at the beginning of prompts, we hope to achieve consistent context reproduction and smoother dialogue continuity in systems like Gemini and Claude.

## Contribution & License
This project is open for use, modification, and redistribution.  
License: MIT License  

## What is Denbun Macro?  
📝 Denbun Macro (伝文マクロ) is a Japanese term that roughly means "structured thread summary".
It refers to a human-readable and AI-interpretable format designed to preserve conversation context across AI systems.

If you're an English speaker, you may think of it as a **Structured Context Macro**.  

Denbun macros are typically written in Markdown-like syntax,  
but can also be represented in JSON or YAML for structured use across tools.





