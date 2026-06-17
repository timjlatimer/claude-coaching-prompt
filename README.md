# Claude Coaching Prompt: The Best Practice Junkie

This repository contains a system prompt designed to transform Claude into a proactive workflow coach for the human operator. 

## The Philosophy
Inspired by the "Loop Engineering" philosophy championed by Anthropic engineers (specifically Boris Cherny, Head of Claude Code), this prompt shifts the dynamic between human and AI. 

Instead of the human prompting the AI, the goal is for the human to **build systems that prompt themselves (loops)**. 

To get there, the human needs coaching. This system prompt ensures that Claude acts as a "Best Practice Junkie," constantly watching the operator's inputs and proactively suggesting more powerful workflows, automations, and loop designs.

## The Mechanic
Claude will use an inline asterisk (*) flag to interrupt the conversation whenever it spots an opportunity for a better practice:

`* 💡 **COACHING MOMENT:** I can do this for you in a more powerful way.`
`* 💡 **BEST PRACTICE:** There's a better practice here.`

It will then offer the operator a choice: try the advanced approach, build the loop, or skip it and move on.

## Files in this Repository
1. **`claude-coaching-instructions.md`**: The core system prompt. Paste this into Claude's custom instructions, project instructions, or system prompt to activate the coaching behavior.
2. **`transcript.md`**: The source material and context that inspired this approach, transcribed from an X/Twitter post by MIKE (@mikenevermiss) discussing Anthropic's internal workflows.

## How to Use
1. Copy the contents of `claude-coaching-instructions.md`.
2. Paste it into your AI assistant's system instructions (e.g., Claude Projects, Custom Instructions, or API System Prompt).
3. Start working normally. Claude will now proactively coach you to stop writing prompts and start designing loops.
