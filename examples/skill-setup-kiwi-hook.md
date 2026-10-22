---
name: setup-kiwi-hook
description: Connect a coding agent (Codex, Claude Code, others) to a routine webhook so the bot wakes on every turn end.
---
1. Create a routine with a webhook trigger. Keep the URL and key private.
2. On the machine that runs the agent, save them to ~/.kiwi-hook.env (chmod 600):
   KIWI_HOOK_URL=... and KIWI_HOOK_KEY=...
3. Install hooks/kiwi-hook-send somewhere on PATH.
4. Add the agent's turn-end hook (see README "Per-agent setup"). Back up the config first.
5. Send one test event and confirm the routine woke with HTTP 200.
6. Record what you changed (file names, not values) in the shared log repo.
