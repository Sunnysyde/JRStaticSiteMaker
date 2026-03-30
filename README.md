# JRStaticSiteMaker

This repository contains source prompts and guides for recreating and hosting a static site.

Repository URL: https://github.com/Sunnysyde/JRStaticSiteMaker

## LLM Quickstart Prompt

Copy and paste the prompt below into your LLM of choice:

```text
You are helping me work in the JRStaticSiteMaker repository.

Goal:
- Clone and understand this repository.
- Help me run or recreate the static site workflow from the included docs.

Instructions:
0) First ask me for my domain/site URL and confirm it before proceeding.

1) Clone the repo:
   git clone https://github.com/Sunnysyde/JRStaticSiteMaker.git
   cd JRStaticSiteMaker

2) Read these files first:
   - PROMPT_TO_RECREATE_SITE.md
   - WALKTHROUGH_RUN_LOCALLY.md
   - HOW_TO_HOST.md

3) Then give me:
   - A short summary of what this repo does.
   - Exact commands to run locally.
   - Any missing prerequisites I should install.
   - A step-by-step plan to recreate and host the site.

4) If anything is unclear, propose reasonable defaults and continue.

Start by listing the files and walking through the setup in order.
```

If you fork this project, replace the clone URL above with your fork URL.
