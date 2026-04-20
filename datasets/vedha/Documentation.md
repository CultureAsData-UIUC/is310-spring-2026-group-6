
# Dataset Documentation
## American Art as Political Artifact: A Dataset of Politically Consequential Visual Culture (1754–2020)


## What Is This Dataset and Why Does It Exist?

This dataset catalogs 75 works of American art pieces such as paintings, photographs, political cartoons, murals, posters, performance art and memorials which were selected for their political consequence. The central question driving the project is: How has visual art shaped, responded to, and become inseparable from American political history?

The dataset spans from Benjamin Franklin's *Join or Die* (1754) to the George Floyd memorial murals (2020), covering colonial propaganda, Civil War abolitionism, New Deal documentary photography, civil rights protest imagery, AIDS activism, and contemporary Black Lives Matter visual culture. The unit of analysis is not the artwork as aesthetic object, but the artwork as a political event or something that changed minds, mobilized movements, was censored, was weaponized or became the visual memory of a historical moment.

I chose this topic because American political history is often taught through texts such as speeches, legislation, court decisions while the images that actually shaped public consciousness get treated as illustration rather than argument. This dataset treats them as primary sources in their own right.


## Approach: Creating Data from Scratch

This dataset was built from scratch, item by item, through manual research and personal decision-making. There was no pre-existing structured dataset I could audit or augment that captured this specific combination of visual culture and political impact. Existing art databases (like those from the Smithsonian or Getty) catalog provenance and medium but do not assess political consequence or historical context 


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

**Why include gender and race/ethnicity of the artist?** One of the patterns I was most interested in is the gap between who creates politically consequential art and who is represented within it. Works like *Migrant Mother* (white female photographer) and *The Scourged Back* (white male photographers) depict African-american subjects while the authorial gaze belongs to someone outside that community. Tracking artist identity makes this dynamic legible in the data.

**Why the `notes` field?** The assignment asks us to document what gets lost in data. The notes field is where complications live. Paul Revere copied his engraving from Henry Pelham without credit. Dorothea Lange never paid Florence Owens Thompson. Ernest Withers was later revealed to be an FBI informant. Maya Lin's race and gender were weaponized against her Vietnam memorial design. These facts don't fit cleanly into any structured variable, but they are central to how these works function as political artifacts.


## Computational Tools Used

The dataset was manually created, but I used publically available data set catalogues, museum archives and the AI tool Claude (Anthropic) as a research assistant throughout the process in two ways:

**1. Checking and supplementing historical context.** For works I knew well (e.g., Migrant Mother, Iwo Jima), I used museum archives to verify specific dates, confirm current locations and find details I might have missed (e.g., that Flagg modeled Uncle Sam on his own face; that the Silence = Death*poster predated ACT UP). This was genuinely useful for catching errors and adding depth to the significance field without replacing my own historical knowledge.

**Limitations of using AI assistance:** Claude's knowledge of less-documented works particularly by artists of color, Indigenous artists and works from community archives was noticeably thinner than its knowledge of Euro-American works. For entries like Emory Douglas's Black Panther illustrations, the Chicano Park murals, and Ernest Withers's photographs, I had to rely more heavily on my own research and was more cautious about the details Claude supplied. This is itself a data point about how existing digitized archives skew toward documenting white and institutional art history.


## Inclusion and Exclusion Decisions

Inclusion criteria:
For a work to be included in the dataset, it had to meet three basic requirements. First, it had to have a documented and traceable political effect, meaning there is real historical evidence that it changed public opinion, was used in a political campaign, was censored by a government or institution, helped catalyze a protest movement, or contributed to a legislative outcome. Second, the work had to be primarily visual. I excluded literary works like The Jungle by Upton Sinclair, though I did include visual adaptations and illustrations connected to it, since those circulated as independent political images. Third, the work had to either originate in the United States or be so directly tied to American political history that leaving it out would create a meaningful gap.

What I excluded:
I left out works that are significant in art history but whose influence stayed within aesthetic rather than political conversations. Artists like Winslow Homer and Georgia O'Keeffe are important figures, but their work did not directly shape legislation, mobilize movements, or enter the political record in the ways this dataset is tracking. I also excluded works that have clear political themes but no documented evidence of real-world political impact. Having a political subject is not the same as being a political instrument.
The hardest exclusion decisions:
The most difficult judgment calls involved works that are not single objects at all. Several entries in the dataset are actually clusters of related works that I grouped under one row, such as "Ferguson protest murals and protest art" or "Post-9/11 visual culture." This was a compromise I made deliberately. The BLM visual movement and the AIDS Memorial Quilt are not individual artworks; they are entire visual cultures made up of thousands of objects. I flagged all of these in the notes field as umbrella entries that could and should be broken into individual items if the dataset is expanded in the next phase.

What I know is missing:
The dataset reflects a real limitation in the archival record I was drawing from. It is still weighted toward works that entered mainstream documentation, which means it underrepresents Indigenous visual art traditions, Latinx political art outside the Chicano movement, and Asian American visual activism beyond the Chinese Exclusion era. This is not something I could fix simply by spending more time on research. These gaps exist because community archives are less digitized and less indexed than institutional ones. Addressing them in the next phase will require deliberately seeking out sources outside the mainstream digital record.



## Patterns and Tensions That Emerged
Working through the dataset item by item produced several analytical observations I had not anticipated at the start.

- The white gaze problem in politically progressive imagery. A striking number of the most influential images depicting oppressed communities were made by white artists and photographers. Dorothea Lange photographed Dust Bowl migrants and Japanese American internees. The photographer behind the Scourged Back image was white. Eddie Adams, who photographed the execution of a Viet Cong prisoner, was a white American. These images did genuine political work. They built public support for New Deal programs, helped turn Northern public opinion against slavery, and shifted sentiment on the Vietnam War. But the bodies in the frame were not the bodies behind the camera. Structuring the data with an artist identity column makes this pattern visible across eras and across movements in a way that is much harder to see when looking at individual works in isolation.

- Photography versus painting as political instruments. The dataset reveals a clear shift in the dominant medium of political persuasion around 1860. Before the Civil War, the most politically consequential works are paintings, engravings, and woodcut cartoons. After the rise of mass-circulation illustrated newspapers and then press photography, photographs become the primary vehicle for political influence. This matters for how we think about the political impact rating. A widely circulated cartoon in the 1850s might have reached tens of thousands of people over several months. A photograph published in a national newspaper in the 1940s could reach millions within days of the event it depicted.

- The tension between political intent and political reception. Several entries show works whose political meaning changed completely after they were made. We Can Do It! was originally an internal Westinghouse factory poster meant to boost worker morale during World War II. It was rediscovered four decades later and became one of the most recognized symbols of feminist empowerment. Join or Die was Benjamin Franklin's argument for colonial unity during the French and Indian War and was later repurposed as Revolutionary propaganda. Piss Christ was made as a devotional work and became the center of a national debate about government arts funding. The dataset captures the original political context for each work, but it cannot fully account for these later transformations in meaning. That is a real limitation I will need to think about as the dataset grows.

## Next Steps: Scaling the Dataset

In the next phase, I plan to scale this dataset toward 100–500 items using a combination of approaches:

1. The first option is to use institutional API access. The Smithsonian, the Library of Congress, and the Metropolitan Museum of Art all have open APIs with structured metadata available for public use. I can query these collections for works tagged with politically relevant terms like civil rights, labor, protest, or suffrage, and pull structured data at scale. The main limitation of this approach is that institutional metadata reflects curatorial decisions made by those institutions. It will over-represent canonical works in the established Western art historical tradition and under-represent community art, street murals, protest ephemera, and work that was never formally collected.

2. The second option is LLM-assisted annotation. I can provide a vision model with images and basic metadata and prompt it to generate structured annotations for fields like subject matter, themes, and significance. This would allow me to process a much larger corpus than I could manage manually. The challenge is that I would need to build a careful evaluation framework to check how well the model is actually applying my interpretive criteria, especially the political impact rating, which requires historical reasoning that a model might handle inconsistently.

3. The third option is targeted archival expansion. To address the representational gaps I identified, I can search community-held archives directly, including the Chicano/Latino Arts Archive at UC Berkeley, the Wing Luke Museum digital collections in Seattle, and the Smithsonian's National Museum of the American Indian. This approach will not produce the same volume as an API query, but it will make the dataset more historically honest.

The hardest methodological challenge of scaling is not technical. It is about the significance field. That field is the interpretive core of each entry, and writing it well for each item took more time and judgment than any other part of the process. Automating it risks replacing careful historical reasoning with plausible-sounding text that misses the point of why a particular work mattered. My plan is to use computation to expand the list of items in the corpus while keeping human-authored significance notes for at least the highest-impact entries, where the interpretive stakes are highest.
