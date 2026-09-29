# my-iterative-knowing-skills

Personal collection of [opencode](https://opencode.ai) agent skills that I build
up iteratively as I learn.

## Skills

### english-coach

Corrects my English and then solves the problem, so I can learn the natural
way to phrase things. Only triggers when I write in English — if I switch to
Chinese, it responds natively with no correction.

Every correction block has three parts:

- **Corrected** — my sentence, fixed
- **Notes** — what was wrong, one line each
- **Native** — how a native speaker would actually say it, plus 1-2
  alternatives and when each fits

## Install

Clone and symlink the skills you want into opencode's skill directory:

```bash
git clone https://github.com/donald-laird/my-iterative-knowing-skills.git
mkdir -p ~/.agents/skills
ln -s "$PWD/my-iterative-knowing-skills/skills/english-coach" ~/.agents/skills/english-coach
```

Or copy the directory instead of symlinking:

```bash
cp -r my-iterative-knowing-skills/skills/english-coach ~/.agents/skills/
```

`~/.agents/skills/` is auto-scanned by opencode. Alternatively, point opencode
at this repo with `skills.paths` in `opencode.json`:

```json
{
  "skills": { "paths": ["~/Work/my-iterative-knowing-skills/skills"] }
}
```

Restart opencode after installing — skills are loaded at startup and are not
hot-reloaded.
