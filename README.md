# GERM PCB
## Intro
- This repository holds all the PCB information to allow for seamless syncing between team members who want to work on the design for GERM
- The design files for this project are built from **KiCAD**, and is what we will be using throughout the remainder of the project

## Design
- Design choices for this PCB are per the documentation in the [Drive](https://drive.google.com/drive/u/0/folders/1dtvyD7S52Tu-Nz1_2z5B_uvttlOJOdOd)

## Setup
1. Install **KiCAD 10** and **git**
2. Make sure you have been added to the `turtle-robotics` GitHub repo with write access, and that your SSH key is added to your GitHub account
3. Clone the repo:
   ```
   git clone git@github.com:turtle-robotics/GERM-PCB.git
   ```
   (Or use **File → Clone Project from Repository** in KiCAD and paste the repo link)
4. Open `GERM_PCB.kicad_pro` from the cloned folder in KiCAD
5. That's it!

## Pulling (getting the latest changes)
Nothing syncs automatically. Pull **before you start working**, and any time you want your teammates' latest changes:
```
cd GERM-PCB
git pull
```
Close KiCAD's editors before pulling if you have unsaved changes, then reopen the project afterwards so it loads the new files.

## Pushing (sharing your changes)
When you are done with a work session, save in KiCAD, close it, then run:
```
git add -A
git commit -m "short description of what you changed"
git push
```
If the push is rejected, someone pushed before you. Run `git pull --rebase` and then `git push` again.

## Avoiding conflicts
KiCAD files are text, but two people editing the same file at once cause merge conflicts that are painful to fix by hand.
- Agree on who is editing which file or schematic sheet before starting
- Always pull before you start and push when you stop
- Don't leave your changes unpushed for days

## What is (and isn't) in the repo
- Tracked: `.kicad_pro`, `.kicad_sch`, `.kicad_pcb`, `fp-lib-table`, and the custom footprint library folders (`*.pretty`)
- Ignored (see `.gitignore`): `.history/` (KiCAD's local backups), `*.lck` lock files, `*-backups/`, and `fp-info-cache`
