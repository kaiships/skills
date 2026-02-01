# Claude Code Skills

A collection of open-source skills for [Claude Code](https://claude.ai/claude-code).

Skills are reusable prompts that extend Claude Code's capabilities. Invoke them with `/skill-name` in your conversation.

## Installation

Copy any skill folder to `~/.claude/skills/`:

```bash
# Clone the repo
git clone https://github.com/kaiships/claude-skills
cd claude-skills

# Copy a specific skill
cp -r skills/porto ~/.claude/skills/

# Or copy all skills
cp -r skills/* ~/.claude/skills/
```

## Available Skills

| Skill | Description |
|-------|-------------|
| [porto](/skills/porto) | Manage Porto account abstraction - upgrade wallets, send with stablecoin gas |

## Skill Structure

Each skill is a folder containing a `skill.md` file:

```
skills/
└── porto/
    └── skill.md
```

## Creating Skills

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to create and submit new skills.

Basic template:

```markdown
# Skill Name

Brief description.

## Usage

\`\`\`
/skill-name [arguments]
\`\`\`

## Process

1. What the skill does step by step

## Output

What it produces
```

## License

MIT
