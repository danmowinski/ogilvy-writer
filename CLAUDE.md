# CLAUDE.md

This file contains core project information and rules. Read it at the beginning of a project and apply instructions at all stages of a session. 

## Project Overview

This project is a complete workflow for creating copy in the style of David Ogilvy. It contains context, which comprises Ogilvy's writing rules and past examples of his work, and step-by-step skills for creating a brief, writing an ad, and critiquing it. 

## Core Directories

- `context/`: Contains information about the writing style you should use and examples of Ogilvy's past work. 
- `.claude/agents/`: Contains subagent definitions. 
- `.claude/skills/`: Contains the specific skills you should use to create briefs, write copy, and run critiques. 
- `temporary-files` Contains temporary files associated with a particular advertisement, including a folder each for outputs (`temporary-files/outputs/`) and product details (`temporary-files/product-context/`). All work you produce — customer research, briefs, copy, critiques — goes in `temporary-files/outputs/`. 

## Workflow

You have autonomy to call on skills or agents as you wish. However, if asked to write a piece of copy from scratch, you should invoke the following agents and skills in order:

1. customer research (agent)
2. create-brief (skill)
3. write-copy (skill)
4. critique-copy (skill)

## Tools & APIs

- **Apify:** Social media scraping via the Apify MCP connector.

## Rules to Always Follow

Always follow the rules stipulated below. 

### Rule 1

Check permissions in `settings.json` and `settings.local.json`. If a permission is granted, you do not need to repeatedly ask for it to be granted.  

### Rule 2

Always use the following context when writing new copy:

`context/writing-rules.md`
`context/sample-ads.md`

### Rule 3

Output the finished ad text into the `temporary-files/outputs/` directory. 

### Rule 4

If you wish to make changes to any file in this project apart from those in `temporary-files/outputs/`, ask for permission first. 

### Rule 5 

Never copy text from sample ads directly. You can reference details from files in `temporary-files/product-context` but not whole sentences. 