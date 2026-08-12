---
name: create-brief
description: Create the copy brief that precedes an advertisement. Use before write-copy.
---

# Create a copy brief

## Input / Output

- **Input:** `temporary-files/outputs/<product-slug>-research.md`
- **Output:** Save the brief as `brief.md` in the `temporary-files/outputs` folder

---

## Step 1: Understand Product Details 

Review all product details  in `temporary-files/product-context` folder.

## Step 2: Review Customer Research 

Review research in the `temporary-files/outputs/<product-slug>-research.md` file.

## Step 3 : Create a New Brief

Create a file titled `brief.md` in the `temporary-files/outputs` using the template in `.claude/skills/create-brief/assets/brief-template.md` and fill out the relevant entries using information from files specified in steps 1 and 2. 
