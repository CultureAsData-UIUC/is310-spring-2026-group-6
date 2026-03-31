# Immigration Law Sentiment Analysis — Documentation

## Topic

I'm collecting data on immigration laws passed in Illinois, California, and Arizona from the most recent back to 2008. My goal is to develop a deeper understanding of immigration laws, how the tendency to treat these laws changes depending on the state, and how it has changed over time. I'm using Claude Code, Claude in Browser, and Gemini to get summaries of the laws, extract information, and format and insert it into my database. To evaluate the sentiment of each law — if it supports immigration or opposes — I ran the key summary prompt through both LLM models, Gemini and Claude, to compare their answers. These replies then go through my own judgment and personal input. I also manually write up the reasoning behind each sentiment decision.

The cultural materials I'm working with are laws and regulations passed by each state, sourced from the National Conference of State Legislatures. I chose these documents specifically because they are legitimate and provide a clear picture of what was happening in law enforcement and immigration history at that time. Additionally, official government documents offer a full range of details and decisions on immigration. My approach for this assignment is auditing — I took the existing Immigration Legislation Archived Database (2008–2026) but modified it and added new rows. I tailored the database to my purpose: sentiment ranking and answering the question, "What is the most pro-immigration state?"

I decided to organize the data in Excel and ultimately create a data visualization from it. Currently, I have two sheets: one is my main page with states, laws, key descriptions, and sentiment; the other contains AI answers from Gemini and Claude based on the same prompt asking for a short summary of each law.

To initially populate the database, I used Claude AI and Claude Code. These models helped me understand what resources I could use for my topic, how to finalize my topic idea, and how to build the rows that would go through scanning. Some limitations of these tools: they are restricted in their prompt requests, they sometimes hallucinate, and you need to pay for them.

I started with the initial idea of creating a research question around two variables to see if there was a correlation (which is, of course, not causation) — specifically, whether there is any tendency connecting unemployment rates and immigration. However, researching these variables was too broad in scope and unclear in its outcome goal. I decided to keep only the immigration laws database but make it my own — modify it, add the information I need, and synthesize and reflect on it. I decided to analyze immigration laws passed in Illinois, Arizona, and California. Why these states? Illinois, because it's where I live, and Arizona because it's the most fluctuating state and holds a completely different opinion from its neighbor, California, a state that consistently promotes democratic visions. When deciding what to include, I knew I should have the name of the law, the year it was passed, the state, its core point, and a link to access it. All of this information is available on the Immigration Legislation Archived Database. To categorize these laws, I included two labels: Pro-Immigration or Anti-Immigration. These tags describe the intentions of each law in one sentence. Additionally, I decided to include the reasoning behind why I assigned each law to its category. To document my work with LLM models, I created a separate sheet inside the file to store the answers that all AI models gave for each law. This will help me see firsthand how AI models are trained to produce different results and how some models might fail or hallucinate. Most of the prompts will be included in a PDF document. Working closely with the data made me think twice about how information can be hidden and that you need to double-check AI responses manually or with a different LLM model.

---

## Next Steps

I plan to use Claude Code and AI tools to efficiently prepopulate the spreadsheet with descriptions and summaries of the laws. Since I can't use web scraping on government websites, I will continue to copy and paste the laws list for a certain state and year, upload it to Claude, and ask it to insert it into my spreadsheet. This workflow is already familiar to me, and I will be able to execute it quickly.

The main change I anticipate when using individual state resources is that I will encounter more variety and inconsistency in data formatting. The decisions about what is included and how it will be included will be mine to make. The main pattern that has emerged from the data I've worked with is that California embraces immigration while Arizona restricts it. Once I scale the data, I will be able to determine whether that has been a long-running trend or something that only began around 2008.

---

## Prompts Used

### Claude (Browser) — Research & Topic Development

1. > "Browse through the most trusted and credible datasets and sources available on immigration laws passed at the state level for each 50 states starting from 1950 in the United States. Outline the source. Ask me any questions before you begin the research. Do you understand?"

2. > "Provide me with the best databases to use to merge data on by-state unemployment rates by year and state-level immigration laws."

3. > "Provide me with some resources and information on 'Try to understand the relationship and the political science context about how the laws are created, how they are related to each other. What if a federal law is passed? Within what time frame does it affect certain states? Try to understand if it is the history of the state, if it is a Republican state, if it is a blue state. Just dig into that, read each exact document.'"

4. > "Can you tell me what's the most diverse state in terms of changing the immigration policy to look at?"

5. > "Provide me with resources for this topic. I basically need to find these law documents and read them. Immigration laws passed and their tendency in states: 1. Illinois 2. California 3. Arizona. Analyze key description of each law and document and assign a sentiment analysis of the law being for immigration or against immigration."

6. > "So can you tell me — does the NCSL database reflect all of the current laws as of 2026 that were passed in each state, or do I need to go to each state website and see by myself all of these documents?"

### Claude Code — Database Population & Editing

1. > "Can you populate my database with this info" — initial request with immigration law data for AZ, CA, IL (2026 bills)

2. > "Use this info and put it on my database" — with the 3 bills: AZ SR 1036, CA SJR 9, IL HR 622

3. > "Use this State Immigration Laws_Final.xlsx" — redirecting to the correct file

4. > "Outside convo — can you check if it's safe to run it or not?" — asking about Chrome Local State fix commands

5. > "Glic flag — do they mean this glic? I don't have glic flag" — asking about the Chrome Glic flag

6. > "Based on the attached file with all of the icons, buttons, colors, and sections we have, create a design system. Ask me any questions before you begin to confirm." — Figma design system request with URL

7. > "Can you save all of the things that I wrote on database? It wasn't saved somehow" — asking about lost manual edits

8. > "Please use this information and fill my spreadsheet" — with 45 bills from 2025, all topics, AZ/CA/IL

9. > "Sorry it wasn't filtered by law enforcement — remove all of pasted in the last prompt and use these" — with 15 law enforcement-filtered bills

10. > "Only this please" — narrowing down to 7 bills: 4 CA + 3 IL, 2025

11. > "Please remove and use this" — correcting again to the final 7 bills for 2025

12. > "Use all of these data attached and put it in spreadsheet" — large batch of historical bills from 2009–2022

13. > "Check my writing. Fix awkward wording only and some connections of the sentences" — proofreading request for topic write-up

14. > "Can you go through our chat and extract all of the prompts I used" — extracting prompt history

### Gemini / Claude (Browser) — Law Summaries

> "Explain the point of the law in 1 sentence in conversational and simple language."
