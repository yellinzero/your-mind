# Your Mind

A personal digital brain framework powered by Claude Code.

**[中文版](README.md)**

## Why This Project

Lately, I've been using AI intensively—learning tech, gathering information, and most importantly, doing parallel development with AI. During this process, I gradually became more and more lost.

Why? Because my brain couldn't keep up.

Too much information every day—tech articles, product ideas, learning notes, project thoughts—they rush in like a tide, then recede like a tide, leaving nothing behind.

So I decided to spend some time building a framework for myself. A place to organize my thoughts and let ideas settle. The way to learn thinking is to think often, right?

Then I thought: I should have my own digital brain, letting AI help me organize, think, and accumulate.

And that's how this project came to be.

## How It Works

I started with a private repo called `my-mind`, and had a blast with it:

**Use `/collect` to quickly gather information**—See a great article? Toss it in. AI will tag it and file it in the right document. I just collect, no need to organize.

**Use `/capture` to catch fleeting thoughts**—A random idea pops up? Just say it. AI quickly records and categorizes it.

**Use interactive mode to write life plans, daily notes, weekly reviews**—No more talking to myself. Claude Code guides me through these structured documents like a coach. Everything becomes easy.

## Two Moments That Made Me Open Source This

**The first moment**: While writing a daily note, I said "I want to build a fun product, make this today's goal." The AI automatically caught an idea I had previously recorded in my inspiration library, asking me: "Would you like to make this a target project?" Then it helped me analyze the feasibility of this inspiration through interactive dialogue.

I was stunned. This is exactly what I wanted.

**The second moment**: I suddenly realized this brain's structure is extensible. If you're a product manager, you can totally let Claude Code help you build a product management directory, skills, agents, and commands based on this structure. It understands the project framework well, letting your digital brain grow naturally.

You'll have a brain that's uniquely yours, one-of-a-kind, and increasingly powerful.

The only problem might be—tokens are really expensive. But worth it, right? 😆

## Acknowledgments

The `life-os` part of this project (including related skills, agents, etc.) was inspired by [obsidian-claude-pkm](https://github.com/ballred/obsidian-claude-pkm). Thanks to the original author for the pioneering work!

If this project helps you, feel free to give us both a Star ⭐

---

## Quick Start

### Prerequisites

- [Claude Code](https://claude.ai/code) - AI programming assistant
- [Obsidian](https://obsidian.md/) (optional) - I use it to manage notes, works great, but not required

### Installation

1. Clone or Fork this repo
2. Open the project directory with Claude Code
3. Start chatting with AI and explore your digital brain

## Directory Structure

```
your-mind/
├── life-os/           # Life planning system
│   ├── Daily Notes/   # Daily notes
│   ├── Goals/         # Goal management (5-year/yearly/monthly/weekly)
│   ├── Projects/      # Active projects
│   ├── Templates/     # Note templates
│   ├── Inbox/         # GTD inbox
│   └── Archives/      # Archive
├── output/            # Content output
│   ├── universal/     # Universal drafts
│   ├── quaily/        # Quaily Newsletter
│   ├── wechat/        # WeChat Official Account
│   └── ...            # Other platforms
├── inspiration/       # Inspiration capture
├── news/              # News collection
├── tech/              # Tech knowledge base
│   ├── problems/      # Problem cards
│   └── knowledge/     # Knowledge cards
├── docs/references/   # Reference docs
└── .claude/           # Claude Code config
    ├── commands/      # Custom commands
    ├── skills/        # Custom skills
    └── agents/        # Custom agents
```

## Core Features

### Commands

Commands are shortcuts to interact with your digital brain, triggered by typing a slash.

| Command | Purpose |
|---------|---------|
| `/daily` | Create today's daily note, Claude interactively guides your day planning |
| `/weekly` | Run weekly review process, reflect on last week and plan next |
| `/capture` | Quickly capture inspiration, record fleeting thoughts in one sentence |
| `/collect` | Collect information, drop a link in, AI auto-tags and archives |
| `/card` | Create tech card, record problem solutions or knowledge points |
| `/commit` | Commit changes to Git |
| `/onboard` | Load full context on first use |
| `/catchup` | Sync latest status, let AI know what you've been up to |

### Skills

Skills are Claude's professional capability modules, making it perform better in specific domains.

| Skill | Purpose |
|-------|---------|
| `life-os-file-ops` | Handle Obsidian file read/write standards, manage frontmatter and wiki-links |
| `daily-workflow` | Morning/noon/evening workflows, structure your day |
| `goal-tracking` | Goal progress tracking, calculate completion percentage, find stalled goals |
| `blog-assistant` | Generate article outlines based on topics or inspiration library content |
| `tech-reviewer` | Review tech cards, verify accuracy, find sources to validate |
| `skill-creator` | Help you create new skills, extend digital brain capabilities |

### Agents

Agents are AI assistants that can autonomously complete complex tasks.

| Agent | Purpose |
|-------|---------|
| `goal-aligner` | Analyze alignment between your daily activities and long-term goals, find deviations |
| `weekly-reviewer` | Guide weekly review process, ask you questions like a coach |
| `note-organizer` | Organize notes, fix broken links, merge duplicates, suggest connections |
| `inbox-processor` | Process inbox using GTD principles, categorize, clarify, organize |

## Custom Extensions

The beauty of this framework is that it can grow. You can let Claude Code help you extend any capability or module you need, and Claude Code will help you connect these contents together.

### Add New Command

Create a `command-name.md` file in the `.claude/commands/` directory.

### Add New Skill

Create a skill directory in `.claude/skills/` containing a `SKILL.md` file.

### Add New Agent

Create an `agent-name.md` file in the `.claude/agents/` directory.

**Tip**: You can simply tell Claude "help me create a skill for XXX" and it will do it.

### Multi-language Support

This project is currently in Chinese, but if you prefer another language, just let AI translate the entire project to your preferred language—it works just the same.

## Design Philosophy

1. **Input → Think → Output**: Complete knowledge flow loop
2. **AI Native**: Fully leverage Claude Code's capabilities, not just use AI as a search engine
3. **Structured but Flexible**: Provide framework without limiting freedom, let the brain grow naturally
4. **Traceable**: All decisions and progress are recorded, future you will thank present you

## Contact

Questions or ideas? Welcome to:

- Submit an [Issue](https://github.com/yellinzero/your-mind/issues)
- Find me on Twitter: [@yellin__](https://x.com/yellin__)

## License

[MIT License](LICENSE)

---

**Remember: What you need is your own digital brain. Don't let the framework limit you.**
