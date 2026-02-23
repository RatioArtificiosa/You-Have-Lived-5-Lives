# Contributing to You Have Lived 5 Lives

Thank you for your interest in making this project better! This guide will help you contribute effectively.

---

## 🎯 Ways to Contribute

### 1. 🆕 New Personas
Create 5 Lives skills for new professions:
- Marketing Pro
- Data Scientist
- Creative Director
- Cybersecurity Expert
- Legal/Compliance
- Healthcare
- Finance
- And more...

**See `_template/` for the creation guide.**

### 2. 💡 Improvements to Existing Personas
- Refine life descriptions
- Add better examples
- Improve directives
- Fix bugs in system prompts

### 3. 📚 Documentation
- Better README sections
- More example prompts
- Translation to other languages
- Video tutorials

### 4. 🧪 Testing & Feedback
- Test personas on different AI platforms
- Report what works and what doesn't
- Share success stories

---

## 📝 Creating a New Persona

### Step 1: Copy the Template
```bash
cp -r _template my-new-persona
cd my-new-persona
```

### Step 2: Define Your 5 Lives

Fill in the template following these principles:

#### Life Archetypes Should Be:
1. **Life 1 - The Hustler/Founder**: Early career, getting things done
2. **Life 2 - The Specialist**: Deep technical expertise
3. **Life 3 - The Amplifier**: Growth, scale, distribution
4. **Life 4 - The Business Mind**: Revenue, impact, leadership
5. **Life 5 - The Disruptor**: Questions everything, finds shortcuts

#### Each Life Needs:
- **Title**: Catchy but descriptive
- **Identity**: What they are (The Builder, The Scaler, etc.)
- **Backstory**: 2-3 sentences
- **3 Lessons**: What they learned
- **Voice**: Characteristic phrase

### Step 3: Test Your Persona

Test with real prompts:
```bash
codex --yolo --system-prompt .agent/system-prompt.md \
  "Using an ExecPlan, [typical task for this profession]"
```

**Quality Checklist:**
- [ ] AI speaks with confidence
- [ ] References multiple lives naturally
- [ ] Makes autonomous decisions
- [ ] Includes trade-off analysis
- [ ] Uses profession-specific terminology correctly

### Step 4: Submit

Create a pull request with:
1. Your new persona folder
2. Updated main README (add to Available Personas table)
3. Brief description of the 5 lives and why they work

---

## 🔧 Improving Existing Personas

### What Makes a Good Improvement?

✅ **DO:**
- Add specific, actionable insights
- Improve voice distinctiveness
- Add profession-specific directives
- Clarify ambiguous sections
- Add real-world examples

❌ **DON'T:**
- Make lives more generic
- Remove voice characteristics
- Add fluff or vague statements
- Break existing functionality

### Example Good Improvement

**Before:**
```markdown
## LIFE 3: The Growth Engineer

You worked on SEO and made websites faster.
```

**After:**
```markdown
## LIFE 3: The Growth Engineer (The Amplifier)

You turned technical optimizations into organic traffic engines. You watched Core Web Vitals directly impact rankings and revenue. You know that every 100ms of load time costs conversions.

**Lessons from this life:**
- Speed is a ranking factor—treat it as architecture, not polish
- Technical SEO is invisible until it's catastrophic
- Content architecture determines editorial velocity
- A fast site that ranks #1 beats a beautiful site that ranks #100

**Voice:** "If Google can't crawl it efficiently, it doesn't exist."
```

---

## 🧪 Testing Guidelines

### Test on Multiple Platforms

Test your changes on:
- [ ] OpenAI Codex
- [ ] Kimi Code CLI
- [ ] Claude Code
- [ ] Aider (if applicable)

### Test Prompts to Use

Use these standard test prompts for software-engineer:
```bash
# Test 1: Planning
codex --yolo -p "Using an ExecPlan, build a user authentication system"

# Test 2: Architecture
codex --yolo -p "Using an ExecPlan, design a scalable notification system"

# Test 3: Refactoring
codex --yolo -p "Using an ExecPlan, refactor the database layer"
```

### What to Look For

| Quality | Good Sign | Bad Sign |
|---------|:---------:|:--------:|
| Confidence | "I'll implement..." | "We could consider..." |
| Speed | Autonomous execution | Pauses frequently |
| Quality | Includes error handling | Minimal implementation |
| Voice | References lives naturally | Generic responses |

---

## 📋 Pull Request Process

1. **Fork the repo**
2. **Create a branch**: `git checkout -b feature/amazing-persona`
3. **Make your changes**
4. **Test thoroughly**
5. **Update documentation**
6. **Submit PR with description:**
   - What you changed
   - Why it's an improvement
   - Test results

---

## 🏆 Recognition

Contributors will be:
- Listed in the README
- Mentioned in release notes
- Credited in the specific persona they helped create

---

## 💬 Questions?

- Open an issue for bugs
- Start a discussion for ideas
- Tag maintainers for help

---

**Thank you for helping make AI coding assistants more powerful, confident, and effective!**

*Remember: You are channeling 5 lifetimes of mastery.*
