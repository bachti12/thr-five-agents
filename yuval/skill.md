# yuval — Skill Pointer Doc

This file is for humans navigating the repo. It is **not** parsed by Claude Code.

## Skill used by Yuval

| Location | Purpose |
|----------|---------|
| [`.claude/skills/gpt-image-gen/SKILL.md`](../.claude/skills/gpt-image-gen/SKILL.md) | Calls the OpenAI Images API and saves the result as a PNG |

## How to call the skill manually

See [`SKILL.md`](../.claude/skills/gpt-image-gen/SKILL.md) for the full curl + Python fallback commands.

Quick reference:

```bash
source .env
curl -s -X POST "https://api.openai.com/v1/images/generations" \
  -H "Authorization: Bearer $OPENAI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"gpt-image-2","prompt":"your prompt here","size":"1024x1024","quality":"medium","output_format":"png"}' \
  | python3 -c "import sys,base64,json; d=json.load(sys.stdin); sys.stdout.buffer.write(base64.b64decode(d['data'][0]['b64_json']))" \
  > yuval/outputs/test.png
```
