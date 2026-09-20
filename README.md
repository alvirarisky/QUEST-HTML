# HTML Quest — Code the World

A static pixel RPG for the Week 2 HTML practicum. Students guide BYTE through five HTML challenges, using a code editor, sandboxed preview, and requirement-based feedback.

## Play

Enter Nama, NIM, and Kelas, then press **START QUEST**. Only the current map region can be opened. In each battle, **RUN CODE** updates the preview and **ATTACK** checks the answer. A wrong attack costs 1 HP. A hint reduces that level's reward from 100 to 75 XP. The game starts with 3 HP; the maximum score is 500 XP. The timer begins at START QUEST.

The five regions cover a body with an h1, a campus link, a table header with colspan 3, an image src, and a POST form. Answers are parsed as HTML and checked by requirement. The preview iframe is sandboxed without script or form navigation permissions.

## Attempt storage

The attempt is saved in `localStorage` as `htmlQuestAttempt`, with player data, start time, current level, HP, XP, editor drafts, hints, and screen. The final result is saved as `htmlQuestResult`. Refreshing an active attempt resumes it; finishing or running out of HP locks that browser's attempt. Opening the site alone does not use an attempt.

For development only, clear an attempt in the browser console:

```js
localStorage.removeItem('htmlQuestAttempt');
localStorage.removeItem('htmlQuestResult');
location.reload();
```

`localStorage` enforces one attempt per browser/device only. It does **not** guarantee one attempt per NIM globally. Global enforcement requires a server and identity verification.

## Deploy

Deploy the folder directly to Vercel with Framework Preset **Other**. No build command or dependencies are needed.
