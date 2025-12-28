# LoreLock Quick Start Guide
## Your AI Campaign Memory in 15 Minutes

---

## What Is This?

LoreLock is a Claude Project setup that gives you an AI assistant with **actual persistent memory** for your D&D campaign (or any TTRPG).

Unlike regular ChatGPT or Claude conversations that forget everything, LoreLock:
- ✅ Remembers every NPC, location, and plot point
- ✅ Tracks what happened each session
- ✅ Catches contradictions before your players do
- ✅ Separates DM secrets from player knowledge

---

## Setup (10 minutes)

### Step 1: Create a Claude Project

1. Go to [claude.ai](https://claude.ai)
2. Click **Projects** in the sidebar (requires Claude Pro - $20/month)
3. Click **New Project**
4. Name it: `[Your Campaign Name] - LoreLock`

### Step 2: Add the System Prompt

1. In your new Project, click **Project Instructions**
2. Copy the entire contents of `DM_SYSTEM_PROMPT.md`
3. Paste it into the Project Instructions
4. Save

### Step 3: Upload Your Campaign Registry

1. Open `CAMPAIGN_REGISTRY_TEMPLATE.json`
2. Fill in the basics:
   - Campaign name
   - Player characters (at minimum: names, classes, key traits)
   - Current situation (where are they, what's happening)
   - 3-5 important NPCs they've met
   - Key locations
3. Save it as `CAMPAIGN_REGISTRY.json`
4. In your Claude Project, click **Add Content** → **Upload Files**
5. Upload your filled-in Registry

### Step 4: Test It

Start a new conversation in the Project and say:

> "Hi LoreLock. Let's do a quick check - what do you know about my campaign so far?"

It should summarize what you've uploaded. If it does, you're ready!

---

## Basic Usage

### Before Each Session (5 min prep)

Start a conversation and say:
> "Session prep for Session [#]. We're picking up at [location/situation]. What should I have ready?"

LoreLock will:
- Remind you of active quests and plot threads
- List relevant NPCs for that location
- Flag any dangling threads from last session

### During the Session

If you need to quickly check something:
> "What's the name of the innkeeper in Millbrook?"
> "What did the party learn about the cult last session?"
> "Is it canon that the duke has a daughter?"

### After Each Session (5-10 min)

Say:
> "Log session [#]. Here's what happened: [describe major events]"

Or for a more structured log:
> "Let me log session [#] with the full template"

Then fill in the key sections:
- Who was there
- Major events
- NPC interactions
- Decisions made
- Where we ended

**Important:** After logging, download the updated conversation or copy key additions to your Registry file. Claude Projects maintain context within the project, but having a master file ensures nothing is lost.

---

## Key Commands

| Say This | To Do This |
|----------|------------|
| "Add to canon: [fact]" | Record a new established fact |
| "Is it canon that...?" | Check if something is established |
| "What do we know about [topic]?" | Get all info on a subject |
| "Recap session [#]" | Get a summary of that session |
| "What are our active quests?" | List current objectives |
| "Does [new idea] conflict with anything?" | Contradiction check |
| "Players know: [fact]" | Mark something as player knowledge |
| "Secret: [fact]" | Mark something as DM-only |
| "NPC status check" | List all NPCs and their current status |
| "Plot thread check" | List all open plot threads |

---

## Managing Your Registry

### Option A: Single File (Simpler)
- Keep one `CAMPAIGN_REGISTRY.json` file
- Update it periodically with new information
- Re-upload when starting fresh conversations

### Option B: Registry + Session Logs (Better for Long Campaigns)
- Keep the Registry for stable world info
- Create separate `SESSION_##.json` files for each session
- Upload both Registry + recent session logs for context

### When to Update the Registry

Update your master Registry file when:
- A new major NPC is introduced
- A quest is completed
- A major plot revelation happens
- Every 3-5 sessions (routine maintenance)

---

## Handling Contradictions

When LoreLock detects a potential contradiction, you'll see:

```
⚠️ CONTINUITY CHECK
New Info: [What you just said]
Conflicts With: [Established fact]
Options:
1. Keep original
2. Retcon to new version
3. Explain in-world
```

Your options:
1. **Keep original** - The new thing didn't happen, stick with what was established
2. **Retcon** - Change the canon (LoreLock will note the retcon)
3. **Explain in-world** - Maybe an NPC lied, or there's a magical explanation

---

## Tips for Best Results

### Be Specific When Adding Canon
❌ "There's a tavern in town"
✅ "Add to canon: The Rusty Anchor is a dockside tavern in Millbrook run by a retired sailor named Old Bess"

### Log Sessions Promptly
The sooner you log after a session, the more you'll remember. Even bullet points are better than nothing.

### Use the Knowledge Partition
Marking secrets as DM-only helps when you want to brainstorm player-facing content without accidentally including spoilers.

### Don't Over-Engineer
You don't need to fill every field in every template. Start with the basics and add detail as needed.

---

## Troubleshooting

### "LoreLock forgot something I told it"
- Check if it's in your uploaded Registry file
- If you added it in conversation but not the file, it may not persist to new conversations
- Solution: Add important facts to the Registry file itself

### "The responses are too long/short"
Say: "Please give me [shorter/more detailed] responses for the rest of this conversation"

### "I need to fix something in the canon"
Say: "Retcon needed: [old fact] is now [new fact]. Reason: [why]"

### "I want to start fresh but keep my world"
- Download/save your current Registry
- Start a new conversation in the Project
- Upload the Registry again

---

## What's Next?

After a few sessions using LoreLock:

1. **Does it work?** Is it actually remembering things and catching contradictions?
2. **Is it useful?** Are you saving time and avoiding "wait, didn't we already..." moments?
3. **What's missing?** What would make it better?

Your feedback helps improve the system. If you're part of the beta test, share what's working and what isn't.

---

## Files Included

| File | Purpose |
|------|---------|
| `DM_SYSTEM_PROMPT.md` | Instructions that make Claude act as LoreLock |
| `CAMPAIGN_REGISTRY_TEMPLATE.json` | Master template for your campaign state |
| `SESSION_LOG_TEMPLATE.json` | Template for logging individual sessions |
| `QUICK_START_GUIDE.md` | This guide |

---

*LoreLock v1.0 - Your world deserves to be remembered.*
