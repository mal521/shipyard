# Claude Code in Cursor: A Beginner's Guide
*Written for high school students, parents, and anyone who has never used a terminal before*

---

## Before You Start: What Are We Installing?

Think of this like setting up a game. There are three things you need, and they all work together:

**Claude Pro** -- a subscription ($20/month, or start a free trial) from Anthropic. This is like buying a ticket that gives you access to Claude's brain. Without it, Claude Code won't work.

**Claude Code** -- the actual AI assistant that lives inside your terminal (the text window on your computer). You type questions and instructions to it in plain English, and it does the work.

**Cursor** -- a program that looks like a fancy notepad for writing code. It has a built-in terminal window at the bottom where you'll run Claude Code. The free version is all you need.

---

## Part 1: Installation

### Step 1 -- Get Claude Pro

1. Go to [claude.ai](https://claude.ai)
2. Create a free account if you don't have one
3. Click your name or icon in the bottom left corner and choose **Upgrade to Pro**
4. Subscribe ($20/month) or start a free trial if you'd rather not pay right away

Done. You now have access.

---

### Step 2 -- Install Cursor

1. Go to [cursor.com](https://cursor.com)
2. Click **Download** and install it like any other Mac app (drag it to your Applications folder)
3. Open Cursor -- it looks like a code editor with a file list on the left side

---

### Step 3 -- Open the Terminal Inside Cursor

The terminal is a plain text window where you talk to your computer by typing commands. It sounds scarier than it is -- you'll be using it constantly and it becomes second nature fast.

To open it in Cursor:

1. Click **Terminal** in the top menu bar
2. Select **New Terminal**
3. A panel opens at the bottom of the screen with a blinking cursor

You'll see a line that looks like this:
```
yourname@MacBook ~ %
```

This is called your **command prompt**. It tells you you're ready to type. The `~` symbol means you're currently in your home folder (your main Mac folder, named after your username).


---

### Step 4 -- Install Claude Code

Type the following command exactly and press **Enter**:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

What this does: it goes out to the internet, downloads Claude Code, and installs it on your computer automatically.

After it finishes, close the terminal (click the trash icon or X on the terminal panel) and open a fresh one via Terminal > New Terminal. This is necessary so your computer recognizes the newly installed program.

Check that it worked by typing:
```bash
claude --version
```
You should see a version number printed back. If you see "command not found," open a completely new terminal window and try again.


---

### Step 5 -- Log In

Type:
```bash
claude
```

The first time, it will ask you to log in with your Anthropic account. It will open a browser window for you to confirm. Once you're in, you're inside Claude Code and can start talking to it.


To exit Claude Code at any time, type `/quit` and press Enter.

---

## Part 2: Setting Your Default Model (Do This Once)

Claude Code can use different versions of Claude's brain -- called **models**. The most powerful one is called **Opus**. The default is usually Sonnet, which is faster but slightly less capable.

You can switch on the fly, but the easiest approach is to set Opus as your permanent default so you never have to think about it.

### The One-Time Setup (Recommended)

This adds a single line to a hidden settings file that tells your computer "always use Opus when I launch Claude Code." Type this in the terminal:

```bash
echo 'export ANTHROPIC_MODEL="opus"' >> ~/.zshrc && source ~/.zshrc
```

What that does: it adds the instruction to use Opus into your Mac's startup settings, so it applies every time you open a terminal. You only need to do this once.

To verify it worked, type:
```bash
echo $ANTHROPIC_MODEL
```
You should see `opus` printed back.

### Switching Models During a Session

If you're already inside Claude Code and want to switch models mid-conversation:

```
/model
```

This opens an interactive menu where you can choose between Opus, Sonnet, or Haiku using your arrow keys. Press Enter to confirm.

### The Three Models, Simply Explained

**Opus** -- the smartest, most thoughtful model. Best for complex planning, writing, and decision-making. Uses the most of your usage budget.

**Sonnet** -- a great middle ground. Fast and smart. Good for most everyday tasks. The default if you don't specify anything.

**Haiku** -- the quickest and cheapest. Good for simple, quick questions. Not great for anything complex.

**Tip:** There's also a special mode called **opusplan** -- it automatically uses Opus when planning and thinking, then switches to Sonnet when doing the actual writing or building. This saves your usage budget while still getting Opus's smart planning.

---

## Part 3: The Three Working Modes

This is one of the most important things to understand. Claude Code has three different modes that control how much it's allowed to do without asking you first. You switch between them by pressing **Shift + Tab** inside a running Claude Code session.


---

### Mode 1: Normal Mode (Default)
**What it is:** Claude asks your permission before doing almost anything -- creating files, running commands, making changes.

**When to use it:** When you're learning, when something is important and you want to review every step, or when you're working on something you don't fully understand yet.

**What you'll see:** Claude will pause frequently and ask "Can I do this?" You say yes or no.

---

### Mode 2: Auto-Accept Edits Mode
**What it is:** Claude automatically makes edits to files without stopping to ask you each time. It still asks for permission before running bigger system commands.

**How to turn it on:** Press **Shift + Tab** once inside Claude Code. You'll see a message that says `auto-accept edits on`.

**When to use it:** When you trust the work Claude is doing and don't want to click "yes" every few seconds on file edits. Good for when you've reviewed the plan and are happy with the direction.

**Think of it like:** Letting a contractor work in your house without watching every nail they hammer -- but you're still home if something big needs approval.

---

### Mode 3: Plan Mode
**What it is:** Claude can only look at files and think -- it cannot make any changes at all. It reads everything and gives you a detailed plan, but it won't touch anything until you switch modes.

**How to turn it on:** Press **Shift + Tab** twice. You'll see `plan mode on`.

**When to use it:** When you want Claude to analyze a situation and tell you what it would do BEFORE it does anything. Great for getting a second opinion, reviewing a complex problem, or starting a big task safely.

**Think of it like:** Asking an architect to walk through your house and describe what they'd renovate -- before any actual work begins.

---

### The Fourth Option: Dangerously Skip Permissions
**What it is:** Claude gets permission to do absolutely everything -- run commands, create files, delete files, make changes -- all without ever pausing to ask. No safety checks at all.

**How to use it:** You add a special flag when starting Claude Code:
```bash
claude --dangerously-skip-permissions
```

**Why it's named "dangerously":** Anthropic put that word in the name on purpose. This mode is powerful but genuinely risky. Claude could accidentally delete files you didn't want deleted, edit something it shouldn't have, or go further than you intended -- and it won't ask before doing any of it.

**When it's okay to use:** Only for very well-defined, low-stakes tasks where you've clearly told Claude exactly what to do and what not to touch. Many experienced users never use this mode at all.

**A good rule of thumb:** If you're not sure whether to use it, don't.

---

### Quick Mode Reference

| Mode | Shift+Tab presses | What Claude can do |
|------|-------------------|--------------------|
| Normal | 0 (default) | Everything, but asks you first |
| Auto-Accept Edits | 1 press | Makes file edits automatically; asks for bigger stuff |
| Plan Mode | 2 presses | Can only read and think -- no changes at all |
| Skip All Permissions | Launch flag | Does everything with no questions asked (use carefully) |

---

## Part 4: Understanding Your Folders

### How Folders Work in the Terminal

Folders on your Mac (what you see in Finder) are the same folders the terminal sees. The only difference is how you write their location.

In Finder you might click: **YourName > claudeprojects > my-project**

In the terminal, that same path is written as: `/Users/yourname/claudeprojects/my-project`


The `~` symbol is a shortcut that means "my home folder" (`/Users/yourname`). So you can also write the path above as `~/claudeprojects/my-project`.

---

### The `cd` Command: How to Move Around

`cd` stands for "change directory." A "directory" is just another word for a folder. This is how you navigate in the terminal.

**Go into a folder:**
```bash
cd claudeprojects
```

**Go straight to a project:**
```bash
cd ~/claudeprojects/my-project-name
```

**Go back up one level:**
```bash
cd ..
```
(Two dots means "go up one folder")

**Go all the way home from anywhere:**
```bash
cd ~
```

**See where you currently are:**
```bash
pwd
```
(Stands for "print working directory" -- it prints your location)

**See what's inside the current folder:**
```bash
ls
```

**See hidden files too:**
```bash
ls -a
```
(The `-a` means "all" -- including files that start with a dot, which are normally invisible)

---

### What the Hidden `.claude` Folder Is

Here's something that trips everyone up: your Mac hides files and folders that start with a dot (`.`). This is on purpose -- these are usually settings files that you're not supposed to accidentally mess with.

So when Claude Code installs itself, it creates a folder called `.claude` inside your home folder. You'll never see it in Finder normally. It's not missing -- it's just hidden.

Inside `.claude` is where Claude Code stores all its settings, your login credentials, and most importantly, a special instructions file called `CLAUDE.md` (explained in Part 10).

**To peek at your hidden files in Finder:** Open Finder, navigate to your home folder, and press **Cmd + Shift + .** (Command + Shift + Period). Hidden files and folders will appear grayed out. Press that shortcut again to hide them.

**To see hidden files in the terminal:** Type `ls -a` and you'll see everything, including files starting with `.`

---

### Recommended Folder Structure

Here's the full system we recommend, including all the special files covered in this guide:

```
yourname/                              <- your home folder, also written as ~
  .claude/                             <- hidden folder, created automatically
    CLAUDE.md                          <- your global rules for Claude (see Part 10)
    settings.json                      <- Claude Code's settings
  claudeprojects/                      <- your projects live here
    project-one/
      CLAUDE.md                        <- rules just for this project (optional)
      README.md                        <- what this project is
      SNAPSHOT.md                      <- save point you can return to
      tasks/
        todo.md                        <- Claude's step-by-step plan
        lessons.md                     <- mistakes learned, rules to prevent them
    project-two/
      README.md
      SNAPSHOT.md
      tasks/
        todo.md
        lessons.md
```

A companion visual for this is included as a separate file with this guide.

---

### Creating a New Project

```bash
cd ~/claudeprojects
mkdir my-new-project
cd my-new-project
```

`mkdir` means "make directory" -- it creates a new folder.

---

### Starting Claude Code in a Project

Always navigate into your project folder before starting Claude Code. This is how Claude knows which project it's working on -- it reads the files in whatever folder you launched it from.

```bash
cd ~/claudeprojects/my-project-name
claude
```

---

## Part 5: Terminal Shortcuts

The terminal doesn't behave exactly like a normal text box. Here are the shortcuts that save the most frustration:

| What you want to do | Shortcut |
|---------------------|----------|
| Erase everything you've typed on the current line | **Ctrl + U** |
| Erase from your cursor to the end of the line | **Ctrl + K** |
| Jump to the start of the line | **Ctrl + A** |
| Jump to the end of the line | **Ctrl + E** |
| Move backward one word at a time | **Option + Left Arrow** |
| Move forward one word at a time | **Option + Right Arrow** |
| Clear the whole screen | **Ctrl + L** (or type `clear`) |
| Repeat your last command | **Up Arrow** |
| Stop whatever is running | **Ctrl + C** |

So yes -- **Ctrl + U** clears the whole line. Very useful when you've made a typo halfway through a long command.

---

## Part 6: What Is a .md File?

A file ending in `.md` is a **Markdown file**. Markdown is a simple way to write text that can be formatted nicely -- with headings, bold text, lists, and so on.

You write it in plain text using a few simple symbols:

| You write | It looks like |
|-----------|---------------|
| `# Big Title` | A large heading |
| `## Smaller Heading` | A medium heading |
| `**bold text**` | **bold text** |
| `- list item` | a bullet point |

The beauty of Markdown is that even without any special software, the file is completely readable as plain text. But tools like Cursor, GitHub, or Notion will display it beautifully formatted.

You'll use `.md` files constantly for notes, instructions, and documentation in your projects.

---

## Part 7: What Is a README?

A `README.md` file is the welcome mat of any project. It lives in the main (root) folder of a project and is the first thing anyone reads to understand what the project is.

Claude Code reads your `README.md` automatically when you start a session. This means any instructions you write there will be followed every time -- no need to re-explain things from scratch.

Think of the README as a standing briefing note for your AI assistant.

**Other common `.md` files you'll see:**
- `CLAUDE.md` -- instructions specifically for Claude's behavior
- `SNAPSHOT.md` -- a save point you can return to after closing the terminal
- `tasks/todo.md` -- a step-by-step plan with checkboxes
- `tasks/lessons.md` -- a record of mistakes and rules to avoid repeating them
- `CHANGELOG.md` -- a log of what changed and when

---

## Part 8: How Tokens and Usage Limits Work

### What Is a Token?

When you send a message to Claude, every word uses up a small amount of computing resource called a **token**. A token is roughly 3/4 of a word. So "hello" is about one token, and a paragraph of text might be 100 tokens.

Think of tokens like text messages: each one uses a small amount of your plan's allowance.

### How Claude Pro Limits Work

Claude Pro gives you a generous monthly allowance. You'll almost never hit limits for normal use. But if you have extremely long conversations or send huge amounts of text repeatedly, you might see a message saying you've used up your current window.

To stay within limits:
- Start a fresh session for each new task instead of letting one conversation grow forever
- Use `/compact` to summarize a long session so Claude remembers the key points without storing every single word
- Opus uses more per message than Sonnet -- use Sonnet for quick simple tasks

### Context Window

This is related to tokens but slightly different. The "context window" is how much text Claude can hold in its working memory during a single conversation. Imagine it like short-term memory -- if a conversation gets very long, the oldest parts start to fade out.

When this happens, Claude might seem to "forget" earlier things you said. The fix is to either use `/compact` to compress the history, or start a new session and point Claude to the README and SNAPSHOT files to catch it up.

---

## Part 9: The Snapshot System

When you close the terminal, your Claude Code session ends. Any memory of what you discussed or built is gone. The snapshot system is how you make sure nothing is lost.

The idea is simple: you include instructions in your README telling Claude to save a summary file after every significant step. When you come back later, you show Claude that summary file and it picks up right where you left off.

### How to Set Up Your README

The easiest way is to drag this guide's PDF (or a screenshot of the template below) into the terminal in Cursor while you're inside your project folder, and tell Claude: *"create a README.md in this project using the example template, filled in with [a 2-3 sentence description of what you're building]."*

Claude will create the file with your project info and the snapshot instructions baked in.

### README Template (For Reference)

This is the template Claude will use. You can read through it to see what gets added to your project:

```markdown
# [Project Name]

## What This Project Is
[Write 2-3 sentences describing what this project does or what you're building]

## Current Status
[Claude will update this each session]

## Instructions for Claude
Please do the following after every significant edit or decision:
1. Update the "Current Status" section above with what was just done
2. Update or create a file called SNAPSHOT.md in this folder containing:
   - The date of this snapshot
   - A summary of what has been built or decided so far
   - What the next steps are
   - Any important decisions made and why

When starting a new session, always read README.md and SNAPSHOT.md first before doing anything.
```

When you come back after closing the terminal, just type:
> "Please read README.md and SNAPSHOT.md before we begin."

Claude will read them and be fully caught up.

---

## Part 10: CLAUDE.md -- Teaching Claude How to Behave

### What It Is

`CLAUDE.md` is the most powerful file in your whole setup. Claude Code reads it automatically at the start of every session -- before you say a single word. Whatever rules, preferences, or instructions you write in it become standing behavior.

There are two levels:

**Global** (`~/.claude/CLAUDE.md`) -- applies to every project on your entire computer. This is where you put your universal rules -- like the workflow rules below.

**Project-level** (`~/claudeprojects/my-project/CLAUDE.md`) -- applies only to that one project. Good for project-specific instructions or context.

---

### How to Set Up Your Global CLAUDE.md

The easiest way is to drag this guide's PDF (or a screenshot of the workflow rules below) into the terminal in Cursor and tell Claude: *"add this content to my global CLAUDE.md."* Claude will create the hidden `.claude` folder and the `CLAUDE.md` file for you if they don't already exist.

You can do the same with the Folder Structure Visual -- drag it into the terminal and tell Claude: *"add this folder structure to my global CLAUDE.md and follow it for all projects."*

These additions aren't mandatory, but they're really nice to have for quality control and organization.

---

### Workflow Rules (For Reference)

These are the workflow rules contained in the Workflow Orchestration screenshot. They're shown here so you can see exactly what gets added to your global `CLAUDE.md`:

```markdown
# Claude's Working Rules

## Workflow Orchestration

### 1. Plan Mode Default
- Enter plan mode for ANY non-trivial task (3+ steps or architectural decisions)
- If something goes sideways, STOP and re-plan immediately -- don't keep pushing
- Use plan mode for verification steps, not just building
- Write detailed specs upfront to reduce ambiguity

### 2. Subagent Strategy
- Use subagents liberally to keep the main context window clean
- Offload research, exploration, and parallel analysis to subagents
- For complex problems, throw more compute at it via subagents
- One task per subagent for focused execution

### 3. Self-Improvement Loop
- After ANY correction from the user: update `tasks/lessons.md` with the pattern
- Write rules for yourself that prevent the same mistake
- Ruthlessly iterate on these lessons until mistake rate drops
- Review lessons at session start for the relevant project

### 4. Verification Before Done
- Never mark a task complete without proving it works
- Diff behavior between main and your changes when relevant
- Ask yourself: "Would a staff engineer approve this?"
- Run tests, check logs, demonstrate correctness

### 5. Demand Elegance (Balanced)
- For non-trivial changes: pause and ask "is there a more elegant way?"
- If a fix feels hacky: "Knowing everything I know now, implement the elegant solution"
- Skip this for simple, obvious fixes -- don't over-engineer
- Challenge your own work before presenting it

### 6. Autonomous Bug Fixing
- When given a bug report: just fix it. Don't ask for hand-holding
- Point at logs, errors, failing tests -- then resolve them
- Zero context switching required from the user
- Go fix failing tests without being told how

## Task Management

1. **Plan First**: Write plan to `tasks/todo.md` with checkable items
2. **Verify Plan**: Check in before starting implementation
3. **Track Progress**: Mark items complete as you go
4. **Explain Changes**: High-level summary at each step
5. **Document Results**: Add review section to `tasks/todo.md`
6. **Capture Lessons**: Update `tasks/lessons.md` after corrections

## Core Principles

- **Simplicity First**: Make every change as simple as possible. Impact minimal code.
- **No Laziness**: Find root causes. No temporary fixes. Senior developer standards.
- **Minimal Impact**: Changes should only touch what's necessary. Avoid introducing bugs.
```

---

### The Full File Ecosystem

| File | Where it lives | What it's for | Who creates it |
|------|----------------|---------------|----------------|
| `~/.claude/CLAUDE.md` | Hidden global folder | Universal rules for all projects | You (once) |
| `CLAUDE.md` | Inside a project | Rules for just that project | You (per project) |
| `README.md` | Inside a project | What the project is + snapshot prompt | You + Claude updates |
| `SNAPSHOT.md` | Inside a project | Session save point | Claude auto-updates |
| `tasks/todo.md` | `tasks/` subfolder | Step-by-step plan with checkboxes | Claude creates + updates |
| `tasks/lessons.md` | `tasks/` subfolder | Mistake log + rules to avoid repeating | Claude updates after corrections |

---

## Quick Reference Card

| What you want | Command or shortcut |
|---------------|---------------------|
| Go to your projects folder | `cd ~/claudeprojects` |
| Go into a project | `cd project-name` |
| Go back up one folder | `cd ..` |
| Go home from anywhere | `cd ~` |
| See where you are | `pwd` |
| See files in current folder | `ls` |
| See hidden files too | `ls -a` |
| Create a new folder | `mkdir folder-name` |
| Create nested folders | `mkdir -p folder/subfolder` |
| Start Claude Code | `claude` |
| Start with Opus model | `claude --model opus` |
| Start with all permissions off (careful!) | `claude --dangerously-skip-permissions` |
| Exit Claude Code | `/quit` |
| Switch model during a session | `/model` |
| Compact a long session | `/compact` |
| Check current model | `/status` |
| Clear the terminal screen | `clear` |
| Erase current line | **Ctrl + U** |
| Switch modes (normal / auto-edit / plan) | **Shift + Tab** |
| Stop a running command | **Ctrl + C** |

---

## Troubleshooting

**"command not found: claude"** -- Close the terminal completely and open a new one. If it still doesn't work, run the install command from Part 1 again.

**Claude Code asks you to log in again** -- Completely normal if it's been a while. Just follow the browser prompts.

**Lost and don't know where you are** -- Type `pwd` to see your location. Type `cd ~` to go home and start fresh.

**Claude seems to have forgotten the project** -- Type `/compact` to compress the session, or start fresh and say "Please read README.md and SNAPSHOT.md before we begin."

**Hidden .claude folder isn't showing in Finder** -- Press **Cmd + Shift + .** while in Finder to reveal hidden files and folders.

**Default model keeps reverting to Sonnet** -- This is a known bug in Claude Code. The most reliable fix is the environment variable method from Part 2 (adding it to your `.zshrc` file).

---

## Part 11: Working from Your Phone

Once you have a project running on your computer, you can mirror it into the Claude app on your phone -- handy for picking up where you left off without being tied to your desk.

### How to Turn It On

Inside Claude Code (in your Cursor terminal), type:

```
/remote-control
```

That's it. Your project will automatically show up in the Claude app on your phone, and you can keep working on the same project from there.

---

## Part 12: Publishing Your Project

### Before You Publish

Your site will be public — anyone with the link can see it. Use your first name only. Don't include your phone number, home address, personal email, school name, or daily schedule.

### What Is Netlify?

Netlify is a free service that turns your project folder into a live website. You drag your folder onto a page, and it gives you a URL anyone can visit. No complicated setup, no public code repositories -- just drag, drop, done.

### Step 1 -- Create a Free Netlify Account

Go to [netlify.com](https://www.netlify.com) and click **Sign up**. You can sign up with an email address. The free plan is all you need. Creating an account means your site stays up permanently.

---

### Step 2 -- Go to Netlify Drop

Once logged in, go to **app.netlify.com/drop** in your browser. You'll see a large area that says to drag your folder here.

---

### Step 3 -- Deploy Your Project

1. Open Finder and find your project folder (the one with `index.html` inside)
2. Drag the entire folder onto the Netlify Drop page
3. Wait a few seconds -- Netlify will give you a live URL that looks like `random-name-12345.netlify.app`

That's your live website. Share that link with anyone and they can visit it in their browser.

---

### Updating Your Site Later

When you make changes and want to update the live version:

1. Log into Netlify and go to your site's dashboard
2. Click the **Deploys** tab
3. Drag your updated project folder onto the deploy area
4. Your site updates instantly at the same URL

---

*Guide written for macOS + Cursor (free). Last updated February 2026.*
