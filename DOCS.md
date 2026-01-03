# Usage Guide

## Getting Started

Run the command with a description of what you want to build:

```bash
/spec:init <what you want to build or document>
```

## Demo

### 1. Welcome
Describe your feature, bug fix, or system to spec out.

![Welcome](assets/01-welcome.png)

---

### 2. Interview
Claude asks targeted questions with selectable options.

![Interview](assets/02-interview-questions.png)

---

### 3. Deep Dive
Multiple rounds covering architecture, edge cases, tradeoffs.

![Deep Dive](assets/03-interview-deep-dive.png)

---

### 4. Insights
Claude explains complex concepts as you discuss them.

![Insights](assets/04-insights-explanations.png)

---

## Intent Detection

The plugin detects your intent from signal words:

| Intent | Signal Words | Behavior |
|--------|--------------|----------|
| **Document** | "document", "spec out", "PRD", "requirements" | Creates SPEC.md, then stops |
| **Build** | "build", "implement", "create", "add", "make" | Creates SPEC.md, then executes |
| **Explore** | No clear signal | Creates SPEC.md, asks what to do |

## Examples

```bash
# Documentation only
/spec:init document the authentication system
/spec:init spec out a caching layer

# Build immediately
/spec:init build a notification service
/spec:init implement OAuth login

# Exploratory
/spec:init caching
/spec:init user dashboard
```

## Resume Mode

Pick up an existing spec in a new session:

```bash
/spec:init implement ./SPEC.md
```

## Output

The generated `SPEC.md` includes:

- Quick reference summary
- Problem statement & goals
- System architecture (Mermaid diagrams)
- File structure with paths
- Codebase patterns to follow
- Implementation phases
- Verification commands
- Test cases
- Debugging guide
