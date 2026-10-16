# Homeschool Evidence Recorder

A Progressive Web App (PWA) for homeschool families to record learning evidence with photos, check learning area coverage, and print tidy reports. It runs in any modern browser on Windows, Mac, Chromebook, iPad, iPhone and Android, installs to the home screen or desktop, and works offline.

**Privacy:** there is no account, no server and no tracking. Every record and photo is stored only in the family's own browser on their own device.

## What's in this folder

| File | Purpose |
|---|---|
| `index.html` | The whole app (layout, styles and code in one file) |
| `manifest.json` | Makes the app installable (name, colours, icons) |
| `sw.js` | Service worker: lets the app open and work offline |
| `icon-*.png` | App icons for home screens, desktops and browser tabs |

## Publish it free on GitHub Pages

1. Sign in to GitHub and create a **new public repository**, for example `evidence-recorder`.
2. On the repository page, click **Add file → Upload files**. Drag in every file from this folder (not the folder itself) and click **Commit changes**.
3. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose the `main` branch and the `/ (root)` folder, then click **Save**.
4. After a minute or two the page shows your address, for example
   `https://YOUR-USERNAME.github.io/evidence-recorder/`

That address is the app. Open it on a phone, tablet or computer to check it works.

> GitHub Pages requires a public repository on a free account. That is fine here: the code is public, but families' records never leave their own devices.

### Using your own domain (optional)

In **Settings → Pages → Custom domain** you can use something like `recorder.careeradvantage.training`. Add the CNAME record GitHub shows you at your domain provider.

## Linking it from LearnWorlds

Add a button or text link in a lesson pointing to your GitHub Pages address. Suggested lesson text:

> Open the Evidence Recorder, then install it so it works like a normal app:
> - **Windows, Mac or Chromebook (Chrome or Edge):** click the install icon at the right of the address bar.
> - **Android:** browser menu → *Add to Home screen*.
> - **iPhone or iPad:** open the link in **Safari**, tap **Share** → **Add to Home Screen**.

A 1–2 minute screen recording of installing and adding a first entry helps families most.

## Publishing an update

1. Upload the changed `index.html` (and any other changed files) to the repository.
2. Open `sw.js` and change the version on the first code line, for example `evidence-recorder-v1` to `evidence-recorder-v2`. Commit it.

Families receive the update the next time they open the app while online. Their records are not affected.

## Things to tell families

- **Photos, files and links.** Each entry can hold photos, attached files (PDF, Word, Excel, PowerPoint, audio, video, Scratch or Python projects, up to 50 MB each) and web links. For long videos, a link to YouTube, Google Drive or OneDrive keeps the app and its backups small.

- **Back up regularly.** Records live in the browser on one device. *Backup → Download backup* saves a single file with every entry and photo. Keep it in OneDrive, Google Drive or on a USB stick. The app reminds them if a backup is overdue.
- **Changing devices:** download a backup on the old device, then use *Restore from a backup* on the new one.
- **Don't clear browsing data** for the app's site, as this deletes records. Installing the app and using *Keep my records safe from clean-up* (in Backup) reduces the risk of the browser removing data automatically.
- **Reports:** *Report → Print or save as PDF*. Choose *Save as PDF* as the printer to keep a digital copy.
- **iPhone and iPad:** Safari may remove website data that hasn't been used for several weeks. Adding the app to the Home Screen avoids this, so recommend installing.

## Customising

- **Learning areas** are the eight WA Curriculum learning areas. To change them, edit the `AREAS` list near the top of the script in `index.html`.
- **Evidence types** are in the `TYPES` list just below it.
- **Colours and fonts** are set as variables at the top of the `<style>` block.

## Browser support

Current versions of Chrome, Edge, Safari (iOS 16.4+ / macOS) and Firefox. Installation as an app is supported in Chrome, Edge and Safari; Firefox runs it as a normal web page.
