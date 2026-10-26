# Host the portfolio from the command line (Windows PowerShell)

Run all commands inside the portfolio folder (the one containing index.html).
Tip: in VS Code, right-click the folder > Open in Integrated Terminal.

## 0. Test locally first (do NOT just double-click index.html)
    py -m http.server 8000
Open http://localhost:8000 . Stop with Ctrl+C.
(Double-clicking opens it as file:// and the browser blocks the font.)

## Option A: Vercel (you already used it)  ~3 minutes
    node -v                 # need Node.js. If missing: https://nodejs.org (LTS)
    npm i -g vercel
    vercel login            # opens the browser, sign in with GitHub
    vercel                  # first run, answer the questions:
                            #   Set up and deploy? Y
                            #   Link to existing project? N
                            #   Project name: vanij-portfolio
                            #   Directory: ./   (press Enter)
                            #   Override settings? N
    vercel --prod           # live link: https://vanij-portfolio.vercel.app
To update later: edit files, run `vercel --prod` again.

## Option B: Netlify
    npm i -g netlify-cli
    netlify login
    netlify deploy          # choose: Create & configure a new site, publish directory: .
    netlify deploy --prod   # live link
To update later: `netlify deploy --prod`.

## Option C: GitHub Pages (updates with git push)
    winget install Git.Git
    winget install GitHub.cli        # then close and reopen the terminal
    gh auth login                    # GitHub.com > HTTPS > login with browser
    git init
    git add .
    git commit -m "Portfolio"
    git branch -M main
    gh repo create portfolio --public --source=. --remote=origin --push
    gh api -X POST repos/Vanij23/portfolio/pages -f "source[branch]=main" -f "source[path]=/"
Live in 1-2 minutes at https://vanij23.github.io/portfolio/
To update later:
    git add .
    git commit -m "Update"
    git push
Then hard refresh the site with Ctrl+Shift+R.

## Check after deploying
- Open the live link on your phone and your laptop.
- Avatar > Download my resume works.
- If the planet is still, avatar > Settings > Animations must be ON
  (Windows "Show animations" being off also freezes it).
