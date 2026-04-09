# Invinsible: The Vibecoding Framework for OpenCode

**Build apps with AI — without needing to write code yourself.**

Invinsible is a framework that gives OpenCode everything it needs to build your app autonomously. Just tell it what you want, and it handles the technical work. You test in your browser and say what's wrong. That's it.

---

## Who Is This For?

- **Non-technical people** who have app ideas but don't know how to code
- **Solo builders** who want to move fast without learning development
- **Teams** who want a standardized way to build with AI

If you've ever thought "I wish I could just tell someone what I want and they'd build it" — this framework is exactly that, but the "someone" is OpenCode.

---

## What You'll Need

1. **OpenCode installed** on your computer (free, open-source)
2. **An idea** for something you want to build
3. **10-15 minutes** for the first setup conversation

That's it. No coding knowledge required.

---

## Step-by-Step: How to Use This Framework

### Step 1: Copy the Framework Into Your Project

Create a new folder for your app idea, then copy these files into it:

```
your-project/
├── AGENTS.md           ← Keep at root (tells OpenCode how to work)
├── SETUP.md           ← Keep at root (setup wizard)
├── opencode.json      ← Keep at root (permissions config)
├── .opencode/        ← Keep this folder as-is
│   └── agents/       ← Your custom agents
└── context/          ← Your project's knowledge (generated during setup)
```

### Step 2: Open OpenCode in Your Project Folder

Open your terminal in that folder and run:

```bash
opencode
```

Or open the folder in your IDE where OpenCode is integrated.

### Step 3: Start the Setup Wizard

Type naturally — not a command. Just say:

> "I want to build [your idea]."

OpenCode will read AGENTS.md, find that setup isn't done, and start the setup wizard automatically. It asks you questions like:

- What are you building?
- Who is it for?
- What problem does it solve?
- What features do you want?
- How should it look?

**You just answer in plain English.** That's all.

### Step 4: Setup Completes

When done, OpenCode generates a full `context/` folder with everything it needs to remember about your project:

- `context/project/` — What you're building, scope, roadmap, task list
- `context/features/` — Each feature's specification
- `context/technical/` — Tech stack, database, APIs
- `context/design/` — Colors, typography, UI patterns
- `context/developer/` — Code rules, testing approach

OpenCode reads these automatically at the start of every session.

### Step 5: Build Your First Feature

When ready, just say what you want:

> "Build user login" or "Add a contact form"

OpenCode follows a pipeline:

1. **Check** — Is this in your plan?
2. **Spec** — Write exactly what needs building
3. **Build** — Write the code
4. **Review** — Check for problems
5. **Test** — Run automated tests
6. **You test** — Try it in your browser (the only step you do)
7. **Sync** — Update all docs

### Step 6: Test in Your Browser

OpenCode gives you a simple checklist:

```
Browser Test: User Login

1. Go to http://localhost:3000/login
2. Enter "test@example.com" and "password123"
3. Click "Sign In"
4. Look for: You should see the dashboard

What to report:
- Did you get to the dashboard?
- Any error messages?
- What happened instead?
```

You just follow the steps, click around, and tell OpenCode what you see. If something looks wrong, describe it and OpenCode fixes it.

### Step 7: Continue Anytime

Close the chat. Come back later. Just say:

> "Continue where we left off" or "What were we working on?"

OpenCode reads the task list and picks up exactly where it stopped. No need to explain anything.

---

## How the Communication Works

With this framework, you never need to:

- Open a terminal
- Run a command
- Read an error message
- Understand what went wrong

OpenCode does the technical work. You make decisions and test in the browser.

| Instead of... | You just say... |
|---|---|
| "Run npm run dev" | (OpenCode runs it. You just open the URL it gives you) |
| "Install dependencies" | (OpenCode installs them. It tells you when ready) |
| "Run the tests" | (OpenCode runs them. It tells you pass/fail) |
| "Fix the bug" | "The login button isn't working" — OpenCode finds and fixes it |

---

## The Mental Model

Think of this framework as having a **technical partner** who:

- Reads your project context before every conversation
- Always knows what task comes next
- Handles all the code, commands, and debugging
- Gives you simple things to test in your browser
- Fixes anything you say looks wrong

Your job is simple:
1. Answer questions during setup
2. Say what you want to build
3. Test in your browser and report what you see

That's it. OpenCode handles the rest.

---

## File Structure

Here's what lives where:

```
your-project/
├── AGENTS.md              ← Instructions for OpenCode (don't edit)
├── SETUP.md               ← Setup wizard (don't edit)
├── opencode.json          ← Permissions (don't edit)
├── .opencode/
│   ├── agents/            ← Custom agents (don't edit)
│   └── commands/         ← Custom commands (optional)
└── context/               ← YOUR project's knowledge
    ├── project/
    │   ├── OVERVIEW.md    ← What you're building
    │   ├── SCOPE.md       ← What's in/out of v1
    │   ├── ROADMAP.md     ← Build phases
    │   ├── TASK-LIST.md   ← What needs doing
    │   └── DECISIONS.md  ← Why decisions were made
    ├── features/
    │   └── [feature].md  ← One file per feature
    ├── technical/
    │   ├── STACK.md      ← Tech choices
    │   ├── DATA_MODELS.md
    │   └── ENVIRONMENT.md
    ├── design/
    │   ├── DESIGN_SYSTEM.md
    │   └── COMPONENTS.md
    ├── developer/
    │   ├── CONVENTIONS.md
    │   └── WORKFLOW.md
    └── ops/
        └── INFRASTRUCTURE.md
```

The `context/` folder is your project's brain. OpenCode reads it every session.

---

## What If Something Goes Wrong?

**Don't panic. Just describe what happened.**

| You say... | OpenCode does... |
|---|---|
| "It won't start" | Checks the error, fixes it, tries again |
| "The button doesn't work" | Investigates why, fixes the code |
| "I'm getting an error" | Reads the error, diagnoses it, solves it |
| "This looks wrong" | Looks at what you expected, finds the bug, fixes it |

You never need to debug. Just describe the symptom. OpenCode finds the cause.

---

## Key Principles

1. **OpenCode does technical work, you make decisions**
   - You never touch code or terminals
   - You test in browser, report what you see

2. **Context is the memory**
   - Everything lives in `context/` folder
   - You never repeat yourself between sessions

3. **Task list drives the work**
   - Every task has a T-number
   - OpenCode always knows what's next

4. **Human validation is required**
   - Features aren't complete until you test them
   - Your browser is the final check

5. **Pick up anytime**
   - Say "continue" and OpenCode resumes
   - No need to re-explain

---

## Quick Reference

| When you want to... | You say... |
|---|---|
| Start a new project | "I want to build [idea]" |
| Build something | "Add [feature]" or "Build [feature]" |
| Fix something | "The [something] isn't working" |
| Test what we built | "Test this" or "Let me test" |
| Continue | "Continue" or "Where were we?" |
| See what's next | "What's next?" |

---

## Prerequisites to Check Before Starting

1. **OpenCode is installed**
   - Run `opencode --version` to verify

2. **API key configured**
   - OpenCode needs a model provider (Anthropic, OpenAI, etc.)
   - Set your API key in environment or OpenCode config

3. **Permissions allow dev commands**
   - The included `opencode.json` allows common commands
   - If something is blocked, OpenCode will tell you

---

## What This Framework Gives You

- A setup wizard that asks the right questions
- A context system that remembers everything
- A feature pipeline with built-in quality checks
- Human validation as a required step
- Autonomous task management — no "what next?" questions

**You bring the idea. OpenCode brings the code.**

---

## Need Help?

- **Setup questions?** → Read `SETUP.md`
- **Project context?** → Read files in `context/`
- **What features exist?** → Check `context/project/ROADMAP.md`

The `context/` folder is your single source of truth. OpenCode reads it, you can read it too.

---

*Invinsible + OpenCode = Build anything without writing code.*