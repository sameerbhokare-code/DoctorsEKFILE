# EK FILE website

Static website for EK FILE. Plain HTML, no build step.

| File | What it is |
|---|---|
| `index.html` | Landing page: story, how it works, playable demo, business, roadmap, team, FAQ |
| `demo.html` | Full clinic demo: queue, patient summary, voice prescription, allergy check, print and WhatsApp preview |

`index.html` links to `demo.html`, so keep both files in the same folder.

## Run it locally

Double-click `index.html`, or serve the folder:

```bash
npx serve .
```

## Deploy

Any static host works. Upload this whole folder.

- **Netlify:** go to app.netlify.com/drop and drag this folder in.
- **Vercel:** run `npx vercel` in this folder and accept the defaults.
- **GitHub Pages:** push this folder to a repository, then Settings → Pages → deploy from the main branch, root folder.

## Notes

- Fonts load from Google Fonts and the QR code library from cdnjs, so the pages need internet for the full look.
- Voice input in the demo works in Chrome and Edge, and needs HTTPS (every host above gives you that) and microphone permission.
- Outside claude.ai, the demo uses its built-in reader to turn speech into a prescription. It works best in English. Press "Use sample consultation" for a reliable demo.
- Team email: in `index.html`, search for `var EMAIL = '';` and put the address between the quotes. The contact card then shows it with a Copy button.
- All patients, clinics and records are made up for demonstration.
