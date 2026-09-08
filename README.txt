## 1. Managing the Draft Branch (Step-by-Step)

### A. Create the Draft Branch (Do this ONCE at the start)
Run this command in the terminal to create and switch to your hidden sandbox branch:
```bash
git checkout -b draft-mode
```

### B. Daily Saving Strategy (Work PC ↔ MacBook Sync)
Whenever you finish editing at the end of the day and want to switch computers *without* making your rough draft public, run these commands:
```bash
git add .
git commit -m "Drafting updates"
git push origin draft-mode
```

### C. Moving to a New Device (Opening the Draft)
When you log into your Codespace on your other computer and need to ensure you are working inside your draft rather than the live site, run:
```bash
git checkout draft-mode
```

---

## 2. Publishing Live (When the site is 100% finished)
When your template changes look flawless in the preview panel and you are ready to update your public website (`sitediagnostics.github.io`), follow these step-by-step commands to merge your draft into the main line:

1. **Switch to your main branch:**
   ```bash
   git checkout main
   ```
2. **Pull down the draft changes you made:**
   ```bash
   git merge draft-mode
   ```
3. **Push to the live public internet:**
   ```bash
   git push origin main
   ```
4. **Switch back to draft mode for future edits:**
   ```bash
   git checkout draft-mode
   ```
