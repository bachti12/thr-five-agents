---
name: gpt-image-gen
description: "Call the OpenAI Images API (gpt-image-2) to generate a PNG from a text prompt. Returns a saved .png file at a caller-specified output path. Uses OPENAI_API_KEY from .env."
---

# gpt-image-gen Skill

## What It Does

Sends a prompt to `POST https://api.openai.com/v1/images/generations` using model `gpt-image-2`,
receives a base64-encoded PNG, and writes it to `<output-path>.png`.

## Prerequisites

`OPENAI_API_KEY` must be set in `.env` (or already exported in the shell).

## Parameters

| Parameter | Required | Default | Notes |
|-----------|----------|---------|-------|
| `prompt` | yes | — | The image generation prompt |
| `output-path` | yes | — | Destination file path without `.png` extension |
| `size` | no | `1024x1024` | `256x256`, `512x512`, or `1024x1024` |
| `quality` | no | `medium` | `low`, `medium`, or `high` |

---

## Usage — Primary (curl + jq)

```bash
source .env          # load OPENAI_API_KEY

curl -s -X POST "https://api.openai.com/v1/images/generations" \
  -H "Authorization: Bearer $OPENAI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-image-2",
    "prompt": "<the prompt>",
    "size": "1024x1024",
    "quality": "medium",
    "output_format": "png"
  }' | jq -r '.data[0].b64_json' | base64 --decode > <output-path>.png
```

---

## Usage — Fallback (Python; use when jq is not installed, e.g. Git Bash on Windows)

```bash
source .env

curl -s -X POST "https://api.openai.com/v1/images/generations" \
  -H "Authorization: Bearer $OPENAI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-image-2",
    "prompt": "<the prompt>",
    "size": "1024x1024",
    "quality": "medium",
    "output_format": "png"
  }' | python3 -c "
import sys, base64, json
data = json.load(sys.stdin)
sys.stdout.buffer.write(base64.b64decode(data['data'][0]['b64_json']))
" > <output-path>.png
```

---

## Verification

After the call, check the file exists and is non-empty:

```bash
test -s <output-path>.png && echo "OK" || echo "FAILED — empty or missing"
```

---

## Error Handling

| Symptom | Cause | Fix |
|---------|-------|-----|
| HTTP 401 | `OPENAI_API_KEY` missing or wrong | Check `.env` and re-run `source .env` |
| HTTP 400 | Prompt violates content policy | Rephrase the prompt |
| Empty output file | API returned error JSON instead of image | Run without the decode pipe to inspect raw JSON |
| `jq: command not found` | jq not installed | Use the Python fallback above |
