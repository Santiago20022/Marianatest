Explain one of the bugs in index.html as if teaching a junior developer.

The user specifies which bug: $ARGUMENTS (1, 2, or 3)

Structure your explanation:
1. **What the code does** — read the relevant lines and quote them
2. **What goes wrong** — describe the symptom the user would see in the browser
3. **Why it's wrong** — root cause in plain language
4. **The fix** — show the before/after diff

Keep it short: 4 sections, no fluff. Use a code block for the diff.
Agent({
  isolation: "worktree",  // ← trabaja en una copia, no en tu repo real
  prompt: "Intentá el refactor, si no funciona no importa"
})