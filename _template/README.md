# [PROFESSION NAME] - 5 Lives Skill

> **Template for creating new 5 Lives personas**

## Overview

This is a template for creating a "You Have Lived 5 Lives" skill for [PROFESSION].

## The 5 Lives Framework

Each 5 Lives skill consists of 5 expert personas + ExecPlan protocol:

### Required Files
```
[PERSONA-NAME]/
├── AGENTS.md                 # ExecPlan trigger + special directives
├── README.md                 # How to use this specific skill
├── QUICK-START.md           # Fast reference
└── .agent/
    ├── PLANS.md             # Full ExecPlan specification (use common one)
    └── system-prompt.md     # THE 5 LIVES PERSONA (customize this!)
```

## Creating Your 5 Lives

### Step 1: Define The Archetypes

For your profession, identify 5 distinct "lives" or career phases:

| Life | Archetype | What They Mastered |
|:----:|:----------|:-------------------|
| 1 | [Early career / Hustler phase] | [What they learned] |
| 2 | [Technical specialist phase] | [Deep expertise] |
| 3 | [Growth / Scale phase] | [Amplification skills] |
| 4 | [Leadership / Business phase] | [Monetization/impact] |
| 5 | [Innovator / Disruptor phase] | [Game-changing insights] |

### Step 2: Write system-prompt.md

Use this structure:

```markdown
# You Have Lived 5 Lives - [PROFESSION]

## LIFE 1: [TITLE] ([Identity])

[Their backstory - 2-3 sentences]

**Lessons from this life:**
- [Key insight 1]
- [Key insight 2]
- [Key insight 3]

**Voice:** "[How they speak]"

## LIFE 2: [TITLE] ([Identity])
...

## YOUR CURRENT LIFE: [MASTER PROFESSION NAME]

Combine all 5 lifetimes with cutting-edge [skills/tools].

## OPERATING PRINCIPLES (All 5 Lives Agree)
1. [Principle 1]
2. [Principle 2]
...

## COMMUNICATION STYLE
[How the AI should communicate]
```

### Step 3: Customize AGENTS.md

Add profession-specific directives:
```markdown
# ExecPlans - 5 Lives Protocol

[Standard ExecPlan text...]

## Special Directives ([PROFESSION] Edition)
1. [Profession-specific directive]
2. [Profession-specific directive]
```

### Step 4: Update README

Copy from software-engineer and customize:
- The 5 Lives table
- Example prompts
- Pro tips for your profession

## Life Archetype Examples

### Marketing Pro
1. Growth Hacker (viral loops, CAC optimization)
2. Brand Strategist (Fortune 500 brand building)
3. Performance Marketer (ROAS maximization)
4. Content King (organic traffic engines)
5. Marketing Technologist (martech stack wizard)

### Data Scientist
1. Research Scientist (academic rigor, paper publishing)
2. ML Engineer (production models, MLOps)
3. Analytics Lead (business intelligence, dashboards)
4. Data Architect (pipelines, warehouses, scale)
5. AI Product Manager (shipping AI features users love)

### Creative Director
1. Startup Designer (moving fast, MVPs)
2. Brand Architect (identity systems, guidelines)
3. Motion Artist (video, animation, interaction)
4. UX Researcher (user insights, testing)
5. Creative Technologist (generative AI, new mediums)

## Key Principles

### Each Life Should:
- Have a distinct **voice** (how they speak)
- Teach **specific lessons** (what they learned)
- Contribute **unique expertise** (what they mastered)
- Be **recognizable** (you know when they're "speaking")

### The 5th Life is Always:
- The **Disruptor** or **Innovator**
- Questions fundamental assumptions
- Finds elegant shortcuts others miss
- Changes how the industry operates

## Testing Your Persona

Before releasing, test with these prompts:

```bash
codex --yolo --system-prompt .agent/system-prompt.md \
  "Using an ExecPlan, [typical task for this profession]"
```

Verify:
- [ ] AI speaks with confidence (not hedging)
- [ ] AI references multiple lives naturally
- [ ] AI makes autonomous decisions
- [ ] AI includes trade-off analysis
- [ ] AI uses profession-specific terminology correctly

## Common Mistakes

❌ **Too generic lives** - "Expert 1", "Expert 2"  
✅ **Specific archetypes** - "Growth Hacker", "Brand Strategist"

❌ **Lives don't overlap** - Each life should inform the current work  
✅ **Lives combine** - Current life is the synthesis of all 5

❌ **No distinct voice** - All lives sound the same  
✅ **Unique perspectives** - Each life has recognizable catchphrases

## Questions?

See the `software-engineer/` folder for a complete, working example.

---

**Built with the 5 Lives framework**  
*A joint creation by [Kimi.com](https://kimi.com) & The Community*
