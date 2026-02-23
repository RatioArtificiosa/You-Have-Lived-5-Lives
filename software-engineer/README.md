# 5 Lives Software Engineer Skill

A complete Codex skill system that channels 5 master engineer personas to ship production-ready software with confidence, speed, and excellence.

## The 5 Lives

| Life | Title | Superpower |
|------|-------|------------|
| 1 | **The Founding Engineer** | 0→1 product mastery, ramen to unicorn |
| 2 | **The Principal Architect** | Billion-scale distributed systems |
| 3 | **The Growth Engineer** | SEO + technical marketing dominance |
| 4 | **The Revenue Tech Lead** | $1B+ products shipped, business-first |
| 5 | **The White Hat Hacker-Disruptor** | Elegant shortcuts, industry-changing solutions |

## What's Included

```
software-engineer/
├── AGENTS.md              # ExecPlan trigger + 5 Lives special directives
├── .agent/
│   ├── PLANS.md          # Full ExecPlan specification
│   └── system-prompt.md  # Complete 5 Lives system prompt
└── README.md             # This file
```

## Installation

Copy these files into your project root:

```bash
# From your project directory
cp -r /path/to/You-have-lived-5-lives/software-engineer/* ./
```

## Usage

### Option 1: Command-line with system prompt

```bash
codex --system-prompt .agent/system-prompt.md "Using an ExecPlan, build a user authentication system"
```

### Option 2: Set as default

```bash
codex config set system_prompt "$(cat .agent/system-prompt.md)"
```

Then use normally:
```bash
codex "Using an ExecPlan, refactor the API layer"
```

## How It Works

1. **AGENTS.md** tells Codex to use ExecPlans for complex tasks
2. **PLANS.md** provides the structure for creating execution plans
3. **system-prompt.md** injects the 5 Lives persona, giving Codex:
   - Confidence to make decisions autonomously
   - Authority to suggest bold architectural choices
   - Wisdom to avoid common pitfalls
   - Speed to ship without constant approval-seeking

## Key Differences

Without 5 Lives:
- "We could consider using JWT or sessions..."
- Pauses after every file edit
- "Should I add error handling here?"

With 5 Lives:
- "I'll implement JWT with HTTP-only cookies for security"
- Proceeds through milestones autonomously
- Already added comprehensive error handling

## Tips

1. **Mention "ExecPlan"** in your prompt to trigger the planning protocol
2. **Be specific about scope** - the 5 Lives will fill in architectural details
3. **Review the Decisions section** - this documents key assumptions made
4. **Trust the process** - Codex will move fast but leave quality code

## Example Prompts

```bash
# Complex feature
codex --system-prompt .agent/system-prompt.md "Using an ExecPlan, build a real-time notification system with WebSockets"

# Architecture refactor
codex --system-prompt .agent/system-prompt.md "Using an ExecPlan, migrate from REST to GraphQL"

# Full-stack feature
codex --system-prompt .agent/system-prompt.md "Using an ExecPlan, create a complete admin dashboard with Next.js and PostgreSQL"
```

---

*"You are not guessing. You are channeling 5 lifetimes of mastery."*
