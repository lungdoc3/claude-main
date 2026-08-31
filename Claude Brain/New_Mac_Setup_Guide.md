# Quadriune Brain Dev Machine — New Mac Setup Guide
*Step-by-step environment recreation. Follow in order.*

---

## Phase 1: App and Account

**Step 1 — Install Claude desktop app**
Download and install Claude for Mac on the new machine. Same process as the current Mac.

**Step 2 — Sign in with the same account**
Use the same login (the.psychedelic.md@gmail.com). Your account carries over subscriptions and app settings — including global custom instructions if they sync, and connected Cowork folders will need to be re-added manually (see Phase 4).

---

## Phase 2: Folder Structure

Create these three folders somewhere permanent and memorable on the new Mac. Recommendation: root of home directory (`/Users/[you]/`) to mirror the current machine exactly.

```
~/Claude Brain/
~/Claude Shorts/
~/Claude Book/          (optional — add only if doing book work on this machine)
```

**Do not rename them.** Claude's memory and session briefings reference these exact names.

### Claude Brain — internal structure to recreate

```
Claude Brain/
├── _START_HERE.md              ← Claude reads this first each session
├── Manifesto.md                ← philosophical + theoretical foundation
├── Lab_Notebook.md             ← chronological working notes
├── Del_Briefing.md             ← Del's technical briefing document
├── Memory_Seed.md              ← NEW: bootstrap file for Claude on fresh machines
├── Domain_Specs/
│   └── README.md               ← next major writing task
└── (Del's new material — add subfolders here as needed after he shares)
```

### Claude Shorts — internal structure to recreate

```
Claude Shorts/
├── _START_HERE.md
├── Character_Bible.md
├── HeadQuarters_Character_Bible.md
├── HeadQuarters_Production_Copy.md
├── HeadQuarters_Voice_Audition_Scripts.md
├── HeadQuarters_Voice_Generation_Prompts.md
├── HeadQuarters_VoiceBinding_Monologues.md
├── HeadQuarters_Midjourney_Prompts.md
├── Narrator_Intro_Scripts.md
├── Narrator_FullReel_Script.md
├── Scene_01_TheMeeting.md
└── [all media files: .png, .mp3, .mp4, .mov]
```

---

## Phase 3: Transfer Files

### Option A — AirDrop (simplest for folders under ~1 GB)
AirDrop each folder from current Mac to new Mac. For Claude Shorts this will take a few minutes due to the media files.

### Option B — iCloud Drive
Move the folders into iCloud Drive on the current Mac, wait for sync, access from new Mac. Rename back to original paths after. Clean but slower.

### Option C — External drive / USB
Copy folders to drive, plug into new Mac, drag to home directory.

**What to transfer:**
- `~/Claude Brain/` — all files
- `~/Claude Shorts/` — all files including media (largest)
- `~/Claude Book/` — all files, if this machine will do book work

---

## Phase 4: Connect Folders in Cowork

On the new Mac, open Cowork mode in Claude. Connect each folder:

1. In the Cowork interface, look for the folder/connect icon (left panel or Settings)
2. Add `Claude Brain` — Claude will ask for permission, approve it
3. Add `Claude Shorts`
4. Add `Claude Book` if needed

Claude needs these connected to read and write your project files. Without them, it can only work in the temporary outputs folder.

---

## Phase 5: Global Custom Instructions

Check whether your global custom instructions transferred automatically (some account settings sync, some don't).

Go to **Settings > Custom Instructions** (or equivalent in the app). They should read:

```
At the start of each new session, read the file _START_HERE.md located 
in the relevant project folder (Claude Brain, Claude Shorts, or Claude Book) 
before responding.

For any writing or content production in the Claude Book project, 
follow VOICE-REFERENCE-Foundation2.md and use the critic protocol in 
critic.md, both located in the Claude Book folder.
```

If they're blank or show the old "Med Expert" version, paste the above in manually.

---

## Phase 6: Memory

Memory files are stored locally inside `~/Library/Application Support/Claude/...` and are machine-specific. They will NOT transfer automatically unless you use Migration Assistant.

### Option A — Migration Assistant (transfers everything)
If you haven't set up the new Mac yet, run Migration Assistant from the current Mac. This moves ~/Library/Application Support/Claude/ including memory. Cleanest option.

### Option B — Fresh memory + seed file (manual, recommended otherwise)
Open a new session on the new Mac, tell Claude: "Read Memory_Seed.md in Claude Brain and rebuild memory from it."

The Memory_Seed.md file (see Phase 2 above) contains everything Claude needs to reconstruct working context for both projects.

---

## Phase 7: Del's New Material

Once the above is complete, add Del's harness architecture and related files into Claude Brain. Suggested subfolder:

```
Claude Brain/
└── Del_Harness/
    ├── [architecture docs]
    ├── [code or specs]
    └── [whatever he provided]
```

Exact structure will depend on what he shared. We'll organize it together after you share the materials.

**Note on "CLAUDE APEX":** If Del is using this term to describe a specific folder or layer in the harness architecture, we'll wire it into the structure above once you share his docs. Hold on naming that folder until we see how it fits.

---

## Phase 8: Verify

Start a fresh session on the new Mac and say: "Run startup check." Claude should:
- Confirm it can read `_START_HERE.md` in Claude Brain
- Confirm it can read `Lab_Notebook.md` and `Del_Briefing.md`
- Report what's in memory (from seed or migration)

If any step fails, troubleshoot the folder connection first — that's the most likely point of failure.

---

*Created: June 2026*
*For: Randy Evans — Quadriune Brain dev machine setup*
