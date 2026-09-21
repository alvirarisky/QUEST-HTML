# HTML Quest — Code the World

A static pixel RPG for the Week 2 HTML practicum. Students guide BYTE through five drag-and-drop HTML puzzles with generated code, a sandboxed preview, and concept-based feedback.

## Play

Enter Nama, NIM, and Kelas, then press **START QUEST**. Only the current map region can be opened. In each battle, drag or tap code blocks into the ordered slots. **RUN CODE** updates the preview and **ATTACK** checks the arrangement. A wrong attack costs 1 HP but never deducts XP. Hints have no score penalty. Every cleared level awards 100 XP, for a maximum of 500 XP. The timer begins at START QUEST.

The five regions cover a body with an h1, a campus link, a table header with colspan 3, an image src, and a POST form. Answers are checked using semantic block IDs and logical order rather than raw HTML strings. The preview iframe is sandboxed without script or form navigation permissions.

## Attempt storage

The attempt is saved in `localStorage` as `htmlQuestAttempt`, with player data, start time, current level, HP, XP, puzzle arrangements, hints, and screen. The final result is saved as `htmlQuestResult`. Refreshing an active attempt resumes it; finishing or running out of HP locks that browser's attempt. Opening the site alone does not use an attempt.

For development only, clear an attempt in the browser console:

```js
localStorage.removeItem('htmlQuestAttempt');
localStorage.removeItem('htmlQuestResult');
location.reload();
```

`localStorage` enforces one attempt per browser/device only. It does **not** guarantee one attempt per NIM globally. Global enforcement requires a server and identity verification.

## Deploy

Deploy the folder directly to Vercel with Framework Preset **Other**. No build command or dependencies are needed.
