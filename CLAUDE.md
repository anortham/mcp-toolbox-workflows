# MCP Toolbox Workflows - Claude Code Plugin

This plugin provides **composite skills** that orchestrate three powerful MCP servers together for systematic development workflows.

## Required Dependencies

This plugin **requires** all three MCP Toolbox plugins:

### 1. **Goldfish** - Persistent Memory System
- **GitHub**: https://github.com/anortham/goldfish
- **Purpose**: Checkpoint progress, recall context, manage plans
- **Key Tools**: `recall()`, `checkpoint()`, `plan()`

### 2. **Sherpa** - Workflow Guidance
- **GitHub**: https://github.com/anortham/sherpa
- **Purpose**: Guide through systematic development phases
- **Key Tools**: `guide()`, `approach()`

### 3. **Julie** - Code Intelligence
- **GitHub**: https://github.com/anortham/julie
- **Purpose**: Fast semantic search, symbol navigation, safe refactoring
- **Key Tools**: `fast_search()`, `fast_goto()`, `fast_refs()`, `get_symbols()`

## Composite Skills Included

This plugin provides 5 composite skills that orchestrate the above tools:

### 🚀 Smart Session Start
**Automatic context restoration at every session start**

- **Skill File**: [skills/smart-session-start/SKILL.md](skills/smart-session-start/SKILL.md)
- **What it does**:
  - Goldfish recalls recent work (7 days)
  - Julie re-indexes workspace if needed
  - Sherpa suggests appropriate workflow
  - Presents actionable next steps
- **Activates**: Automatically at session start
- **Use when**: Every session! Mandatory for context restoration

### 🧪 TDD Powerhouse
**Complete Test-Driven Development workflow**

- **Skill File**: [skills/tdd-powerhouse/SKILL.md](skills/tdd-powerhouse/SKILL.md)
- **What it does**:
  - Phase 1: Define Contract (Julie finds patterns)
  - Phase 2: Write Tests (Julie shows examples)
  - Phase 3: Implement (Julie aids navigation)
  - Phase 4: Refactor (Julie safe refactoring)
  - Goldfish checkpoints after each phase
- **Activates**: When implementing new features
- **Use when**: "Build X feature", "Implement Y", "Create new service"

### 🕵️ Bug Detective
**Systematic debugging workflow**

- **Skill File**: [skills/bug-detective/SKILL.md](skills/bug-detective/SKILL.md)
- **What it does**:
  - Phase 1: Reproduce & Isolate (Julie traces execution)
  - Phase 2: Capture in Test (Julie finds patterns)
  - Phase 3: Fix the Bug (Julie safe fixes)
  - Phase 4: Verify & Prevent (Julie checks impact)
  - Goldfish documents investigation trail
- **Activates**: When debugging or fixing bugs
- **Use when**: "Fix this bug", "Debug X error", "Users report Y issue"

### 🔄 Refactor with Confidence
**Safe code improvement workflow**

- **Skill File**: [skills/refactor-with-confidence/SKILL.md](skills/refactor-with-confidence/SKILL.md)
- **What it does**:
  - Phase 1: Tests First (ensure coverage)
  - Phase 2: Refactor Code (Julie safe tools)
  - Phase 3: Verify (tests stay green)
  - Goldfish preserves before/after state
- **Activates**: When refactoring code
- **Use when**: "Refactor X", "Clean up Y", "Extract Z class"

### 📚 Explore and Document
**Token-efficient codebase exploration**

- **Skill File**: [skills/explore-and-document/SKILL.md](skills/explore-and-document/SKILL.md)
- **What it does**:
  - Phase 1: Learn (architecture overview)
  - Phase 2: Investigate (patterns and flows)
  - Phase 3: Prototype (verify understanding)
  - Phase 4: Document (create architecture plan)
  - Julie provides 70-90% token savings!
- **Activates**: When learning unfamiliar code
- **Use when**: "Understand X system", "How does Y work?", "Explain this codebase"

## How Composite Skills Work

Each skill **orchestrates multiple tools** to create a cohesive workflow:

```
Example: TDD Powerhouse Flow
1. Goldfish recall → Restore context
2. Sherpa approach(tdd) → Activate TDD workflow
3. Sherpa guide → Get phase 1 guidance: "Define Contract"
4. Julie fast_search → Find similar patterns in codebase
5. [You design the interface based on patterns]
6. Goldfish checkpoint → Save design progress
7. Sherpa guide(done) → Advance to phase 2: "Write Tests"
8. Julie fast_search → Find test examples
9. [You write comprehensive tests]
10. Goldfish checkpoint → Save test progress
11. Sherpa guide(done) → Advance to phase 3: "Implement"
... and so on
```

## Installation

### Prerequisites
Install the three required MCP servers first:
1. Goldfish: https://github.com/anortham/goldfish
2. Sherpa: https://github.com/anortham/sherpa
3. Julie: https://github.com/anortham/julie

Follow each repo's installation instructions to set up the MCP servers.

### Install This Plugin

```bash
# Clone this repo
git clone https://github.com/anortham/mcp-toolbox-workflows.git

# Then add to Claude Code (method depends on your setup)
# See: https://docs.claude.com/en/docs/claude-code/plugins
```

## Documentation Links

### Claude Code Official Docs
- **Plugins**: https://docs.claude.com/en/docs/claude-code/plugins
- **Skills**: https://docs.claude.com/en/docs/claude-code/skills
- **MCP Servers**: https://docs.claude.com/en/docs/claude-code/mcp

### MCP Toolbox Components
- **Goldfish Plugin**: https://github.com/anortham/goldfish
- **Sherpa Plugin**: https://github.com/anortham/sherpa
- **Julie Plugin**: https://github.com/anortham/julie
- **This Plugin**: https://github.com/anortham/mcp-toolbox-workflows

### Skill Details (in this repo)
- [Smart Session Start](skills/smart-session-start/SKILL.md) - Session restoration
- [TDD Powerhouse](skills/tdd-powerhouse/SKILL.md) - Test-driven development
- [Bug Detective](skills/bug-detective/SKILL.md) - Systematic debugging
- [Refactor with Confidence](skills/refactor-with-confidence/SKILL.md) - Safe refactoring
- [Explore and Document](skills/explore-and-document/SKILL.md) - Codebase exploration

## Why Composite Skills?

**The whole is greater than the sum of its parts.**

Individual tools are powerful:
- Goldfish remembers your work
- Sherpa guides your process
- Julie makes code intelligence fast

**Together**, they create professional workflows:
- **TDD**: Systematic test-first development with checkpoints
- **Debugging**: Methodical investigation with preserved trail
- **Refactoring**: Safe improvements with test protection
- **Exploration**: Efficient learning with documented findings
- **Session Start**: Zero-friction context restoration

## Usage Examples

### Starting Your Day
```
[You start Claude Code]

→ Smart Session Start activates automatically
→ "Welcome back! Last session 16 hours ago..."
→ "You were implementing PaymentService (Phase 2: Tests written)"
→ "Workspace indexed, 247 files ready"
→ "Suggested: Continue TDD workflow, Phase 3: Implementation"

[You're instantly back in context, ready to code]
```

### Building a New Feature
```
You: "Implement Stripe payment processing"

→ TDD Powerhouse activates
→ Sherpa: "Phase 1: Define Contract"
→ Julie: Searches for similar payment patterns
→ [You design PaymentService interface]
→ Goldfish: Checkpoints design
→ Sherpa: "Phase 2: Write Tests"
→ Julie: Finds test examples
→ [You write 12 comprehensive tests]
→ Goldfish: Checkpoints tests
→ Sherpa: "Phase 3: Implementation"
... and so on
```

### Fixing a Bug
```
You: "Users getting randomly logged out"

→ Bug Detective activates
→ Sherpa: "Phase 1: Reproduce & Isolate"
→ Julie: Traces session.destroy() calls
→ [Discovers race condition]
→ Goldfish: Documents discovery
→ Sherpa: "Phase 2: Capture in Test"
→ [You write failing test]
→ Sherpa: "Phase 3: Fix the Bug"
... fix implemented, verified, documented
```

## Performance

- **Smart Session Start**: <500ms (instant context restoration)
- **Tool orchestration overhead**: ~50-100ms (negligible)
- **Julie token savings**: 70-90% (massive context efficiency)
- **Goldfish checkpoints**: ~10ms each (fast persistence)
- **Sherpa guidance**: ~50ms (instant phase updates)

**Result**: Workflows feel natural and fast!

## Philosophy

These composite skills enforce **professional development practices** through intelligent orchestration:

- ✅ **Systematic over reactive** (Sherpa guides phases)
- ✅ **Tested over untested** (TDD enforces test-first)
- ✅ **Efficient over wasteful** (Julie saves 70-90% tokens)
- ✅ **Persistent over ephemeral** (Goldfish preserves context)
- ✅ **Safe over risky** (Refactoring protected by tests)

Not rigid constraints - just good habits, naturally encouraged.

## Contributing

This plugin is open source (MIT License). Contributions welcome!

## Support

- **Issues**: https://github.com/anortham/mcp-toolbox-workflows/issues
- **Discussions**: https://github.com/anortham/mcp-toolbox-workflows/discussions

---

**The MCP Toolbox: Professional development workflow automation for Claude Code! 🚀**
