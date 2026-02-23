# Quick Start - Marketing Pro 5 Lives

## 30-Second Setup

1. **Copy files to your project:**
   ```bash
   cp -r marketing-pro/* /your/project/
   ```

2. **Run with the system prompt:**
   ```bash
   cd /your/project
   codex --yolo --system-prompt .agent/system-prompt.md \
     "Using an ExecPlan, build a customer acquisition strategy"
   ```

3. **Watch the magic** ✨

## Magic Words

Trigger the full 5 Lives experience:

| Trigger | Use Case |
|---------|----------|
| "Using an ExecPlan" | Activates planning protocol |
| "viral" "high-converting" | Triggers research + premium execution |
| "comprehensive strategy" | Full-funnel approach |
| "data-driven" | Analytics + measurement included |

## Example Sessions

### Growth Campaign
```bash
codex --yolo -p "Using an ExecPlan, design a referral program 
that incentivizes sharing and drives viral growth"
```

### Content Strategy
```bash
codex --yolo -p "Using an ExecPlan, create a 90-day content 
calendar targeting enterprise SaaS buyers"
```

### Paid Acquisition
```bash
codex --yolo -p "Using an ExecPlan, build a Meta Ads campaign 
structure for a $50k/month budget"
```

### Email Automation
```bash
codex --yolo -p "Using an ExecPlan, design lifecycle email 
flows: onboarding, activation, retention, win-back"
```

## Pro Tips

1. **Enable Web Search!** Add to `~/.codex/config.toml`:
   ```toml
   [features]
   web_search = "live"
   ```
   This lets the Marketing Pro research current trends, competitor campaigns, and platform best practices!

2. **Include budget** when discussing paid acquisition
3. **Mention target audience** for better positioning
4. **Say "data-driven"** for analytics and measurement
5. **Use "viral"** for growth hacking mechanics

## Troubleshooting

**AI not using ExecPlan format?**
- Make sure you say "Using an ExecPlan"
- Verify AGENTS.md exists

**Output seems generic?**
- Use quality keywords: "high-converting," "best-performing"
- Be specific about channels or metrics

---

**Remember:** *Channel 5 master marketers. Dominate your market.*
