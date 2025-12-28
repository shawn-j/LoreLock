# LoreLock

**The AI DM assistant that actually remembers your campaign.**

---

## What Is This?

LoreLock is a memory system for AI-assisted D&D campaigns. It gives Claude (or other LLMs) persistent, structured memory so it can:

- Remember every NPC, location, and plot thread across sessions
- Catch contradictions before your players do
- Separate DM secrets from player knowledge
- Track session history so you can answer "wait, when did that happen?"

No more re-explaining your world every conversation. No more AI forgetting the dragon is already dead.

---

## How It Works

LoreLock uses a structured Campaign Registry (JSON) plus a System Prompt that teaches the AI how to use it. The architecture includes:

- **Versioned memory** - Everything is tracked and timestamped
- **Token Walls** - Conceptual barriers (Castle Walls for core rules, Picket Fences for strategy, Hedges for working data)
- **Contradiction detection** - AI checks new info against established canon
- **Knowledge partitioning** - DM-only secrets stay separate from player knowledge

When you tell it something that conflicts with established lore, it flags it:

```
⚠️ CONTINUITY CHECK
New Info: The party killed the Drowned Priestess in Session 8
Conflicts With: She's marked as "not yet encountered" and Session 13 is her planned first appearance
Options:
1. Keep original canon
2. Retcon to new version  
3. Explain in-world
Your call, DM.
```

---

## Quick Start

1. **Get Claude Pro** ($20/month) - Required for Projects feature
2. **Create a new Claude Project** - Name it after your campaign
3. **Add the System Prompt** - Copy `DM_SYSTEM_PROMPT.md` into Project Instructions
4. **Upload your Campaign Registry** - Start with `CAMPAIGN_REGISTRY_TEMPLATE.json`, fill in your campaign details
5. **Start chatting** - Ask "What do you know about my campaign?"

Full setup instructions in [QUICK_START_GUIDE.md](QUICK_START_GUIDE.md)

---

## Files

| File | Purpose |
|------|---------|
| `DM_SYSTEM_PROMPT.md` | The instructions that make Claude act as LoreLock |
| `CAMPAIGN_REGISTRY_TEMPLATE.json` | Blank template - fill in for your campaign |
| `SESSION_LOG_TEMPLATE.json` | Template for logging individual sessions |
| `EXAMPLE_CAMPAIGN_REGISTRY.json` | Filled-in example ("The Shattered Crown" campaign) |
| `QUICK_START_GUIDE.md` | Detailed setup and usage instructions |

---

## Example

Using the included example campaign:

**You:** "What do the players know about Duke Varen versus what I know as DM?"

**LoreLock:**
```
🎭 PLAYER KNOWLEDGE
- Duke Varen is connected to the Obsidian Hand cult
- His signet ring was found on a dead cultist (Session 7)
- That's all they've confirmed.

🔒 DM-ONLY KNOWLEDGE
- Varen is high-ranking in the cult
- He doesn't know "The Voice" is the Tyrant King's spirit
- He framed Theron's brother Marcus, who is alive and imprisoned
- Red Marta (Thornwood bandits) works for him
```

---

## Current Status

**Beta** - Looking for DMs running active campaigns to test this and give feedback.

This is a solo project. I built it to solve my own frustrations with AI forgetting campaign details. If it's useful to others, I'll keep improving it.

---

## Feedback

Found a bug? Have a suggestion? Want to share how it's working for you?

Open an issue or reach out.

---

## License

Free to use for personal campaigns. Please don't resell or redistribute as your own product.

---

*Your world deserves to be remembered.*
