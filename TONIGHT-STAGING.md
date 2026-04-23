# NKOTB Dinner Club — Tonight's Staging Checklist

Goal: get the local project folder ready so tomorrow's deploy takes under 10 minutes.

---

## Step 1 — Create the local folder

On your Windows machine, create a new folder:

```
D:\Projects\nkotb-dinner-club\
```

(Or wherever you keep your projects. The path doesn't matter.)

---

## Step 2 — Drop these files in

You'll get all of these from the file panel in this chat. The final folder structure should look EXACTLY like this:

```
nkotb-dinner-club/
├── index.html
├── netlify.toml
├── .gitignore
└── images/
    ├── boris-cutout.png
    ├── boris-yearbook.png
    ├── kim-mitchell-logo.png
    ├── klaus-cutout.png
    ├── klaus-yearbook.png
    ├── nadia-cutout.png
    ├── nadia-yearbook.png
    ├── olaf-cutout.png
    ├── olaf-yearbook.png
    ├── tallulah-cutout.png
    └── tallulah-yearbook.png
```

**Watch out for these gotchas:**
- `.gitignore` has a dot at the start. Windows may hide this by default. Turn on "show hidden files" in File Explorer if you can't see it.
- `images/` must be a **subfolder** containing the 11 PNG files. Not loose files in the root.
- The 5 `*-yearbook.png` files are used on the tour poster polaroids. The 5 `*-cutout.png` files (no background) are used on the character merch tees. All 11 are needed.

---

## Step 3 — Verify locally

Before going to bed, double-check it works by running a local server.

Open a Windows terminal (PowerShell or Command Prompt) in the project folder and run:

```
cd D:\Projects\nkotb-dinner-club
py -m http.server 8000
```

Then open `http://localhost:8000/` in your browser. You should see the full site — intro animation, wordmark, tour poster, merch gallery, brass placard, all of it. Test that the tee flips work.

If that loads correctly → you're ready for tomorrow. Leave the folder alone until then.

If it doesn't load → something's missing from the folder. Check the file list above against what's in your folder.

---

## Step 4 — Sanity checks (optional but recommended)

A few things to confirm now so they're not surprises tomorrow:

- [ ] I have a GitHub account I can log into
- [ ] I have a Netlify account I can log into
- [ ] Git is installed on my Windows machine (open a terminal and run `git --version` — should return a version number)
- [ ] I have admin rights on the machine in case I need to install anything

If any of those aren't true, fix them tonight so tomorrow isn't a scavenger hunt.

---

## Tomorrow's run-of-show (preview)

For reference, the whole tomorrow flow is:

1. Create a new GitHub repo named `nkotb-dinner-club` (don't initialize with a README)
2. In the project folder terminal: `git init`, `git add .`, `git commit -m "Initial commit"`, `git remote add origin <repo url>`, `git push -u origin main`
3. Go to Netlify → "Add new site" → "Import an existing project" → pick the `nkotb-dinner-club` repo
4. Netlify auto-detects the `netlify.toml`. Click "Deploy site."
5. ~30 seconds later: live at a random `.netlify.app` URL
6. Rename the site to `nkotb-dinner-club.netlify.app` in Netlify site settings

Done. I'll walk you through each step tomorrow.

---

## If you hit a wall tonight

Anything that's confusing or broken, just tell me the next time we chat. Don't spend more than 10 minutes stuck on any one step — stage what you can, and I'll help with the rest tomorrow.
