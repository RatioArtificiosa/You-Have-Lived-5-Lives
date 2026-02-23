# Quick Start - Creative Director 5 Lives

## 30-Second Setup

1. **Copy files to your project:**
   ```bash
   cp -r creative-director/* /your/project/
   ```

2. **Run with the system prompt:**
   ```bash
   cd /your/project
   codex --yolo --system-prompt .agent/system-prompt.md \
     "Using an ExecPlan, design a brand system"
   ```

3. **Watch the magic** ✨

## Magic Words

Trigger the full 5 Lives experience:

| Trigger | Use Case |
|---------|----------|
| "Using an ExecPlan" | Activates planning protocol |
| "beautiful" "premium" | Triggers research + motion + polish |
| "design system" | Full component architecture |
| "micro-interactions" | Motion and delight focus |

## Example Sessions

### Brand System
```bash
codex --yolo -p "Using an ExecPlan, create a complete brand identity 
with logo, color system, typography, and component library"
```

### UI/UX Design
```bash
codex --yolo -p "Using an ExecPlan, design a premium mobile app UI 
with animations and interaction patterns"
```

### Creative Technology
```bash
codex --yolo -p "Using an ExecPlan, create an immersive landing page 
with generative backgrounds and scroll animations"
```

### Motion Design
```bash
codex --yolo -p "Using an ExecPlan, design a comprehensive animation 
system with easing curves and timing specifications"
```

## Pro Tips

1. **Enable Web Search!** Add to `~/.codex/config.toml`:
   ```toml
   [features]
   web_search = "live"
   ```
   This lets the Creative Director research current Awwwards trends, Behance featured work, and design Twitter for the latest patterns!

2. **Include brand context** (target audience, values, competitors)
3. **Mention technical constraints** (React, specific design system)
4. **Say "delightful"** for motion and micro-interactions
5. **Use "accessible"** for WCAG compliance focus

## Troubleshooting

**AI not including motion?**
- Use keywords: "animated," "delightful," "micro-interactions"

**Output seems generic?**
- Add: "research current trends" or "Awwwards-style"

---

**Remember:** *Channel 5 master creators. Design experiences that move people.*
