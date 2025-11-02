# MCP Toolbox Workflows Plugin

Composite workflows that orchestrate Julie (code intelligence), Sherpa (workflow guidance), and Goldfish (persistent memory) for powerful, systematic development patterns.

## Overview

This plugin provides **composite Skills** that combine the strengths of all three MCP toolbox servers:
- **Julie**: Fast code intelligence, semantic search, safe refactoring
- **Sherpa**: Workflow guidance with behavioral adoption
- **Goldfish**: Persistent memory and progress tracking

Together, they create workflows that are greater than the sum of their parts.

## Requirements

**This plugin requires all three MCP servers installed and configured:**

1. **[Julie](https://github.com/anortham/julie)** - Code intelligence server
   Fast semantic search, symbol navigation, safe refactoring

2. **[Sherpa](https://github.com/anortham/sherpa)** - Workflow guidance server
   Systematic development phases with behavioral adoption

3. **[Goldfish](https://github.com/anortham/goldfish)** - Persistent memory server
   Checkpoint progress, recall context, manage plans

**Install all three MCP servers first** by following the installation instructions in each repository above.

## Installation

### Step 1: Install MCP Servers

Install the three required MCP servers by following the instructions in each repository:

1. **[Julie Installation](https://github.com/anortham/julie#installation)** - Download binary or build from source
2. **[Sherpa Installation](https://github.com/anortham/sherpa#installation)** - Bun + TypeScript setup
3. **[Goldfish Installation](https://github.com/anortham/goldfish#installation)** - Bun + TypeScript setup

Make sure all three are added to your Claude Desktop `claude_desktop_config.json` and working.

### Step 2: Install This Plugin

```bash
# Clone this repository
git clone https://github.com/anortham/mcp-toolbox-workflows.git
```

Then install the plugin in Claude Code according to the [Claude Code plugin documentation](https://docs.claude.com/en/docs/claude-code/plugins).

**That's it!** The composite skills will automatically activate when appropriate based on your task context.

## Composite Skills

### 🧪 TDD Powerhouse
**Complete Test-Driven Development**

Orchestrates all three tools for systematic TDD:
- Sherpa guides through 4 phases
- Julie searches patterns and provides safe refactoring
- Goldfish checkpoints after each phase

**Phases:**
1. Define Contract - Julie finds similar patterns
2. Write Tests - Julie shows test examples
3. Implement - Julie aids navigation
4. Refactor - Julie enables safe refactoring

**Activates when:** Implementing new features, building from scratch

**Example:**
```
User: "Implement Stripe payment processing"

→ TDD Powerhouse activates
→ Sherpa guides through phases
→ Julie finds payment patterns in codebase
→ Goldfish checkpoints: design, tests, implementation, refactor
→ Result: Clean, tested payment processing with full history
```

### 🕵️ Bug Detective
**Systematic Bug Hunting**

Combines investigation tools for methodical debugging:
- Sherpa guides 4-phase bug hunt
- Julie traces execution and finds errors
- Goldfish documents investigation trail

**Phases:**
1. Reproduce & Isolate - Julie traces execution paths
2. Capture in Test - Julie finds test patterns
3. Fix the Bug - Julie enables safe fixes
4. Verify & Prevent - Julie checks impact

**Activates when:** Fixing bugs, debugging errors

**Example:**
```
User: "Users randomly getting logged out"

→ Bug Detective activates
→ Julie traces session.destroy() execution
→ Discovers race condition
→ Goldfish checkpoints investigation steps
→ Sherpa guides to test, fix, verify
→ Result: Bug fixed with test coverage and documented solution
```

### 🚀 Smart Session Start
**Intelligent Context Restoration** (MANDATORY)

Automatically restores full working context:
- Goldfish recalls last 7 days of work
- Julie re-indexes if needed
- Sherpa suggests appropriate workflow

**Activates at:** Every session start (automatic!)

**What it does:**
1. Recalls recent checkpoints and plans
2. Analyzes work patterns
3. Ensures workspace indexed
4. Suggests next workflow
5. Presents actionable next steps

**Example:**
```
[Claude Code starts]

→ Smart Session Start activates automatically
→ Goldfish: "Last session 2 hours ago - wrote 8 tests for PaymentService"
→ Julie: Workspace indexed, 247 files ready
→ Sherpa: "TDD Phase 2 complete, ready for Phase 3: Implementation"
→ Present: "Welcome back! Ready to implement PaymentService?"
```

### 🔄 Refactor with Confidence
**Safe Code Improvement**

Systematic refactoring with test protection:
- Sherpa guides refactor workflow
- Julie provides safe rename and reference checking
- Goldfish preserves before/after state

**Phases:**
1. Tests First - Ensure coverage
2. Refactor Code - Julie safe tools
3. Verify - Tests stay green

**Activates when:** Refactoring, code cleanup, reorganizing

**Example:**
```
User: "Extract validation logic from UserService"

→ Refactor with Confidence activates
→ Goldfish: Pre-refactor checkpoint
→ Sherpa: Verify tests exist (23 tests ✅)
→ Julie: Extract UserValidator class, rename references
→ Goldfish: Post-refactor checkpoint
→ Result: Clean extraction, all tests green, full history
```

### 📚 Explore and Document
**Codebase Understanding**

Systematic exploration with documentation:
- Julie's token-efficient exploration (70-90% savings!)
- Sherpa guides exploration phases
- Goldfish documents findings as plans

**Phases:**
1. Learn - Architecture overview
2. Investigate - Patterns and flows
3. Prototype - Verify understanding (optional)
4. Document - Create architecture plan

**Activates when:** Learning new code, onboarding, documentation

**Example:**
```
User: "Help me understand the authentication system"

→ Explore and Document activates
→ Julie: Semantic search finds auth components
→ Julie: get_symbols shows structure (93% token savings!)
→ Julie: trace_call_path maps execution flow
→ Goldfish: Checkpoints discoveries
→ Goldfish: Creates "Auth Architecture" plan
→ Result: Complete understanding, documented for future reference
```

## How Composite Skills Work

### Tool Orchestration

Each composite skill coordinates multiple tools:

```
TDD Powerhouse Flow:
1. Goldfish recall → Restore context
2. Sherpa approach(tdd) → Activate workflow
3. Sherpa guide → Get phase guidance
4. Julie fast_search → Find patterns
5. [User works]
6. Goldfish checkpoint → Save progress
7. Sherpa guide(done) → Advance phase
8. Repeat for each phase
```

### Cross-Tool Benefits

**Sherpa + Julie:**
- Sherpa guides WHEN to search
- Julie provides efficient search
- Result: Systematic code discovery

**Julie + Goldfish:**
- Julie finds code
- Goldfish documents findings
- Result: Knowledge preservation

**Goldfish + Sherpa:**
- Goldfish restores context
- Sherpa suggests workflow
- Result: Seamless continuation

**All Three Together:**
- Systematic process (Sherpa)
- Efficient execution (Julie)
- Persistent memory (Goldfish)
- Result: Professional workflow automation

## Usage Patterns

### Session Start (Every Time)
```
[Claude Code starts]
→ Smart Session Start activates automatically
→ Context restored
→ Workspace ready
→ Workflow suggested
→ Next steps clear
```

### Feature Development
```
User: "Implement X feature"
→ TDD Powerhouse activates
→ Guides through test-first development
→ Checkpoints all progress
→ Result: Well-tested feature
```

### Bug Fixing
```
User: "Fix this bug"
→ Bug Detective activates
→ Systematic investigation
→ Test-driven fix
→ Result: Bug fixed with prevention
```

### Code Improvement
```
User: "Refactor this"
→ Refactor with Confidence activates
→ Safe refactoring with tests
→ Before/after tracking
→ Result: Cleaner code, tests green
```

### Learning Code
```
User: "Understand this codebase"
→ Explore and Document activates
→ Token-efficient exploration
→ Documented findings
→ Result: Knowledge preserved
```

## Performance

### Composite Overhead
- Skill orchestration: ~50-100ms
- Cross-tool coordination: ~10-20ms per call
- Total overhead: Negligible (<200ms)

### End-to-End Workflows
- **TDD Powerhouse**: 4 phases, ~2-10 minutes (implementation time)
- **Bug Detective**: 4 phases, ~1-5 minutes (debugging time)
- **Smart Session Start**: <500ms (instant context)
- **Refactor with Confidence**: 3 phases, ~1-3 minutes
- **Explore and Document**: 4 phases, ~2-5 minutes

## Integration Examples

### TDD with Session Continuity
```
Day 1:
→ Smart Session Start (new work)
→ TDD Powerhouse (Phases 1-2)
→ Goldfish checkpoints design and tests
[End of day]

Day 2:
→ Smart Session Start (restores context)
→ "Last session: Wrote 8 tests for PaymentService"
→ TDD Powerhouse resumes (Phase 3: Implementation)
→ Complete phases 3-4
→ Goldfish final checkpoint
```

### Bug Hunt with Documentation
```
→ Bug Detective activates
→ Phase 1: Julie traces execution, Goldfish logs discoveries
→ Phase 2: Julie finds test patterns
→ Phase 3: Implement fix
→ Phase 4: Verify with Julie's fast_refs
→ Goldfish: Complete investigation trail preserved
```

### Refactoring During Feature Work
```
[During TDD]
→ TDD Phase 2: Writing tests
→ Notice messy code
→ Refactor with Confidence (sub-workflow)
  - Tests exist ✅
  - Safe refactor with Julie
  - Back to TDD
→ Continue TDD with cleaner code
```

## Best Practices

### Let Skills Activate Automatically
- Smart Session Start is mandatory (don't prevent it!)
- Other skills activate based on task intent
- Trust the skill selection logic

### Checkpoint Frequently
- After each TDD phase
- After each discovery
- Before and after refactoring
- At natural stopping points

### Use Julie Efficiently
- get_symbols before reading files (70-90% token savings!)
- Semantic search for concepts
- Trace execution paths for understanding

### Follow Sherpa Guidance
- Don't skip phases
- Mark progress explicitly with guide(done)
- Let celebrations happen naturally

### Document with Goldfish
- Create plans for long-term work
- Checkpoint discoveries
- Use tags for searchability

## Troubleshooting

### Composite skill not activating
- Verify all three dependencies installed
- Check MCP servers are running
- Restart Claude Code

### Cross-tool coordination slow
- Check individual tool performance
- Ensure Julie workspace is indexed
- Verify Goldfish storage accessible

### Workflow suggestions off
- More checkpoints help pattern detection
- Explicit workflow requests work (e.g., "use TDD")
- Session start analyzes recent work only

## Advanced Usage

### Custom Workflow Combinations
```
Create your own patterns:
1. Goldfish recall specific work
2. Julie search related code
3. Sherpa activate appropriate workflow
4. Execute with orchestration
5. Goldfish checkpoint results
```

### Cross-Workspace Workflows
```
→ Smart Session Start shows all workspace activity
→ TDD in primary workspace
→ Explore reference workspace with Julie
→ Document findings across workspaces
```

## Philosophy

**Systematic Development:**
These composite skills enforce good practices through intelligent orchestration, not rigid constraints.

**Memory Persistence:**
Work survives context resets, crashes, and time away. Knowledge is preserved.

**Efficiency:**
Julie's token efficiency (70-90% savings) makes systematic exploration practical.

**Behavioral Adoption:**
Sherpa's celebrations build habits. Goldfish's checkpointing builds discipline.

**Professional Quality:**
Test-first development, systematic debugging, safe refactoring - all encouraged naturally.

---

**The whole is greater than the sum of its parts. Julie + Sherpa + Goldfish = Professional development workflow automation! 🚀**
