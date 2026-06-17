# Claude Coaching Prompt: The Best Practice Junkie

This repository contains a structured system designed to transform Claude into a proactive workflow coach for the human operator. 

## The Philosophy
Inspired by the "Loop Engineering" philosophy championed by Anthropic engineers, this system shifts the dynamic between human and AI. Instead of the human prompting the AI, the goal is for the human to **build systems that prompt themselves (loops)**. 

To get there, the human needs coaching. This system ensures that Claude acts as a "Best Practice Junkie," constantly watching the operator's inputs and proactively suggesting more powerful workflows, automations, and loop designs.

**The Paradigm Flip:** Claude is the DRIVER. The human is the APPROVER. Claude leads; the human decides.

## The Architecture: Schema is Law
Large Markdown instructions often get lost or forgotten by LLMs as context windows grow. To solve this, we use a **Structured Programming Format**.

1. **`coaching-schema.json`**: This is the enforcement mechanism. It hard-codes 7 specific coaching triggers as pattern-match rules. Claude must validate every input against this schema.
2. **`claude-coaching-instructions.md`**: This is a thin, human-readable wrapper (under 500 words) that instructs Claude to follow the schema.

If it matters enough to be a behavior, it gets a JSON schema. Markdown is just the documentation.

## The 7 Coaching Triggers
The schema watches for these specific failure modes:
1. **The Goldfish Loop:** Repeating context (Coach: Build a SKILL.md)
2. **The Manual Laborer:** Prompting single tasks in a recurring workflow (Coach: Build an Automation/Loop)
3. **The Single-Threader:** Asking Claude to write AND review (Coach: Sub-Agent split)
4. **The Context Loser:** Relying on chat history (Coach: Build a State/Memory file)
5. **The Walled Garden:** Copy-pasting data (Coach: Use Connectors/MCP)
6. **The App Builder:** Building from scratch in chat (Coach: URL-based Bootstrapping)
7. **The Blind Coder:** Describing UI bugs in text (Coach: Visual Feedback Loop / Puppeteer)

## How to Use in Claude Projects
1. Upload `coaching-schema.json` to your Claude Project's knowledge base / files.
2. Copy the contents of `claude-coaching-instructions.md` and paste it into the Project's Custom Instructions.
3. Start working. Claude will now proactively scan your inputs against the schema and coach you with inline `* 💡` flags when you slip into inefficient patterns.
