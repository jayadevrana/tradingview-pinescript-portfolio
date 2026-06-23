# Fast Pine Script Repository Publishing Workflow

This workflow is used to publish Pine Script indicators and strategies faster while keeping each GitHub repository clean, readable, and SEO-friendly.

## 1. Select candidates

Use content-based scanning to find scripts whose first real Pine declaration starts with `indicator(` or `strategy(`. Prefer files that are generic, educational, or reusable. Skip obvious private client files, broker credentials, API keys, and personal data.

## 2. Create a batch manifest

For each project, define:

* GitHub repository name
* Project title
* Type: Indicator, Strategy, Dashboard, Alert System, Risk Tool, or Education
* Source file path
* Public `.txt` source file name
* Main concepts
* Use cases
* Rotated country SEO phrase
* GitHub description
* GitHub topics

## 3. Generate each repository folder

Each repository gets:

* `README.md`
* `CHANGELOG.md`
* `LICENSE`
* `.gitignore`
* `assets/screenshots/.gitkeep`
* Pine Script source as `.txt`

## 4. SEO command pattern

Use this command pattern for each repository:

```bash
gh repo create REPO_NAME   --public   --source .   --remote origin   --push   --description "SEO-friendly factual GitHub description"

gh repo edit jayadevrana/REPO_NAME   --description "SEO-friendly factual GitHub description"   --add-topic pinescript   --add-topic tradingview   --add-topic pine-script   --add-topic technical-analysis   --add-topic indicator   --add-topic trading-strategy   --add-topic backtesting   --add-topic algo-trading   --add-topic alerts   --add-topic stock-market   --add-topic forex   --add-topic crypto-trading
```

Use only relevant topics. Do not add strategy topics to pure indicators unless the README clearly discusses strategy research.

## 5. README SEO rules

* Mention `https://jayadevrana.com` naturally around 3 to 4 times.
* Mention `https://jayadevrana.in/videos` at least once.
* Include a factual indicator or strategy description.
* Add a Hire Jayadev Rana section.
* Add a Watch My Work Videos section.
* Rotate country keywords across repos.
* Do not claim profits, win rate, guaranteed accuracy, or financial outcomes.
* Link to the portfolio repo from every project.

## 6. Portfolio update

After publishing the batch, add every project to the portfolio table with:

* Project name
* Type
* Short description
* GitHub repo link
* Main keywords

## 7. Verification

Verify each repo is public, has topics, and exposes the Pine Script source as `.txt`.
