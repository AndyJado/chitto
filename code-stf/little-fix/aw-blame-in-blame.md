[# blame-blame](https://github.com/extrawurst/gitui/issues/1336)

**Describe the bug**
---
My working repo is `rust` from `rust-lang`, I go `<Shift-B>` on a file from another commit and I see some spinning, then spinning goes off and freeze, I can `esc` to go back.

**To Reproduce**
---
Steps to reproduce the behavior:
1. Go to 'Files'
2. 'Blame'
3. Inspect that commit 'l'
4. Go to 'Files'
5. `Blame`
6. freeze!

**Expected behavior**
---
Maybe forbid recursively blaming?

**Additional context**
---
If it's not a hurry, I'd like to fix it. I'm currently rather loaded
