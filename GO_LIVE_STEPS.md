# Make the Meta app "Tech_2" Live (free)

App ID: 4126353520833440
Dashboard: https://developers.facebook.com/apps/4126353520833440/

## 0. Before you start
Open the dashboard and note the mode (top bar toggle, or "Publish" in the left menu).
- Already "Live"  -> stop; Development mode is not the cause, tell Claude.
- "Development"   -> continue.

## 1. Edit the two HTML pages
Replace YOUR_EMAIL_HERE with a contact email you are happy to make public. It appears in
index.html, privacy.html and data-deletion.html (footer on each, plus the contact sections).
In VS Code: Ctrl+Shift+H, search YOUR_EMAIL_HERE, "Replace All" within this folder.

## 2. Host them for free (GitHub Pages)
Use a NEW PUBLIC repo (GitHub Pages on private repos needs a paid plan, and this project's repo holds
your tokens/config paths, so do not make that one public).
1. github.com -> New repository -> name: `tech2-legal` -> Public -> Create.
2. Upload the 5 files from this folder (index.html, privacy.html, data-deletion.html, style.css, icon.png)
   with "Add file -> Upload files" -> Commit.
3. Repo Settings -> Pages -> Source: "Deploy from a branch" -> Branch: main, folder: / (root) -> Save.
4. After ~1 minute your URLs are:
   - Privacy Policy : https://<your-github-username>.github.io/tech2-legal/privacy.html
   - Data deletion  : https://<your-github-username>.github.io/tech2-legal/data-deletion.html
   Open both in a browser to confirm they load.

## 3. Fill in the app's basic settings
Dashboard -> App settings -> Basic:
- App icon (1024x1024)  : upload icon.png
- Privacy Policy URL    : the privacy.html URL above
- User data deletion    : the data-deletion.html URL above (choose "Data deletion instructions URL")
- Category              : Business and pages
- Contact email         : your email
- Save changes.

## 4. Go live
- Left menu has "Publish" -> open it, clear any checklist items, click "Go live" (bottom right).
- OR top bar toggle "App Mode: Development" -> switch to "Live".
- Business apps (no modes) -> tell Claude.
App Review is NOT needed: you only post to your own Page as the app admin.
If it asks for Business Verification, you can skip it unless the switch is blocked.

## 5. Verify
1. Your token keeps working (same app); do not regenerate it.
2. Open an old API-posted reel logged out / incognito:
   https://www.facebook.com/reel/1096214729705172/
   Meta says data from Development mode becomes visible after the switch.
3. Upload a new reel:  python main.py upload reel --to facebook
   and open it in incognito.

## 6. If it does not help
Switch back to Development (reversible) and tell Claude: the app mode screenshot and a hidden reel ID.
Other suspects: Page restriction (Professional dashboard), new/unverified Page.

## Cost
Free. No payment method is required at any step.
