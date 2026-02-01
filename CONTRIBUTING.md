# Contributing Skills

We welcome contributions! Here's how to add a new skill.

## Creating a Skill

1. **Create a folder** in `skills/` with your skill name (lowercase, hyphens for spaces)
2. **Add `skill.md`** with the skill definition
3. **Test locally** by copying to `~/.claude/skills/`
4. **Submit a PR**

## Skill Format

Every skill needs a `skill.md` file:

```markdown
# Skill Name

Brief description of what this skill does.

## Usage

\`\`\`
/skill-name [arguments]
\`\`\`

## Inputs

- What the skill needs from the user

## Process

1. Step one
2. Step two
3. ...

## Output

What the skill produces
```

## Guidelines

- **Keep it focused** — One skill, one purpose
- **Be specific** — Clear instructions produce better results
- **Include examples** — Show how to invoke the skill
- **Document dependencies** — If it needs external tools, say so
- **Test it** — Make sure it works before submitting

## Good Skill Ideas

- Automating repetitive workflows
- Integrating with external APIs/tools
- Domain-specific tasks (crypto, devops, data, etc.)
- Project scaffolding and boilerplate

## PR Checklist

- [ ] Skill folder created in `skills/`
- [ ] `skill.md` follows the template
- [ ] Added to README.md table
- [ ] Tested locally
- [ ] No secrets or API keys hardcoded
