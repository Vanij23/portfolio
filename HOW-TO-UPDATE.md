# How to update your portfolio

## Files
- index.html            the whole website (text, styles, code)
- Vanij_Raut_Resume.pdf  your resume (the Download buttons use this exact name)
- assets/avatar.jpg      your small profile photo (square, about 200x200)
- assets/fonts/Inter.woff2  the font (do not delete)

## 1. Edit
1. Open the folder in VS Code (File > Open Folder).
2. Open index.html and press Ctrl+F to find the text you want to change.
3. Change the words between the tags, e.g. <p>old text</p> -> <p>new text</p>.
4. To preview, right-click index.html > Open with Live Server (or just double-click it).
   Note: fonts may only load fully on a real server, so check the live link too.

## Common changes
- Resume: replace Vanij_Raut_Resume.pdf with the new file, SAME NAME.
- Profile photo: replace assets/avatar.jpg with a square photo, SAME NAME.
- Email: search rautvanij@gmail.com and replace everywhere (about 3 places).
- Colours: top of the <style> section. The :root block is dark mode, the [data-theme=light]
  block right below it is light mode. --orange is the accent colour.
- Theme and accent can also be changed live from the avatar panel (top right) > Settings.
- New project: find  <article class="card">  copy the whole block up to  </article>,
  paste it after the last project card and edit the text.
- Project links: inside a project block add
  <a class="arrow" href="https://YOUR-LINK" target="_blank" rel="noopener">View live<i></i></a>
- Skills: find the skill-group blocks and add <li>New skill</li> inside the <ul class="tags">.

## 2. Publish the update
### Netlify drag-and-drop
1. app.netlify.com > your site > Deploys tab.
2. Drag the whole updated folder onto the "Drag and drop" area. Done, same link.

### GitHub Pages
1. Open your repo on github.com.
2. Click the file (e.g. index.html) > pencil icon > edit > Commit changes.
   For new/replaced files: Add file > Upload files > drag them in > Commit.
3. Wait 1-2 minutes, then hard refresh the site (Ctrl+Shift+R).

### Optional: auto-update (best)
Connect the GitHub repo to Netlify (Add new site > Import from Git). After that,
every change you commit to GitHub updates the site by itself.
