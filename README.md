# repo-exercise
#!/usr/bin/env bash
# This script walks through the full sequence of commands to complete the “repo-exercise” workflow.

# Step 2: Authenticate with GitHub CLI (interactive; you’ll be prompted to paste your token)
gh auth login

# Step 3: Clone your newly created repo
gh repo clone <vsvks>/repo-exercise

# Step 4: Enter your repo folder
cd repo-exercise

# Step 6: Copy the downloaded result.txt into this folder
# (Adjust the source path if your file is elsewhere)
cp ~/Downloads/result.txt .

# Step 7: Show status (should list result.txt as “untracked”)
git status

# Step 9: Stage the file
git add result.txt

# Step 10: Verify it’s staged
git status

# Step 12: Commit with the required message
git commit -m "Successful exercise"

# Step 14: Push your commit up to GitHub
git push origin main

# Done: You can now visit:
# https://github.com/<vsvks>/repo-exercise
# to verify that result.txt appears in the repo.
