# 📝 Submission Guidelines

This folder is where you place your submission files 

---

## Required Files

### 1. `predictions.csv`

Your model predictions must follow this format:

```csv
id,y_pred
0,1
1,0
2,1
...
```

* `id` — integer index of the test function
* `y_pred` — 1 if vulnerable, 0 if non-vulnerable

---

### 2. `metadata.json`

Contains metadata about your submission:

```json
{
  "team": "example_team",
  "run_id": "example_run_id",
  "type": "human",   // must be "human", "llm-only", or "human+llm"
  "model": "GAT",
  "notes": "Additional notes"
}
```

---

## How to Submit

1. Encrypt your `predictions.csv` using: ``` python  extra/encrypt.py predictions.csv ```
2. Place your `predictions.csv.enc` and `metadata.json` in this `submissions/` folder
3. Commit and push your changes to your forked repository
4. Create a **Pull Request** to the main repository
5. GitHub Actions will automatically evaluate your submission
6. Your results will be posted as a comment and added to the leaderboard
