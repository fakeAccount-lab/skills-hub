# Skills Hub

A collection of Agent Skills for testing the skill-installer tool.

## Available Skills

### weather
Get current weather and forecasts for any location.

**Usage:** Use when the user asks about weather conditions, temperature, or forecasts for a specific location.

### git-helper
Common Git operations and workflows for version control.

**Usage:** Use when the user needs help with Git commands, branching, merging, or rebasing.

### code-review
Perform code reviews with focus on quality, best practices, and potential issues.

**Usage:** Use when the user asks to review code, check for best practices, or identify potential bugs.

## Installation

Use the skill-installer tool to install these skills:

```bash
skill-installer add fakeAccount-lab/skills-hub --agent openclaw
```

## Testing

To test skill-installer with these skills:

```bash
# List available skills
skill-installer list fakeAccount-lab/skills-hub

# Install all skills to OpenClaw
skill-installer add fakeAccount-lab/skills-hub --agent openclaw

# Install specific skill
skill-installer add fakeAccount-lab/skills-hub --agent openclaw --skill weather

# Install with copy mode
skill-installer add fakeAccount-lab/skills-hub --agent openclaw --mode copy
```

## Contributing

To add new skills to this hub:

1. Create a new directory under `skills/`
2. Add a `SKILL.md` file with proper YAML frontmatter
3. Commit and push to the repository

## License

MIT
