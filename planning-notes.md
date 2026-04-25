# Planning Notes — Homepage Change Gate Checklist

## Purpose
Use this checklist as a mandatory **pre-edit gate** before making any homepage copy, wording, or style changes.

---

## One-Page Constraint Lock Checklist

### A) `home.html` Structure Contract (Do Not Change)
Before edits, verify these IDs and mount points exist and remain unchanged:

- [ ] `hero`
- [ ] `method`
- [ ] `revenue`
- [ ] `domains`
- [ ] `nameMeaning`
- [ ] `principles`
- [ ] `closingCta`
- [ ] `siteHeader`
- [ ] `siteFooter`

**Gate rule:**
- [ ] No renaming, removing, or repurposing any listed ID/mount point.
- [ ] No insertion that breaks anchor/link behavior or JS mounting expectations.

---

### B) `home.js` Render + Data Contract (Do Not Change)
Before edits, confirm render function names and expected JSON keys are preserved.

- [ ] Keep existing render function names unchanged.
- [ ] Keep expected JSON key names unchanged.
- [ ] If a rename/add/remove is needed, stop and plan a coordinated content-schema update first.

**Gate rule:**
- [ ] No unilateral schema drift between `home.js` and `data/home.json`.
- [ ] Any schema change requires explicit coordinated plan and follow-up updates.

---

### C) `site.js` Partial Loading Contract (Do Not Change)
Before edits, confirm partial loading contract remains intact.

- [ ] Header partial remains `header.html`.
- [ ] Footer partial remains `footer.html`.
- [ ] Load flow and mount behavior stay compatible with current contract.

**Gate rule:**
- [ ] No path/name/contract change for partials without coordinated architectural update.

---

## Pre-Edit Gate (Must Pass)
Run this gate before any copy/style edits:

- [ ] I validated all locked IDs/mount points in `home.html`.
- [ ] I validated all render functions and JSON keys in `home.js` remain unchanged.
- [ ] I validated `site.js` still targets `header.html` and `footer.html`.
- [ ] I confirmed no contract-level changes are included in this edit.

If any box cannot be checked, pause and create a coordinated change plan before proceeding.
