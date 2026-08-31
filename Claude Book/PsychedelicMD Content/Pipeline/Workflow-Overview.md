# Production Workflow Overview

## The Pipeline

```
Book Chapter / Raw Idea
        ↓
Script Adaptation (Claude)
        ↓
Script Review & Approval (Randy)
        ↓
Avatar Video Generation (HeyGen)
        ↓
Assembly: Captions + Music + Lower Thirds
        ↓
Review & Export
        ↓
Platform-Specific Cuts (YouTube / LinkedIn / Instagram)
        ↓
Publish + Log
```

---

## Manual Workflow (Start Here)

Before automating anything, run the first few videos manually to validate quality at each step.

1. Script adapted in Claude, saved to Video Scripts/
2. Open HeyGen, paste script, generate avatar video
3. Download video, import to Descript or CapCut
4. Add captions (auto-generated, review for accuracy)
5. Add background music (low, instrumental)
6. Export at platform specs (see Assets/Platform-Specs.md)
7. Upload and log in Published/Tracker.md

---

## Automated Workflow (Phase 2)

Once manual workflow is validated, connect via Make.com:

- **Trigger:** New script file saved to Video Scripts/ folder
- **Step 1:** HeyGen API call with script text → returns video file
- **Step 2:** Captions.ai or HeyGen built-in captions → returns captioned video
- **Step 3:** (Optional) Remotion template renders final branded video
- **Step 4:** Notification sent for review before publish

See Pipeline/Make-Automation.md for setup details once Phase 1 is complete.

---

## Quality Checks Before Publishing

- [ ] Avatar lip sync looks natural
- [ ] Captions are accurate (especially medical/plant medicine terminology)
- [ ] No claims that would attract regulatory attention
- [ ] Physician voice and credibility is present throughout
- [ ] Ends with a clear, simple idea — not a call to action for psychedelics
