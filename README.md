# Denbun Macro

Japanese version available: [README.ja.md](./README.ja.md)

## Introduction

This project explores prompt engineering using structured data formats optimized for AI interaction. It currently focuses on applying the "Denbun Macro"—a structured prompt format originated from ChatGPT—to other AI systems.

The long-term goal is to establish a cross-AI compatible structured prompt format that can be reused across multiple platforms.

## Usage

For usage instructions, see the following files:

* [EN : usage.md](https://github.com/Nana-Kusa/crossai-context-macro/blob/main/docs/usage.md)
* [JA : usage.ja.md](https://github.com/Nana-Kusa/crossai-context-macro/blob/main/docs/usage.ja.md)

## Why Structure Prompts as Data?

This is one of the most important questions in this project. We asked three different AI systems—ChatGPT 4o, Gemini 2.5 Flash, and Claude 4—to explain the benefits of structured prompts. Each AI offers a unique perspective on the topic.

### ChatGPT 4o's Perspective

Structuring prompts into data formats offers the following clear advantages. It’s not just about formatting—it fundamentally changes the quality of interaction between humans and AI.

* **Improved Processing Efficiency**
  Natural language requires significant computational resources to resolve ambiguity and interpret context. Structured data conveys meaning explicitly, allowing faster parsing by AI.

* **Better Consistency and Accuracy**
  Structured input specifies key parameters and constraints, leading to more predictable and intended outputs while reducing variance and misinterpretations.

* **Reusability and Versatility**
  A structured prompt (like Denbun Macro) can be reused across different AI systems. This enables better information sharing and task coordination in cross-AI environments.

* **Ease of Debugging and Validation**
  Because prompts are sectioned, it’s easier to trace which parts influence the response, making iterative improvements more manageable.

* **Foundation for Multimodal AI**
  In contexts involving text, images, or audio, structured meaning becomes even more critical. Structured prompts enhance compatibility with future multimodal AI systems.

In short, a structured prompt serves as a reliable "interface" for AI interaction, yielding more controllable performance than natural language alone.

### Gemini 2.5 Flash's Perspective

The primary reason for structuring prompts is to make communication with AI more efficient, accurate, and consistent.

AI tries to understand the natural language that humans use daily, but natural language is inherently ambiguous and polysemous. For example, the word “big” could refer to size, importance, or age depending on context. While humans interpret this easily, AI may misinterpret such expressions, leading to degraded performance.

Structured data solves this by labeling and formalizing meanings and relationships. This allows AI to instantly recognize the role and intent of each element, freeing up resources for better output generation.

Key benefits include:

* **Improved Response Accuracy**
  Better understanding of user intent leads to higher-quality answers.

* **Increased Consistency**
  AI tends to generate more predictable responses using consistent logic.

* **Faster Processing**
  Parsing time is reduced, resulting in smoother interactions.

* **Prompt Management and Reusability**
  Structured prompts can be templatized and modularized. This enhances organization and makes them suitable for large-scale or multi-purpose scenarios.

* **AI Model Portability**
  Clearly structured prompts improve cross-compatibility. This opens the path for platform-agnostic prompt design in cross-AI research and applications.

In summary, structured prompts maximize AI potential and form a foundational approach for human–AI collaboration.

### Claude 4's Perspective

* **Fundamental Efficiency Gains**
  AI models are designed to process tokenized, structured information. Natural language requires an additional interpretive layer, which structured prompts eliminate.

* **Precision and Consistency**
  Natural language carries inherent ambiguity. For instance, “a big red car” can be interpreted in various ways. Structured data defines each element clearly for consistent interpretation.

* **Scalability and Maintainability**
  Complex tasks quickly become unmanageable with natural language prompts. Structured data enables localized updates and better global predictability. Templates and automation are also easier.

* **Alignment with Cognitive Architecture**
  Transformer-based models, such as those widely used today, utilize attention mechanisms that are optimized for structured relationships. Hierarchical prompt structures align well with these mechanisms.

* **Ease of Debugging and Optimization**
  Structured prompts make it easier to isolate what affects outputs and allow systematic A/B testing and iterative tuning.

* **Cross-Platform Compatibility**
  Structured prompts improve portability across AI systems. Transformation rules can preserve logical structure while optimizing per model.

## Contribution & License

This project is open for use, modification, and redistribution under the following license:

**License: MIT License**
