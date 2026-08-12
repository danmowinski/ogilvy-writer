---
name: write-copy
description: Write the advertisement itself from an approved brief. Use after create-brief and before critique-copy. Produces headline options and full body copy into temporary-files/outputs/copy-vN.md.
---

# Write copy

## Input / Output

- **Input:** `temporary-files/outputs/brief.md`
- **Output:** Save the copy as `copy-vN.md` in the `temporary-files/outputs` folder, where N is the next unused number

---

## Step 1: Read your materials

In this order:

1. `temporary-files/outputs/brief.md`
2. `context/writing-rules.md` — the numbered rules
3. `context/sample-ads.md`
4. `.claude/skills/write-copy/assets/templates.md`

If `brief.md` does not exist, run create-brief first.

## Step 2: Write twenty headlines

Generate twenty headlines and select one. 

## Step 3: Write the body

Pick one structure from `templates.md` and write out the copy in full. Keep `context/writing-rules.md` and `context/sample-ads.md` in mind. 

## Step 4: Save

Write to `temporary-files/outputs/copy-vN.md`, where N is the next unused number: Include the twenty headlines (specify your chosen one) and all of the elements included in the template. 

## Rules

- Never lift phrasing from `context/sample-ads.md`, per Rule 5 in `Claude.md`. Borrow the method, not the words.

- Any words placed inside quotation marks must appear verbatim in the customer research file or in `temporary-files/product-context/`. Never invent a quotation. Where a source reports what someone said without giving their words, write it as reported speech instead. You can eschew rule 5 that  forbids reproducing whole sentences from `temporary-files/product-context/` for quotes. 

- Every figure must carry the qualifier its source carries. If the source says "up to 18%", the copy says "up to 18%". If a measurement is taken under a named test condition, say which.
