---
pretty_name: "Picture Perfect Portfolios (Articles, EN)"
license: cc-by-nc-4.0
language:
  - en
task_categories:
  - text-generation
  - question-answering
  - summarization
size_categories:
  - n<1K
tags:
  - finance
  - investing
  - portfolio-management
  - asset-allocation
  - quantitative-finance
  - systematic-investing
  - personal-finance
---

# Picture Perfect Portfolios (Articles, EN)

A dataset of long-form finance and investing articles from **Picture Perfect Portfolios** (Samuel & Audrey Media Network).

## What’s inside

- **448** article records
- Formats:
  - `picture-perfect-portfolios.jsonl` (canonical)
  - `picture-perfect-portfolios.jsonl.gz`
  - `picture-perfect-portfolios.csv` (same fields as JSONL, one row per record)
  - `picture-perfect-portfolios.csv.gz`

## Record fields

Each record includes:

- `id` — stable identifier
- `title` — article title
- `text` — full article text
- `lang` — `en`
- `domain` — source domain
- `source` — dataset slug (`picture-perfect-portfolios`)
- `content_hash` — integrity / dedupe hash of the text

See `DATA_DICTIONARY.md` and `SCHEMA.json` for full details.

## Loading examples

### Python (datasets)

```python
from datasets import load_dataset

ds = load_dataset("samuelandaudreymedianetwork/picture-perfect-portfolios", data_files="picture-perfect-portfolios.jsonl")["train"]
print(ds[0]["title"])
print(ds[0]["text"][:200])
```

### Python (jsonlines)

```python
import json

with open("picture-perfect-portfolios.jsonl", "r", encoding="utf-8") as f:
    first = json.loads(next(f))
print(first["title"])
```

## License

CC BY-NC 4.0 (cc-by-nc-4.0)

## Hugging Face

https://huggingface.co/datasets/samuelandaudreymedianetwork/picture-perfect-portfolios
