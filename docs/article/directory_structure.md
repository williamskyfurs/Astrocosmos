
# My Fork/Version of Worldbuilding Directory Structure 

- This post here

<blockquote class="reddit-embed-bq" style="height:316px" data-embed-showusername="false" data-embed-height="316">
<a href="https://www.reddit.com/r/worldbuilding/comments/1r5yqwb/a_fantasy_worldbuilding_project_template_for/">A fantasy worldbuilding project template for structure and design</a><br>> by
<a href="https://www.reddit.com/user/After-Autumn/">u/After-Autumn</a>> in
<a href="https://www.reddit.com/r/worldbuilding/">worldbuilding</a>
</blockquote><script async="" src="https://embed.reddit.com/widgets.js" charset="UTF-8"></script>

- but when i apply this, it doesnt match my workflow
- SHORTLY, it is because ...

### Method of Explanation

- Definition used in this document
  - "current" is the reddit's, "proposed" is the mine
- this version is highly influenced by my current galactic-scale worldbuilding project
- I also see other structure
- im trying to be universal as far as i could
  - this also means by using omni-sciential perspective to the world
- my principes: structured by category, except location which are structured by from general to specific

## Level One (Root)

```text
.
├── Gameplay
│   ├── Mechanics & Systems
│   ├── Modules
│   ├── NPCs
│   └── Sessions
├── Infrastructure
│   ├── Change Log.md
│   ├── Contradictions & Retcons
│   ├── Dashboards
│   ├── Map of Content Indices
│   │   ├── Cosmology
│   │   ├── Nations
│   │   ├── Pantheons
│   │   └── Regional
│   ├── Media
│   │   └── Images
│   ├── References
│   │   └── Inspirational Material.md
│   ├── Style Guides
│   │   └── Tags
│   │       ├── Canon Dictionary.md
│   │       ├── Category Dictionary.md
│   │       ├── Misc. Tag Dictionary.md
│   │       ├── Status Dictionary.md
│   │       └── Tag Index.md
│   ├── Templates
│   ├── Themes & Guidelines
│   │   ├── Aesthetics.md
│   │   ├── Central Conflicts.md
│   │   ├── Ethos.md
│   │   ├── Morals.md
│   │   └── Tone.md
│   ├── TODO.md
│   └── Tools
│       ├── Obsidian.md
│       └── Tree View.md
├── Story
│   ├── Narratives
│   └── Plot Hooks
├── structure.txt
└── Worldbuilding
```

- `Gameplay` and `Story` are placed:
  - one level above the worldbuilding directory if the project is solely for worldbuilding;
  - at the root if they are considered part of the worldbuilding itself.
- Currently, there is no proposed changes to gameplay and story
- If the project is solely for worldbuilding, `Infrastructure` is renamed to `Docs`.
- `Media` inside `Infrastructure` is renamed to `Assets`. If the project is solely for worldbuilding, `Assets` is moved to the root.
- `Templates` is moved to the root if the project is solely for worldbuilding.
- `Worldbuilding` is renamed to `Content`.
  - because ...
- Project manifests and metadata files are placed at the root.
- If the project contains programming or scripting, a `Scripts` directory is placed at the root.


## The `Worldbuilding` folder directory

```text
Worldbuilding
├── Artifacts
│   ├── Cursed Items
│   ├── Fabled Armaments
│   ├── Lost Treasures
│   └── Relics
├── Astronomy & Cosmology
│   └── Celestial Bodies
│       ├── Comets & Asteroids
│       ├── Extrasolar
│       ├── Moons
│       ├── Planets
│       └── Stars
├── Culture
│   ├── Clothing & Fashion
│   ├── Craft
│   ├── Cuisine
│   ├── Customs
│   ├── Demographics
│   ├── Economics & Trade
│   │   ├── Currencies
│   │   ├── Industries
│   │   ├── Shops & Businesses
│   │   ├── Trade Practices
│   │   └── Trade Routes
│   ├── Entertainment
│   │   ├── Art
│   │   ├── Festivals & Events
│   │   ├── Music
│   │   └── Sports
│   ├── Folklore
│   ├── Languages
│   │   ├── Dead
│   │   └── Living
│   ├── Philosophy
│   ├── Professions
│   ├── Religion & Beliefs
│   │   ├── Creation Myths
│   │   ├── Cults
│   │   ├── Gods
│   │   ├── Orders & Sects
│   │   ├── Regional Variants
│   │   └── Sacred Texts
│   ├── Social Taboos
│   └── Thanatology
├── Divinity
│   └── Deities
│       ├── Major
│       └── Minor
├── Factions & Organizations
│   ├── Activist & Social Movements
│   ├── Criminal
│   └── Guilds & Groups
├── Geography
│   ├── Cartography
│   ├── Metaphysical
│   │   ├── Domains
│   │   ├── Planes
│   │   └── Pseudo Planes
│   └── Physical
│       ├── Creatures
│       ├── Fauna
│       ├── Flora
│       ├── Geology                             # grouped as `resource`
│       │   ├── Gemology
│       │   ├── Minerology
│       │   └── Structural
│       ├── Natural Phenomena
│       │   └── Weather
│       ├── Natural Resources                   # grouped as `resource`
│       └── Places
│           ├── Artificial
│           │   ├── Cities
│           │   ├── Dungeons
│           │   ├── Encampments
│           │   ├── Hamlets & Villages
│           │   ├── Kingdoms
│           │   ├── Ruins
│           │   └── Towns
│           └── Natural
│               ├── Biomes
│               ├── Continents
│               ├── Lakes & Wetlands
│               ├── Oceans
│               ├── Regions
│               └── Rivers
├── History
│   ├── Chronological
│   │   ├── Ages
│   │   ├── Eons
│   │   ├── Epochs
│   │   └── Eras
│   ├── Historiography
│   ├── Major Events
│   ├── Thematic                                
│   │   ├── Conflict & War                      
│   │   ├── Magical
│   │   ├── Plague
│   │   ├── Political
│   │   └── Religious
│   └── Timelines
├── _Ideas
│   ├── Abandoned Ideas
│   ├── Note Heap.md
│   ├── To Be Organized
│   └── Transient Notes.md
├── Magic
│   ├── Ambient
│   └── Systems
├── Notable Individuals                         
│   ├── Folk Heroes
│   ├── Leaders & Rulers
│   ├── Legendary Figures
│   ├── People of Interest
│   └── Villains
├── Politics                                    # confused
│   ├── Alliances & Agreements
│   ├── City States
│   ├── Conflicts & War
│   ├── Empires
│   ├── Kingdoms
│   └── Nations
├── Species 
│   ├── Core
│   ├── Extinct
│   ├── Hybrids
│   └── Variants
└── Technology
    ├── Agriculture
    ├── Alchemy
    ├── Armaments
    │   ├── Armor
    │   ├── Defensive Structures
    │   └── Weapons
    │       ├── Equipable
    │       └── War Machines
    ├── Calendars & Timekeeping
    ├── Communication
    ├── Health & Medicine
    │   ├── Pathology
    │   └── Remedies & Treatments
    │       └── Illicit
    ├── Knowledge Sources
    ├── Magitech
    ├── Production
    │   ├── Metallurgy
    │   └── Textiles
    └── Transportation
```


- technology are now explicitly include miscellaneous science
- therefore `Astronomy & Cosmology` be put under `technology`
  - im building a galactic world, thats why im confused

- the folder `Notable Individuals` be named into `characters` or `individuals` with the current children as proposed tags
  - Family tree file lives here

- the folder `species` are named into `creatures` 
  - this because plants are also "creations" 
  - with the current children as proposed tags, except `variants`, which will described in the entity's entry or as its children
  - the proposed children are `sapients`, `flora`, and `fauna`
  - This makes the current `creatures`, `flora`, and `fauna` which inside `Physical` folder be ommited cuz redundancy 

- `Calendars & Timekeeping` are named into `chronometry`, a uncommon word but short enough
- the current `history` are named into `chronology`
  - the proposed terms describe "*at any point of time*" rather than the current term which "*needs the  writer to be present in far future to write the whole history*"
  - `Major Events` are turned into its tags
  - the current `chronological` is named into `periods`
  - `Thematic` are named into `Events`
  - The `timeline` are changed into a file/folder that sort/structurize this even chronologically

- "Divinity" perfetly groups these below, because somehow deties and religion are related to divine things
  - Gods & Deities
  - Religions : the belief aspect of the current `religion and belief `

- a proposed folder "institutions" that groups these below 
  - the collective-individual aspect of the current `religion and belief`   
  - all children of the `faction and organization`
  - polities (some aspect of the folder `politic`)

- a proposed folder "robot" under technology
  - that groups (the models, "class", "blueprint" of )cyborg and android
  - "notable" robot character are placed under proposed `characters`

> [!NOTE] i think there is somekind of term that groups
>   - magic
>   - physics
>   - phenomena
>   - AND MAAYBE JUST MAYBE, 
>       - resource
>       - astronomy

The proposed structure will be explained at the nexxt section

## Tagging 

The current tagging created by the poster are:

>> I wanted to keep tagging to a minimum, so I created a library with a few dictionaries for groups that I find most beneficial for me.
>> They are divided into 3 main groups, and 1 supplementary group:
>>
>> 1. Category (for the type of content the document will contain)
>>
>> 2. Canon (for the degree to which this document's contents are fact or correct for the world)
>>
>> 3. Status (for the completeness or state of the idea as a whole)
>>
>> 4. Misc (for any additionally useful information)
>>
>> **Category** includes, but is not limited to: creature, deity, species, or system.
>> This group of tags is still growing and evolving for me as I create new content and as I pick through information from my past iteration of the project and import it over.
>>
>> **Canon** includes: soft, absolute, myth, contradicted, and obsolete.
>> This group will likely also change slightly going forward as needs require.
>> Most content is soft, being in active development.
>> Things that are fully formed and I accept as fact within the world are absolute.
>> Myth is for anything that is constructed by the peoples of the world, but is not actual fact (ex. a religion misinterpreting a divine being).
>>
>> **Status** follows a pretty static pipeline, but has some important offshoots.
>> Mostly content will follow: seed, draft, integrated, and potentially rework.
>> States that break this pipeline include: abandoned, experimental, locked, placeholder, and stale.
>> The three that should be explained are: experimental, used when an idea has the potential to have significant ramifications for existing content; locked, used when content is not likely to change unless something major shifts the project; and stale, used when revisiting content that was poorly written and I no longer remember what my intention or idea was behind the thought.
>>
>> **Misc** is for everything else I find useful for tagging.
>> Some tags include: needs-name, expand, research, needs-review, needs-linking, and sensitive-content.
>> All of which are pretty self explanatory.

- i want tagging to be exhaustive but minimum: detailed and informative enough
- inst some of the usage of category tags are redundant?

## The Proposed Structure, Re-Explained

### Locations




## Afterword

If the current structure has been made as a github repo template, i will fork it and change like my proposed, and could make a pull request