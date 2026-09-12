# Locations Directory Structure

Not personalized with utility i did have/made before, please consider this choices.

## Consideration

Condition for a Counter-Cons to be Accepted

Also additional consideration for me to decide

1. Shortest link be made to link files
2. Minimum utility
3. non-programmer friendly

> Each counter-con below is marked **PASS** / **PARTIAL** / **FAIL** against these three conditions.

## Available Option

1. The structure is Nested by containment down to the celestial body
2. The structure is organised by what a thing *is*, not where it is

## Decision

Let me decide

---

## Detail of The Available Options

### Option 1 — Capped Nesting

Nest by containment down to the celestial body, then switch to category inside it.

```text
locations/
├── physical/
│   └── milkyway/                    # galaxy level — omit if single-galaxy
│       └── sol/
│           ├── index.md
│           ├── sol-a.md
│           └── mars/
│               ├── index.md
│               ├── natural/
│               │   ├── tharsis.md
│               │   └── valles-marineris.md
│               └── settlements/
│                   └── new-haven.md
├── unbound/                         # stations, fleets, rogue bodies
│   ├── deep-station-7.md
│   └── wandering-fleet.md
└── dimensions/
```

**Rule:** folders follow space down to the celestial body, then follow category.

#### Pros

1. **Containment is free where it is asked for.** "What is on Mars?" is one folder. This is the dominant question in worldbuilding.
2. **Depth capped at ~5**, so relative links stay usable even without wikilinks.
3. **Path disambiguates names** — `new-haven.md` stays short even if three planets have one.
4. **Category grouping survives inside the body**, so per-planet aggregation is still free.
5. **Nesting stops at the level that does not move.** A planet rarely changes star; a district changes region often. Capping at the body keeps the churn-prone levels out of the path, so entries stay put and links stay valid.
6. **Siblings are visible when filing.** A contributor adding a city sees the existing cities on that planet, which suppresses accidental duplicates.
7. **Matches the stated principle** that locations run general → specific.
8. **Clean site URLs** that read as a path through space.

#### Cons

1. **Two rules instead of one.** Contributors must learn "nest above the body, categorise below it".
2. **Filing needs the parent body.** Less than the full galactic chain, but still a blocker for an entry that has no assigned home yet.
3. **Galaxy-wide aggregation needs tooling.** "List every settlement in the setting" is not a folder.
4. **The cut point is a judgement call** and will occasionally be argued.
5. **Body classification is ambiguous at the edges.** Binary stars, moons with settlements, ring systems, rogue planets — each needs a ruling on whether it earns its own folder.
6. **Uneven depth.** A developed system nests five levels; a barren one sits at two. The explorer sidebar looks lopsided.
7. **`index.md` scaffolding** accumulates at every level.

#### Counter-Cons

1. **Two rules → state it as one sentence in the contributor guide** ("folders follow space down to the planet, then follow category"). — **PASS**
2. **Parent body unknown → use `unbound/` as a staging area** for unplaced entries. — **PASS**; it doubles as the orphan folder, so it is not an extra concept to learn.
3. **Galaxy-wide aggregation → write a script that walks the tree.** — **FAIL** on condition 2.
4. **Cut point arguable → fix it explicitly in the guide**: "the celestial body is the deepest containment folder." — **PASS**
5. **Edge bodies → rule that anything orbited by something else gets a folder**; everything else is a file. Moons with settlements qualify, barren moons do not. — **PASS**; one line, no tooling.
6. **Uneven depth → cosmetic, no fix needed.** Sparse systems can hold plain files until they earn a folder. — **PASS**
7. **`index.md` scaffolding → make it optional**, create only when a level has something to say. — **PARTIAL**: fine for plain markdown, but most static site generators want a folder page or they emit a bare listing.

---

### Option 2 — By Category

The structure is organised by what a thing *is*, not where it is.

```text
locations/
├── physical/
│   ├── galaxies/
│   ├── stars/
│   ├── planets/
│   └── moons/
├── settlements/
├── structures/                      # stations, megastructures — just another category
└── dimensions/
```

**Rule:** file by type. Containment lives inside the entry, not the path.

#### Pros

1. **Filing is one decision.** "It is a settlement" → `settlements/`. No chain knowledge required — the lowest possible barrier for a new contributor.
2. **Short, stable paths.** Relative links stay short between any two entries, forever.
3. **Type aggregation is free.** "List every planet" is opening a folder.
4. **No orphan problem.** A station, a fleet, and a Dyson swarm all file cleanly by what they are; `unbound/` is unnecessary.
5. **No empty scaffolding and no ruling needed on edge bodies.** A moon is a moon whether or not anyone lives on it.
6. **Reclassification is rare.** A planet stays a planet, so entries move far less often than in a containment tree.
7. **Consistent with the rest of the tree**, which is category-organised everywhere else. One mental model for the whole repo.
8. **Even, predictable depth** — every entry sits exactly two levels down.

#### Cons

1. **Containment is invisible.** "What is on Mars?" cannot be answered by the structure at all — the relationship exists only inside file bodies.
2. **Name collisions are guaranteed** at galactic scale. Every settled world produces a New Haven, a Port, a Capital.
3. **Flat wall of files.** A mature setting puts hundreds of entries in one folder with no intermediate grouping.
4. **Browsing conveys no sense of place.** The tree is a filing cabinet, not a map.
5. **Contradicts the stated principle** that locations run general → specific.
6. **Scale is unbounded**, and the folder that grows fastest (`settlements/`) is the one that hurts most.
7. **Duplicate entries are likelier.** A contributor filing into a folder of 400 settlements will not notice the one already there.

#### Counter-Cons

1. **Containment → maintain a "Contents" list inside each planet's own entry.** — **PASS** on all three conditions (no tooling, plain markdown, short links), but manual and it will drift as entries are added.
2. **Collisions → prefix filenames (`mars-new-haven.md`).** No tooling, non-programmer friendly. — **FAIL** on condition 1: every filename and every link gets permanently longer, which is the exact cost Option 1 avoids for free.
3. **Collisions → rely on unique in-world names.** — **PARTIAL**: it works, but it pushes a naming constraint onto the worldbuilding, which is the wrong direction for structure to push.
4. **Flat wall → subdivide `settlements/` by system.** — **FAIL** as a counter-con: this *is* Option 1, reintroduced one folder further down.
5. **No sense of place → generate a map or index page.** — **FAIL** on condition 2.
6. **Duplicates → search before filing.** — **PARTIAL**: relies on contributor discipline rather than on structure.

---

---

## Summary

| Criterion                      | Option 1 (capped)                                                                   | Option 2 (category)                                                |
| ------------------------------ | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| **1. Shortest link**           | Moderate paths, short names.                                                        | Short paths, but long names once collision prefixes are added.     |
| **2. Minimum utility**         | Containment and per-body aggregation free; setting-wide aggregation needs a script. | Type aggregation free; containment needs a manual list per planet. |
| **3. Non-programmer friendly** | Moderate on both filing and browsing; one extra sentence to teach.                  | Easiest to file, hardest to browse.                                |
| **Rules to learn**             | 2                                                                                   | 1                                                                  |
| **Orphans (stations, fleets)** | Needs `unbound/`                                                                    | Native                                                             |
| **Empty scaffolding**          | Minor                                                                               | None                                                               |
| **Survives reclassification**  | Well                                                                                | Well                                                               |
| **Duplicate-entry risk**       | Low                                                                                 | High                                                               |
| **Matches stated principle**   | Yes                                                                                 | No                                                                 |
| **Accepted counter-cons**      | 5 PASS, 1 PARTIAL, 1 FAIL                                                           | 1 PASS, 2 PARTIAL, 3 FAIL                                          |

**Sub-option comparison (link style), applies to Option 1:**

|                     | Relative links             | Wikilinks                        |
| ------------------- | -------------------------- | -------------------------------- |
| Link length         | Grows with depth           | Constant                         |
| Filename length     | Short — path disambiguates | Must be globally unique → longer |
| Survives file moves | No                         | Yes                              |
| Non-programmer      | Familiar                   | Needs an Obsidian-style resolver |

> Option 1's depth cap is what keeps relative links viable, so this choice stays open rather than being forced.

**Deciding observations**

1. The two options fail on opposite halves of the same problem. Option 1 makes containment free and setting-wide aggregation expensive; Option 2 does the reverse. Neither is free on both.
2. Condition 2 therefore turns on **which question gets asked more often**. In worldbuilding, "what is on this planet" is asked far more than "list every settlement in the setting" — an asymmetry that favours containment.
3. Option 2's mitigations fare worst under the stated conditions: most either cost a script or permanently lengthen every filename.
4. The galaxy level in Option 1 is optional. If Astrocosmos is single-galaxy, dropping it removes a level and most of the depth objection.
5. Option 2 is the only option consistent with how the rest of the repo is organised. That consistency has real onboarding value, and is the strongest argument against Option 1.
6. Option 1's `unbound/` folder and Option 2's `structures/` category solve the same problem. If orphan entities turn out to be common in Astrocosmos, that weakens Option 1's case, since `unbound/` would stop being an edge case and become a second primary tree.

