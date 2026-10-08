# SkinSeoul AI Influencer Factory

## Persona Builder (`persona-builder.html`)

One offline form that collects everything needed to create an AI influencer, then builds **one clean prompt** to paste into ChatGPT (with your reference images attached).

- Not connected to any AI. No API calls, no keys, no logins.
- Everything stays on your computer.

### How to open it
1. Download `persona-builder.html`.
2. Double-click it. It opens in your browser (Chrome works best).
3. Choose **Start blank**, **Load Remi preset** or **Open saved file**.

### How to use it
1. Fill in sections **A–G**. The left menu shows ✓ done · ! required missing · ○ not started.
2. Hover the **?** next to any field to see what it means plus Remi's example.
3. Turn on **Let AI suggest** on a field if you want ChatGPT to propose options for it.
4. Go to **H. Review & Generate**. It stays locked until every required field is done.
5. Copy the prompt, attach the listed images in ChatGPT, then send.
6. Pick from ChatGPT's suggestions, update the form and click **💾 Save file**.

### Saving
- Your work autosaves in the browser you're using (use **Continue where you left off** on the start screen).
- **💾 Save file** downloads `persona-<name>.json`: the real copy to keep and share with the team. Open it again with **Open saved file**.

### For developers (later)
Each persona is one JSON object: `schema`, `createdAt`, `updatedAt`, `aiSuggest` (field ids ChatGPT should fill), then one object per section: `identity`, `appearance`, `personality`, `lifestyle`, `style`, `content`, `rules`. Images are stored only as file names plus a small thumbnail. The form definition lives in the `SECTIONS` array in the file.
