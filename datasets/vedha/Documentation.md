
# Dataset Documentation
## American Art as Political Artifact: A Dataset of Politically Consequential Visual Culture (1754–2020)

---

## What Is This Dataset and Why Does It Exist?

This dataset catalogs 75 works of American visual culture — paintings, photographs, political cartoons, murals, posters, performance art, and memorials — selected for their political consequence. The central question driving the project is: **how has visual art shaped, responded to, and become inseparable from American political history?**

The dataset spans from Benjamin Franklin's *Join or Die* (1754) to the George Floyd memorial murals (2020), covering colonial propaganda, Civil War abolitionism, New Deal documentary photography, civil rights protest imagery, AIDS activism, and contemporary Black Lives Matter visual culture. The unit of analysis is not the artwork as aesthetic object, but the artwork as political event — something that changed minds, mobilized movements, was censored, was weaponized, or became the visual memory of a historical moment.

I chose this topic because American political history is often taught through texts — speeches, legislation, court decisions — while the images that actually shaped public consciousness get treated as illustration rather than argument. This dataset treats them as primary sources in their own right.

---

## Approach: Creating Data from Scratch

This dataset was built from scratch, item by item, through manual research and interpretive decision-making. There was no pre-existing structured dataset I could audit or augment that captured this specific combination of visual culture and political impact. Existing art databases (like those from the Smithsonian or Getty) catalog provenance and medium but do not assess political consequence, historical context, or impact rating — the variables most central to my research questions.

Building from scratch meant confronting what the assignment correctly warns about: every dataset embeds interpretive choices. Deciding whether something qualifies as "politically consequential" is not a neutral call. It required developing explicit criteria and applying them consistently across very different media, time periods, and communities.

---

## Data Structure and Variable Decisions

Each row represents a single work or cluster of related works. The columns are:

| Field | Description |
|---|---|
| `id` | Sequential identifier |
| `title` | Title or common name of the work |
| `artist` | Creator(s), including photographers, collectives, and institutional producers |
| `year` | Year of creation or first major publication/display |
| `medium` | Physical/material form (oil on canvas, press photograph, street mural, etc.) |
| `era` | Broad historical period for navigation (Colonial & Revolutionary; Civil War & Reconstruction; 20th Century; Contemporary 1970s–present) |
| `political_context` | The specific political moment or debate the work responds to or enters |
| `institution` | Current repository, archive, or location (where known) |
| `subject_matter` | A brief visual description of what the work depicts |
| `gender_of_artist` | Gender of the creator |
| `race_ethnicity_of_artist` | Race/ethnicity of the creator |
| `political_impact_rating` | My 1–5 assessment of how consequential the work was as a political artifact |
| `historical_event_depicted_or_influenced` | The specific event(s) the work depicts, responds to, or helped shape |
| `themes` | Recurring conceptual categories for cross-dataset comparison |
| `significance` | A prose explanation of why this work matters politically — the interpretive core of each entry |
| `source_used` | The archive, catalog, or institutional record consulted |
| `notes` | Complications, controversies, context that doesn't fit elsewhere |

### Key Variable Decisions

**Why a political impact rating?** The rating (1–5) is admittedly the most subjective variable. I defined a 5/5 rating as works that demonstrably changed public opinion, directly contributed to policy or legislative outcomes, catalyzed mass movements, or became so widely reproduced that they defined the visual memory of an event. A 4/5 covers works with significant documented influence that fall short of that threshold. I ended up with very few entries below 4/5 because I was deliberately selecting the most consequential works — the rating system is more useful for distinguishing within the dataset than for filtering it.

**Why include gender and race/ethnicity of the artist?** One of the patterns I was most interested in is the gap between who creates politically consequential art and who is represented within it. Works like *Migrant Mother* (white female photographer) and *The Scourged Back* (white male photographers) depict Black and poor subjects while the authorial gaze belongs to someone outside that community. Tracking artist identity makes this dynamic legible in the data.

**Why the `notes` field?** The assignment asks us to document what gets lost in data. The notes field is where complications live. Paul Revere copied his engraving from Henry Pelham without credit. Dorothea Lange never paid Florence Owens Thompson. Ernest Withers was later revealed to be an FBI informant. Maya Lin's race and gender were weaponized against her Vietnam memorial design. These facts don't fit cleanly into any structured variable, but they are central to how these works function as political artifacts.

---

## Computational Tools Used

The dataset was manually created, but I used Claude (Anthropic) as a research assistant throughout the process in two ways:

**1. Checking and supplementing historical context.** For works I knew well (e.g., Migrant Mother, Iwo Jima), I used Claude to verify specific dates, confirm current institutional locations, and surface details I might have missed (e.g., that Flagg modeled Uncle Sam on his own face; that the *Silence = Death* poster predated ACT UP). This was genuinely useful for catching errors and adding depth to the significance field without replacing my own historical knowledge.

**2. Testing my categorization logic.** I used Claude to probe edge cases — whether a performance piece like Fusco and Gómez-Peña's *Two Undiscovered Amerindians* belonged in a dataset defined around visual art, whether documentary photographs are "art" in the relevant sense, whether a memorial (Maya Lin's Vietnam wall) operates like a political artwork. These conversations helped me articulate and refine my inclusion criteria.

**Limitations of using AI assistance:** Claude's knowledge of less-documented works — particularly by artists of color, Indigenous artists, and works from community archives — was noticeably thinner than its knowledge of canonical Euro-American works. For entries like Emory Douglas's Black Panther illustrations, the Chicano Park murals, and Ernest Withers's photographs, I had to rely more heavily on my own research and was more cautious about the details Claude supplied. This is itself a data point about how existing digitized archives skew toward documenting white and institutional art history.

---

## Inclusion and Exclusion Decisions

**Inclusion criteria:**
- The work must have had a documented, traceable political effect (changed public opinion, was used in a campaign, was censored, catalyzed protest, shaped legislation)
- The work must be primarily visual (I excluded literary works like *The Jungle*, though I included its visual adaptations)
- The work must be American in origin or directly central to American political history

**What I excluded:**
- Works with primarily aesthetic rather than political significance (Winslow Homer, Georgia O'Keeffe)
- Works that influenced art history but not political history
- Works with significant political themes but no evidence of real-world political impact
- Architecture (except the Vietnam Memorial, which I included because of its documented political controversy and effect)

**The hardest exclusion decisions:** Several entries in the dataset are actually clusters of related works treated as a single entry (e.g., "Ferguson protest murals and protest art," "Post-9/11 visual culture"). This was a methodological compromise. The BLM visual movement and the AIDS quilt are not single objects; they are entire visual cultures. I flagged these in the notes field as umbrella entries that could be disaggregated in a scaled dataset.

**What I know is missing:** The dataset is still weighted toward work that entered the mainstream record — meaning it underrepresents Indigenous visual art traditions, Latinx political art outside the Chicano movement, and Asian American visual activism beyond the Chinese Exclusion era. These aren't oversights I can correct by adding more hours; they reflect gaps in the digitized archival record I was working from, which I'll need to address deliberately in the next phase.

---

## Patterns and Tensions That Emerged

Several analytical patterns emerged that I hadn't anticipated before building the dataset:

**The white-gaze problem in politically progressive imagery.** A significant number of the most influential political images depicting oppressed communities were made by white artists and photographers: Dorothea Lange's Dust Bowl work, the *Scourged Back* photograph, Eddie Adams's Vietnam execution photograph, the *Migrant Mother*. These images did real political work — they built public support for New Deal programs, turned opinion against slavery, shifted sentiment on Vietnam. But the bodies depicted were not the bodies behind the camera. The dataset makes this pattern visible across eras in a way that's harder to see when looking at works individually.

**Photography vs. painting as political instruments.** The dataset shows a clear shift around 1860: before the Civil War, paintings, engravings, and cartoons dominate the political visual record. After the invention of mass-circulation press photography, photographs become the primary instruments of political persuasion. This has implications for what "impact" means — a cartoon in the 1850s might reach tens of thousands; a photograph in the 1940s reaches millions in a day.

**The tension between political intent and political reception.** Several entries show works whose political meaning transformed after creation: *We Can Do It!* was an internal factory poster that became a feminist icon 40 years later. *Join or Die* was created for the French and Indian War and redeployed as Revolutionary propaganda. *Piss Christ* was a devotional work that became a battleground over government arts funding. The dataset captures intended political context but can't fully capture these post-hoc transformations — that's a limitation I'll need to think about in documentation.

---

## Next Steps: Scaling the Dataset

In the next phase, I plan to scale this dataset toward 500–1,000 items using a combination of approaches:

**Option 1 — Institutional API access.** The Smithsonian, Library of Congress, and Metropolitan Museum of Art all have open APIs with structured metadata. I can query these for works tagged with politically relevant terms (civil rights, labor, protest, suffrage, etc.) and pull structured data at scale. The challenge will be that institutional metadata reflects curatorial decisions — it will over-represent canonical works and under-represent community art, street murals, and protest ephemera.

**Option 2 — LLM-assisted annotation.** I can feed images and basic metadata into a vision model and ask it to generate structured annotations for the `subject_matter`, `themes`, and `significance` fields. This would allow me to process a much larger corpus, but I'll need to build an evaluation framework to check how accurately the model applies my interpretive criteria — especially the political impact assessment.

**Option 3 — Targeted archival expansion.** To address the gaps I identified (Indigenous art, Latinx visual culture, Asian American activism), I'll supplement with targeted searches in community archives: the Chicano/Latino Arts Archive at UC Berkeley, the Wing Luke Museum digital collections, the Smithsonian's National Museum of the American Indian. This won't scale the same way, but it will make the dataset more representative.

The central methodological challenge of scaling is this: the `significance` field — the interpretive core of each entry — took the most time and judgment to write for each item. Automating it risks losing exactly the kind of close historical reasoning that makes the dataset useful. My goal is to use computation to expand the corpus of items while preserving human-authored significance notes for at least the highest-impact entries.

---

*Dataset created Spring 2026. Source materials drawn from Library of Congress, Smithsonian Institution, National Archives, and individual institutional catalogs as noted in each entry.*
