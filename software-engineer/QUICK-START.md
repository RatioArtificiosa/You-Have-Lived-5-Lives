# Quick Start - 5 Lives Software Engineer

## 30-Second Setup

1. **Copy files to your project:**
   ```bash
   cp -r software-engineer/* /your/project/
   ```

2. **Run Codex with the system prompt:**
   ```bash
   cd /your/project
   codex --system-prompt .agent/system-prompt.md "Using an ExecPlan, [your task here]"
   ```

## Example Session

```bash
$ cd ~/my-startup
$ codex --system-prompt .agent/system-prompt.md "Using an ExecPlan, build a complete user authentication system with email verification and password reset"

# Codex will:
# 1. Read AGENTS.md and PLANS.md
# 2. Create .agent/auth-system-plan.md following the ExecPlan format
# 3. Begin implementing autonomously through milestones
# 4. Update Progress checklist as it works
```

## Magic Words

To trigger the full 5 Lives experience, include these in your prompt:

| Trigger | Effect |
|---------|--------|
| "Using an ExecPlan" | Activates planning protocol |
| "Plan and implement" | Creates plan first, then executes |
| "Complex feature" | Signals to use full 5 Lives depth |
| "Production-ready" | Triggers quality gates |

## What to Expect

**Before (normal Codex):**
- Hesitant suggestions
- Frequent pauses for approval
- Questions about implementation details

**After (5 Lives Codex):**
- Confident architectural decisions
- Autonomous milestone execution
- Trade-off analysis included
- Production-ready code with tests

## Troubleshooting

**Codex isn't using the ExecPlan format?**
- Make sure you say "Using an ExecPlan" in your prompt
- Verify AGENTS.md and .agent/PLANS.md exist

**Codex seems hesitant?**
- Ensure you're using `--system-prompt .agent/system-prompt.md`
- The system prompt sets the confident tone

**Want even faster execution?**
- Add to your prompt: "Move fast. Document assumptions in Decisions."

## Next Steps

Once you've used this skill, try:
- Creating your own ExecPlan templates
- Modifying the 5 Lives for your specific stack
- Sharing improvements back to the community

---

**Remember:** You are channeling 5 master engineers. Trust the process.
