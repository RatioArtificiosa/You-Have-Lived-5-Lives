# Quick Start - Pulitzer Author 5 Lives

## 30-Second Setup

1. **Copy files to your project:**
   ```bash
   cp -r pulitzer-author/* /your/project/
   ```

2. **Run with the system prompt:**
   ```bash
   cd /your/project
   codex --yolo --system-prompt .agent/system-prompt.md \
     "Using an ExecPlan, write a compelling short story"
   ```

3. **Watch the magic** ✨

## Magic Words

Trigger the full 5 Lives experience:

| Trigger | Use Case |
|---------|----------|
| "Using an ExecPlan" | Activates planning protocol |
| "literary" "compelling" | Full craft mode |
| "character-driven" | Deep psychological complexity |
| "unforgettable" | Maximum emotional resonance |

## Example Sessions

### Novel Opening
```bash
codex --yolo -p "Using an ExecPlan, write the first chapter of a 
literary novel about a widow rebuilding her life, with sensory detail and emotional truth"
```

### Character Development
```bash
codex --yolo -p "Using an ExecPlan, create detailed character profiles 
for a protagonist with internal contradictions, complex motivations, and a compelling arc"
```

### Memoir Writing
```bash
codex --yolo -p "Using an ExecPlan, craft a memoir chapter that weaves 
personal experience with universal themes of resilience and transformation"
```

### Narrative Nonfiction
```bash
codex --yolo -p "Using an ExecPlan, write a narrative nonfiction piece 
about an unsung community hero, with immersive reporting and emotional depth"
```

## Pro Tips

1. **Enable Web Search!** Add to `~/.codex/config.toml`:
   ```toml
   [features]
   web_search = "live"
   ```
   This lets the Pulitzer Author research settings, historical context, and authentic details!

2. **Be specific about genre** (literary fiction, thriller, memoir, etc.)
3. **Mention themes** you want to explore
4. **Say "character-driven"** for psychological depth
5. **Use "sensory detail"** for immersive world-building
6. **Add "emotional truth"** for vulnerability and resonance

## Troubleshooting

**Writing feels generic?**
- Use: "with specific sensory details" or "fresh metaphors"

**Characters feel flat?**
- Add: "with internal contradictions" or "complex psychology"

**Plot feels predictable?**
- Say: "with subverted expectations" or "literary complexity"

---

**Remember:** *Channel 5 master storytellers. Write the story only you can tell.*

**No more mechanical writing. Only unforgettable stories.**
