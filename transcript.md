# X/Twitter Post Transcript: MIKE on "Loops vs. Prompts"

**Source Information**
- **Author:** MIKE (@mikenevermiss)
- **Date:** June 16, 2026 (6:27 AM)
- **Platform:** X / Twitter
- **Original URL:** https://x.com/mikenevermiss/status/2066769708641042571
- **Views:** 371K Views
- **Linked Article:** "How to Create Loops with Claude" (published June 15, 2026)

---

### Post Content

Anthropic engineer: "you're not supposed to prompt Claude. you're supposed to build a system that prompts itself [loops]." 

this is one of the best workflows I've seen in a long time 

in this video he breaks down exactly how most people are building loops wrong: 
- the memory so every loop starts from zero 
- the sub-agents that 95% of builders have never split apart 
- the stop condition setup that keeps loops from running forever and billing you in your sleep 
- why writing one prompt a day is the slowest way to use Claude 

if you've been using Claude for more than a month and still typing every task by hand, you've been running one prompt when you could be running a system of loops 

instead of another prompt tonight, watch this 

make sure to bookmark it before it gets buried 

full guide in the article below

*[Video attached: 26 minutes 23 seconds, showing a presentation by Boris Cherny (Head of Claude Code at Anthropic)]*

---

### Context & Supporting Quotes (from Linked/Referenced Material)
The post references the concept of "Loop Engineering," championed by Boris Cherny (Head of Claude Code at Anthropic). 

Key insights from the broader discussion:
> "You shouldn't be prompting coding agents anymore. You should be designing loops that prompt your agents." — Peter Steinberger

> "I don't prompt Claude anymore. I have loops running that prompt Claude and figuring out what to do. My job is to write loops." — Boris Cherny, Head of Claude Code at Anthropic

Loop engineering replaces the human as the one who prompts the agent. Instead, the human designs the system (the loop) that prompts the agent. A loop is a recursive goal where a purpose is defined, and the AI iterates until complete.

The five pieces of a loop:
1. **Automations** that go off on a schedule and do discovery and triage by themselves.
2. **Worktrees** so two agents working in parallel don't step on each other.
3. **Skills** to write down the project knowledge the agent would otherwise just guess.
4. **Plugins and connectors** to plug the agent into the tools you already use.
5. **Sub-agents** so one of them has the idea and a different one checks it.
6. Plus **State/Memory** to track what's done.
