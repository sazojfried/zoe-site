# Resolving gallery.html merge conflicts

If GitHub reports conflicts when merging changes to `gallery.html`, combine both sides manually instead of choosing “ours” or “theirs.” The current expected state already contains the admin password unlock flow (`samandzoe`) and the drag-and-drop/upload tools.

## Quick steps
1. In the GitHub conflict editor, scroll through each highlighted block.
2. Keep the admin unlock UI (password input + “Unlock admin tools” button) and remove the old GitHub token/username fields.
3. Preserve the `ADMIN_PASSWORD = "samandzoe";` constant and the upload/reorder handlers.
4. Remove all conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`) so the HTML/JS is clean.
5. After resolving, click **Mark as resolved** and re-run the PR checks.

## Local resolution
```bash
# from repo root
git checkout work
# pull the latest main branch separately if needed
# git fetch origin main
# git merge origin/main
# edit gallery.html to combine both versions as above
npm test   # or any relevant checks if available
git add gallery.html
git commit -m "Resolve gallery.html merge conflicts"
```

The end result should match the current `gallery.html` in this branch, which includes the password-gated admin panel and GitHub upload logic.
