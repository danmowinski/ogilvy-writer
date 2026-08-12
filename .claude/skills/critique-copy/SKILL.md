---
name: critique-copy
description: Critique a finished draft against Ogilvy's rules. Use after write-copy, or whenever the user asks for a copy review. Writes a revised draft into temporary-files/outputs/copy-vN(finished).md.
---

## Input / Output

- **Input:** `temporary-files/outputs/copy-vN.md`
- **Output:** Save the critique as `copy-vN(finished).md` in the `temporary-files/outputs` folder, matching the draft's number

## Step 1: Read

1. The highest-numbered `temporary-files/outputs/copy-vN.md`. 
2. `temporary-files/outputs/brief.md`
3. `context/writing-rules.md` 

## Step 2: Check the copy against the brief and writing rules 

Run a final pass of the copy against `context/writing-rules.md` and `temporary-files/outputs/brief.md`, changing anything if needed (only if needed). 

## Step 3: Remove AI tells

Change the following AI tells if they appear:

- Overuse of em dashes.
- Repetitive three-part lists.
- “It’s not X, it’s Y” constructions.
- Excessive signposting, such as “Here’s the key takeaway”.
- Frequent use of AI words such as “delve”, “leverage”, “robust” and “nuanced”.
- Excessively uniform sentence length and rhythm.
- Overly balanced “on the one hand, on the other hand” phrasing.
- Vague claims without concrete examples or evidence.

## Step 4: Save the finished draft

If the copy does not meet any of the checklist points, change it accordingly. Save the new version of the copy as `copy-vN(finished).md` in the `temporary-files/outputs` folder, matching the draft's number. 
