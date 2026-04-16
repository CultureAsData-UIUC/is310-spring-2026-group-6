# Individual Articles

<details>
  <summary><strong>Jasmitha: American Stories: A Large-Scale Structured Text Dataset of Historical U.S. Newspapers</strong></summary>
  
## Bibliography
Title: American Stories: A Large-Scale Structured Text Dataset of Historical U.S. Newspapers

Authors: Melissa Dell, Jacob Carlson, Tom Bryan, Emily Silcock, Abhishek Arora, Zejiang Shen, Luca D'Amico-Wong, Quan Le, Pablo Querubin2, Leander Heldring

Publication Venue: Published on Cornell University's arxiv.org
Year: 2023
DOI/URL: https://doi.org/10.48550/arXiv.2308.12477
Link to code repository: https://github.com/dell-research-harvard/AmericanStories

## AI Summary
- prompt:

summurize this article for me:
American Stories: A Large-Scale Structured Text
Dataset of Historical U.S. Newspapers

- response:

American Stories: A Large-Scale Structured Text Dataset of Historical U.S. Newspapers introduces a new dataset designed to make historical newspapers easier to analyze at scale. Built from sources like Library of Congress's Chronicling America collection, the project uses improved OCR and document processing techniques to extract cleaner, more structured text from scanned newspaper pages. Unlike prior datasets that often treat pages as unorganized text blocks, American Stories identifies meaningful units—such as articles, headlines, and sections—making it far more useful for research in history, economics, and data science. A key contribution of the dataset is its emphasis on text quality and usability. The authors apply filtering methods to remove illegible or low-quality regions and evaluate performance using metrics like the non-word rate, showing substantial improvements over existing archives. This combination of higher OCR accuracy and smarter content selection results in a dataset that is both large-scale and reliable, enabling more precise analysis of long-term trends in American society, language, and media.

## Part Two
**What is the Data?**

The data is U.S. public domain newspapers that readable quality might be low. The newspapers are different from the usual format of newspapers. The newspapers are from Library of Congress's Chronicling America and contains almost 20 million scans in a dataset called American Stories. There's always going to be some lines the OCR won't be able to pick up, so we lose historical data. The captures the complexity as article's who's format and texts weren't understood before are now able to analyzed and used digitally.

**How is Computation Used and Why?**

They created a pipeline to extract high quality digitized article text and layout regions from the scans. The computation is detecting the content regions and then an image classifier to removing illegible text bounding boxes and then digitized with OCR. The primary purpose of the computation is to make it the articles more legible, so there's augmenting and then reading the data. The article is filtering out and scanning American Stories and it shows the non-word rate to be less likely as high as Chronicling America's. Yes, they need the computation to read the amount of articles in American Stories. They could transcribe it, which they did for a few randomly selected ones.

## Part Three: What AI Missed

I think ChatGPT gave me a decent summary about the article. It talked about the how American Stories makes "meaningful units" which is what the article's main way of extracting the OCR was, understanding the newspaper format. It also talked about the dataset and it's emphasis on text quality and usability.

</details>

<details>
  <summary><strong>Ananya: The Effect of Gender on Interruptions at Congressional Hearings</strong></summary>
  
## Bibliography
**Article:** Miller, M. K., & Sutherland, J. L. (2023). *The Effect of Gender on Interruptions at Congressional Hearings*. *American Political Science Review*. [https://doi.org/10.1017/S0003055422000260](https://doi.org/10.1017/S0003055422000260)

**Code/Data:** Harvard Dataverse. [https://doi.org/10.7910/DVN/5PEQSS](https://doi.org/10.7910/DVN/5PEQSS)

## AI Summary
Miller and Sutherland investigate whether women members of Congress are more likely to be interrupted than their male colleagues during committee hearings, an important question given that committee work is where most congressional business happens and where members can most directly influence policy. The authors analyze over 24,000 congressional committee hearing transcripts from the Government Printing Office (GPO), spanning the 105th through 115th Congresses (1994–2018), which includes speech data from 1,269 Members of Congress. Using computational text analysis methods to detect interruption markers in the transcripts, they examine whether gender predicts the likelihood of being interrupted while controlling for factors such as seniority, party affiliation, committee chairmanship, and the topic of the hearing.

The study finds that women in Congress are more likely to be interrupted than men, with this effect driven primarily by patterns in the U.S. Senate, where women are approximately 10% more likely to be interrupted than men. The effect is dramatically amplified when hearings discuss "women's issues," such as healthcare, family policy, education, and abortion. In these contexts, women are more than twice as likely to be interrupted overall, and in the House specifically, women are six times more likely to be interrupted during such hearings. The authors also examine "interruption clusters," meaning rapid-fire back-and-forth interruptions that indicate aggressive conflict, and find similar gendered patterns. Notably, they find little evidence that women adjust their communication style as they gain seniority, unlike patterns observed among female Supreme Court justices. Analysis of speaker dyads suggests that interruptions are more common in mixed-gender interactions and that men interrupt women more than they interrupt other men.

## Part Two

### What is the Data?

The cultural data being analyzed consists of 24,103 congressional hearing transcripts published by the Government Printing Office from 1994 to 2018. These transcripts were created by professional court reporters who transcribed, word for word, the discussions within Congress.

The data does not contain tone, speed, body language, loudness, or explicit sentiment of the speakers because it is text-based and only provides a verbatim transcript of the discussions. For that reason, the data flattens certain complexities that are valuable for analysis regarding female policymakers in the United States. However, one detail that captures a valuable complexity is the insertion of em dashes in the transcript by reporters when a speaker is interrupted. This forms the basis of the research, as the consistent usage of this syntax allows for computational text analysis and prediction of interruption, namely through regex and logistic regression.

The missing identity context of the speakers in the transcripts is supplemented through additional data from other peer-reviewed research, such as a database of committee assignments from Stewart (2017).

### How is Computation Used and Why?

The computational methods used include regex parsing of the PDFs of the transcripts to pull chunks of speech text and attribute them to the appropriate member of Congress. The researchers then identified all instances containing the aforementioned em dash that signified that the speaker was interrupted.

Given this data, logistic regression was used to calculate the probability of an interruption. This allowed for analysis into the individual and intersectional factors that contribute to the likelihood of being interrupted in a congressional hearing as a policymaker.

The primary purpose of computation in this research was to process and analyze the data. The article's goals shape the data by encouraging it to be filtered mainly to discussions with interruptions and to create groupings of gender dyads for comparison of interruption rates. Overall, computation was required here because it would have been incredibly difficult and time-consuming to manually process the transcripts, attribute them to speakers, count instances of interruptions based on speaker dyads, and so forth. Computation in this case was able to complete these tasks in a reproducible manner without black-box inference, such as from LLMs.

## Part Three: What AI Missed

Overall, the AI was good at capturing the high-level details of the research, including the general research question, the factors considered, and the results. However, it missed numerous crucial details that were requested in the prompt for the summarization. One issue is that while the summary noted that the authors controlled for factors such as seniority or party affiliation, it did not mention that this was done with the help of supplemental databases, even though the prompt explicitly asked for data sources rather than only a singular primary data source.

Beyond this, the AI was also vague in its description of the methods and did not specifically identify regex parsing and logistic regression as part of the computational approach. Instead, it simplified the method to "computational text analysis," which does not provide a reasonable level of detail. Although there do not appear to be clear hallucinations, the summary still oversimplified the article in ways that left out important methodological specifics.

</details>

<details>
  <summary><strong>Adin: MapSAM: Adapting Segment Anything Model for Automated Feature Detection in Historical Maps</strong></summary>
  
## Bibliography
Title: MapSAM: Adapting Segment Anything Model for Automated Feature Detection in Historical Maps
Authors: Xue Xia, Graduate Student Member, IEEE, Daiwei Zhang, Wenxuan Song, Wei Huang, Lorenz Hurni

## AI Summary
Prompt: In 1-2 paragraphs summarize this article: https://huggingface.co/papers/2411.06971
Summary: **MapSAM** is a framework that adapts Meta's Segment Anything Model (SAM) for automated feature detection in historical maps. [huggingface](https://huggingface.co/papers/2411.06971) The core motivation is that automated feature detection could greatly speed up the reconstruction of geospatial history, but the process is typically bottlenecked by the labor-intensive task of manually creating high-quality training data. While SAM offers strong generalization abilities, applying it directly to historical maps in a zero-shot manner struggles with recognizing certain geospatial features and requires manual input prompts, limiting full automation. [huggingface](https://huggingface.co/papers/2411.06971)

To overcome these limitations, MapSAM introduces a parameter-efficient fine-tuning strategy using Weight-Decomposed Low-Rank Adaptation (DoRA) to inject domain-specific knowledge into SAM's image encoder, along with an automatic prompt generation process that removes the need for manual prompting. The framework also upgrades SAM's positional prompts into richer positional-semantic prompts and modifies the mask decoder's cross-attention with masked attention for better feature aggregation. Experiments show MapSAM performs well across both linear and areal historical map segmentation tasks, and notably adapts effectively even when fine-tuned on very limited data — as few as 10 examples. [huggingface](https://huggingface.co/papers/2411.06971)

## Part Two
This article discusses a relatively new way to process Historical Map Data, which is called the Segment Anything Model (SAM). SAM has been designed to help the process of digitizing maps and understanding the data that they produce. SAM is a "vision foundation model" used for image segmentation. The SAM model was not specifically created for Map data and still struggles with some prompting, so this article discusses MapSAM, a model they created that is more fine-tuned for this specific use case. The researchers ran an experiment comparing their model to existing models. They tested two different datasets to compare the detection of different types of topographic features, railroads, and vineyards. Both datasets were maps collected from the Swiss Sigfried map(s), which is a complete topographic map of Switzerland compiled between 1870 and 1926.

This article is all about a relatively new development in computational humanities: using computer vision. Computer vision as a whole has been making great strides in recent years, making it much easier to digitize records like maps, which otherwise are much more difficult than text-based documents. While this technology is extremely promising for allowing us to further our understanding of map data, since it is so new, we are still learning about its efficacy, which is both exciting and challenging for researchers. While MapSAM is a step in the right direction, there's still a long way to go to create fully accurate maps, and researchers are still working to find better methods.

## Part Three: What AI Missed
Overall, I think AI did a pretty good job of getting the main ideas of this article and explains what SAM is pretty well. The only major details the AI missed were about the methodology and data collection in the article. It also doesn't really discuss the study that the researchers did or how they were aiming to evaluate the model's efficacy. To be very fair about that part, it's the most dense part of the article and requires a good amount of domain knowledge, to the point where I don't even understand most of it.

</details>

<details>
  <summary><strong>Daria: Computational Analysis of 140 Years of US Political Speeches Reveals More Positive but Increasingly Polarized Framing of Immigration</strong></summary>
  
## Bibliography
Authors: Card, Dallas, Serina Chang, Chris Becker, Julia Mendelsohn, Rob Voigt, Leah Boustan, Ran Abramitzky, and Dan Jurafsky.
Title: "Computational Analysis of 140 Years of US Political Speeches Reveals More Positive but Increasingly Polarized Framing of Immigration" Proceedings of the National Academy of Sciences 119, no. 31 (2022): e2120510119.

Link: DOI: 10.1073/pnas.2120510119
Github: https://github.com/dallascard/us-immigration-speeches/

## AI Summary
### Prompt: Summarize this article and provide the key points.
### Summary by Gemini:
This article, published in PNAS, presents the first comprehensive quantitative analysis of 140 years of U.S. political rhetoric regarding immigration, covering both congressional and presidential speeches from 1880 to 2020.

### 1. Methodology and Scope
The researchers used advanced computational tools to analyze a massive dataset:
The Corpus: Over 17 million congressional speeches (of which ~200,000 were immigration-related) and 5,000 presidential communications.
Techniques:
Machine Learning (RoBERTa): Trained to classify the "tone" (pro-immigration, anti-immigration, or neutral).
Lexicons: 14 specific "frames" (e.g., crime, family, labor) were curated to see how immigrants are characterized.
Contextual Embeddings (BERT): Used to identify "implicit dehumanizing metaphors"—language that sounds like it refers to things like "animals" or "cargo" without using those exact labels.

### 2. General Historical Trends
The study identifies three distinct eras in political immigration rhetoric:
1880–1940 (The Negative Era): Tone was consistently negative across both parties. Interestingly, there was no "spike" in negative rhetoric leading up to the strict 1920s quotas; rather, the sentiment had been staunchly anti-immigrant for decades.
1940–1965 (The Humanitarian Shift): Sentiment improved dramatically during and after WWII. This shift was driven by humanitarian concerns and a reframing of the U.S. as a "nation of immigrants," peaking around the passage of the 1965 Immigration and Nationality Act.
1970s–Present (The Polarization Era): While the average tone remains more positive than a century ago, a massive partisan divide began in the late 1970s.

### 3. Key Findings on Polarization and Partisanship
The research reveals a linear increase in polarization that predates general political polarization by a decade:
Democrats: Currently express unprecedentedly positive attitudes toward immigration.
Republicans: Their rhetoric has declined steadily since the late 1970s. Today, Republican speeches are as negative as the average congressional speech was in the 1920s, an era defined by extreme isolationism and quotas.
Presidents: Modern presidents have historically been more pro-immigration than the average member of Congress. However, Donald Trump is the stark exception, identified as the most anti-immigration president in the 140-year record.

### 4. Framing and Dehumanization
The study highlights how the two parties use different "frames" to discuss the topic:
Republican Framing: Disproportionately uses frames related to "crime," "legality," "threats," "deficiency," and "flood/tide."
Democratic Framing: Focuses on "family," "victims," "contributions," and "culture."
Implicit Dehumanization: Republicans are significantly more likely to use language suggestive of metaphors like "animals," "cargo," "vermin," and "disease." This language has been significantly more common in speeches by Republicans than Democrats in recent decades.

### 5. The Persistence of Nationality Bias
Even after the formal elimination of race-based quotas in the 1960s, the tone of speeches varies wildly based on which nationality is mentioned:
The "European" Advantage: Speeches mentioning European groups (e.g., Italians, Irish) shifted to positive earlier and remain overwhelmingly positive.
The Mexican/Chinese Parallel: There is a "striking similarity" between how Mexican immigrants are framed today and how Chinese immigrants were framed during the exclusion era (1882–1943). Both groups are uniquely associated with "crime," "labor," and "legality" frames.
The Outlier: Mexican immigration is the strongest outlier today; the gap in tone between how politicians discuss Mexican versus European immigrants is as wide as the gap between Democrats and Republicans.

### 6. Conclusion
The authors conclude that while the U.S. has nominally moved away from race-based exclusion, nationality and geography remain central factors in how politicians characterize immigrants. Despite high public approval for immigration in modern polls, the political discourse—especially on the right—has regressed to 1920s-level negativity for specific groups.

## Part Two

The data in this research are congressional and presidential speeches. In the congressional record, speeches from 140 years might be missing or taken out of context: without mentioning what historical events were happening locally and globally, it's hard to understand what influenced the sentiment of these speeches. Considering that researchers used a keyword-based approach to filter 17 million congressional speeches to detect immigration speeches, some of the keywords, specifically different variations of the words, might be missing from the filtration context. Based on the lecture that we learnt today about lemmatization and stemming of words, and how 'running' and 'run' and 'runners' might be considered as different words and might be omitted from the context if it doesn't exactly match the spelling, which all depends on the decision that is made by a data scientist. In addition, considering the samples of the project that this research looked at (from Congress and the president), it doesn't include media and activists' voices and speeches. Also, we should keep in mind that the Congressional Record also gets edited sometimes. Overall, while this research offers one of the most comprehensive quantitative analyses of U.S. political speech on immigration to date, its findings should be read as one lens, not the full picture.

In computational analysis research they used human annotations to train the RoBERTa classifier, NLP model that detected the tone of the speech for immigration later in the research, and then applied it at scale. Considering the scale of 200,000 of speeches that were analyzed, I feel a computational approach was necessary here. It took 5 annotators to complete only 7,626 segments to analyze these speeches for tone and framing. So, this is a perfect case when computation is necessary. In terms of what might get lost, again referring to the lemmatization process, depending on how the author of the analysis scanned the text, some of the word formation might be lost; consequently, some sentences and speeches might not be taken for this simple reason.

Their research splits the augmentation and analysis. Firstly, researchers prepare the data, which is a part of the augmentation process: download 17M speeches, extract speakers, year, party for each, clean immigration speeches based on wording, used human annotation from 5 researchers to train the RoBERTa model. The analysis part gets blended at the point when human annotators analyze and classify the content. After NLP classification gets to work, they track trends in the tone of 140 years, comparing the parties' tone (Democrats vs Republicans), identifying specific keywords usage frequency used by each party, such as 'crime', 'families', 'economy', etc. The main purpose of combining these 2 methods was to actually firstly teach NLP on what the guidelines and rules are that it should follow, and apply computational analysis after (NLP text analysis) to speed the process of labeling 200,000 speeches.

## Part Three: What AI Missed

After looking over the Gemini summary and reading the article, I realized that Gemini missed a lot of the statistical and visual table results. For example, dehumanization ratios (under Fig.3) were missing, and the most influential words by era in Table 1 were not mentioned anywhere (under the title 'Language, Framing, and Dehumanization'). It wasn't stated how China, from 1880 to 1900, was mentioned in 20% of all of the congress speeches ("China occupied an especially prominent place in 19th-century congressional debates on the issue, being mentioned in more than 20% of the immigration related speeches in Congress over the years 1880 to 1900."). Also, Gemini didn't get the statement about dehumanization correctly — it didn't add the comparison with Democrats in this statement, which 'has become more common in Republican rhetoric in recent decades'. Overall, Gemini captured the general picture and findings of the research, but omitted most of the visual table details.

</details>

<details>
  <summary><strong>Christina: Explainable stock prices prediction from financial news articles using sentiment analysis</strong></summary>
  
## Bibliography
Authors: Shilpa Gite, Hrituja Khatavkar, Ketan Kotecha, et al.
Title: Explainable stock prices prediction from financial news articles using sentiment analysis
Venue: PeerJ Computer Science (peer-reviewed journal)
Year: 2021
DOI: https://doi.org/10.7717/peerj-cs.340
Article Link: https://pmc.ncbi.nlm.nih.gov/articles/PMC7924447/
Code Repository: https://github.com/Hrituja/Stock-Market-Prediction

## AI Summary
This paper explores how sentiment analysis of financial news can improve stock price prediction. The authors combine historical stock price data with sentiment extracted from news headlines to build a predictive model. They collect over 200,000 financial news headlines and pair them with stock market data from sources like Yahoo Finance. The idea is that investor sentiment, influenced by news, plays a major role in stock price movements.

To model this relationship, the authors use a deep learning approach based on Long Short-Term Memory (LSTM) networks, which are well-suited for time-series data. They also incorporate Explainable AI (XAI) techniques, specifically LIME, to interpret the model's predictions. This allows users to understand which words in news headlines contribute to predicted stock movements. The goal is not only to improve prediction accuracy but also to make the model more transparent and trustworthy for decision-making.

## Part Two
The data in this study consists primarily of financial news headlines and stock market data, reflecting how financial events are communicated and interpreted by the media. The news headlines were collected from Pulse, an aggregator that gathers articles from sources like Reuters and Business Standard, with over 210,000 headlines.

The authors use sentiment analysis and deep learning to analyze how news influences stock prices. The LSTM model learns patterns over time by combining text-based sentiment with numerical stock data, allowing it to capture how past events influence future prices. Additionally, the paper uses Explainable AI to interpret the model. Without machine learning, it would be nearly impossible to process such a large dataset or identify any subtle patterns between language and market behavior. Since the model assumes that sentiment directly impacts prices, it may overlook other factors like certain policies or insider trading. Additionally, since only headlines are used, it could miss a lot of deeper context that sentiment analysis could get from a full article.

## Part Three: What AI Missed
The AI summary was generally accurate in describing the main idea of combining sentiment analysis with stock prediction and mentioning LSTM and explainability. But it did oversimplify how the data works and shapes the results, as it did not mention any limitations, such as the fact that only headlines are used, which reduces complex financial narratives into simplified text. Additionally, the AI made the method seem more straightforward than it is, ignoring tradeoffs like bias in news sources.

</details>

<details>
  <summary><strong>Vedha: Extracting Visual Content from 16 million Historical Newspapers</strong></summary>
  
## Bibliography
**Title:** The Newspaper Navigator Dataset: Extracting and Analyzing Visual Content from 16 Million Historic Newspaper Pages in Chronicling America
**Authors:** Benjamin Lee, Jaime Mears, Eileen Jakeway, Meghan Ferriter, Chris Adams, Nathan Yarasavage, Deborah Thomas, Kate Zwaard, Daniel Weld
**Publication Venue:** ACM International Conference on Information and Knowledge Management (CIKM 2020) — peer-reviewed conference
**Year:** 2020
**DOI/URL:** https://arxiv.org/abs/2005.01583
**Code Repository:** https://github.com/LibraryOfCongress/newspaper-navigator

## Part 1: AI Summary

**Prompt used:** "Summarize this article in 1-2 paragraphs: The Newspaper Navigator Dataset: Extracting and Analyzing Visual Content from 16 Million Historic Newspaper Pages in Chronicling America by Benjamin Lee et al."

**AI-generated response:**

The Newspaper Navigator project, developed by Benjamin Lee and collaborators at the Library of Congress, presents a large-scale machine learning pipeline designed to extract and categorize visual content from over 16 million historic American newspaper pages in the Chronicling America database. Using a Faster-RCNN deep learning model fine-tuned on crowdsourced annotations from the Library of Congress's Beyond Words initiative, the pipeline identifies seven classes of visual content: photographs, illustrations, maps, comics, editorial cartoons, headlines, and advertisements. The result is the largest dataset of extracted visual content from historic newspapers ever produced, complete with image embeddings for visual similarity searching.

The project's primary goal is to make the rich visual culture embedded in historic American newspapers searchable and analyzable at scale for the first time. Previously, users of Chronicling America could only search newspaper text, leaving the visual content — political cartoons, Civil War maps, early photography — largely inaccessible. By releasing the dataset, the fine-tuned model, and all source code into the public domain, the authors aim to enable a wide range of digital humanities, public history, and creative computing research. The paper also demonstrates the dataset's potential through example analyses, such as visualizing the rise of photographs in newspapers at the turn of the 20th century and compiling a collection of Civil War maps from 1861–1865.

## Part 2: My Critical Assessment

### What is the Data?
The cultural data being analyzed is the visual content embedded within historic American newspapers, specifically photographs, illustrations, maps, comics, editorial cartoons, headlines, and advertisements drawn from the Chronicling America database, which spans 174 years of American history from 1789 to 1963 across 47 states, Washington D.C., and Puerto Rico. The data was not collected fresh but was built on top of millions of newspaper pages already digitized through the National Digital Newspaper Program, a partnership between the Library of Congress and the National Endowment for the Humanities. The training data specifically came from Beyond Words, a crowdsourcing initiative where volunteers drew bounding boxes around visual content in WWI era newspapers, with approximately 10,000 verified annotations in total, which were then reformatted into a standard machine learning format to train the model.

The scale is enormous at 16.3 million pages, but the coverage has real gaps worth naming. The selection of which newspapers were included in Chronicling America was driven by which titles existed on microfilm of sufficient quality, meaning entire communities, regions, and language groups are missing or underrepresented. The training data was drawn exclusively from WWI era newspapers, which means the model was never taught what visual content looked like in the 1850s, and the paper's own testing confirms this matters, with model accuracy dropping dramatically for pre-1875 pages from about 63% overall down to just 12% for pages from 1850 to 1875. Most critically for anyone interested in American art and political culture, the dataset captures the existence and location of editorial cartoons but not their meaning. What a cartoon depicts, who it caricatures, what political argument it makes, or what historical moment it was responding to is none of that is in the dataset. The computation extracts the image but strips out the cultural interpretation entirely.

### How is Computation Used and Why?

The core computational method is a fine-tuned Faster-RCNN object detection model, a deep learning approach from computer vision that draws bounding boxes around objects of interest in an image. The model was trained to recognize 7 categories of visual content and was run across 16.3 million newspaper pages using two Amazon AWS cloud computing instances over 19 days of processing time. In addition to the object detection step, the pipeline also extracts the OCR text within each bounding box (to capture captions and headlines), and generates ResNet image embeddings which are numerical representations of each image that allow for fast visual similarity searching.

The primary purpose is augmentation — building a dataset and search tool that makes visual content discoverable at scale for the first time. However, it's important to note that the cultural weight of a political cartoon, its satirical intent, its relationship to specific historical events, is entirely outside the scope of what the model can see or capture. The computation opens a door to studying American visual political culture at scale, but what walks through that door still requires human interpretation.

## Part 3: What AI Missed

The AI summary got the basics right but missed the key issue that the model was only trained on WWI-era newspapers, so it performs poorly on older content (before 1875). It also ignored problems with the training data quality and oversimplified things by treating detecting images as the same as actually understanding them.

</details>

---

# Group Part

## Step 1: Share Your Critical Findings

Each group member gave a brief overview of their article:

- **Jasmitha (Dell et al., 2023):** Data is historical U.S. newspaper scans from Chronicling America. Computational method is an OCR pipeline that cleans, structures, and extracts article-level text from nearly 20 million scans. Purely augmentation — making previously unreadable archives usable.
- **Ananya (Miller & Sutherland, 2023):** Data is 24,103 congressional hearing transcripts from 1994 to 2018. Computational method is regex text analysis to detect em-dash interruption markers, then logistic regression to model gender-based interruption patterns. AI summary missed specific methods (regex, logistic regression) and supplemental data sources.
- **Adin (MapSAM, 2024):** Data is historical Swiss topographic maps from 1870–1926. Computational method is a fine-tuned version of Meta's Segment Anything Model (SAM) adapted for map feature detection. AI summary missed methodology details and the evaluation study.
- **Daria (Card et al., 2022):** Data is 200,000 congressional speeches and 5,000 presidential communications spanning 140 years. Computational method is RoBERTa NLP classification for tone, BERT for implicit dehumanization, and frame lexicons. AI summary (Gemini) missed Table 1 data, dehumanization ratios, and misrepresented the Republican vs. Democrat comparison.
- **Christina (Gite et al., 2021):** Data is 210,000+ financial news headlines paired with stock market data. Computational method is LSTM deep learning with sentiment analysis and Explainable AI (LIME). AI summary oversimplified limitations and missed bias in news sources.
- **Vedha (Lee et al., 2020):** Data is 16.3 million historic newspaper pages from Chronicling America. Computational method is Faster-RCNN object detection trained on crowdsourced annotations to extract 7 types of visual content. AI summary missed that training data was only from WWI-era newspapers, causing poor performance on older content.

## Step 2: Map How Computation Is Being Used

<details>
  <summary><strong>Augmentation</strong></summary>

Lee et al. (2020) and MapSAM (2024) are the clearest examples of augmentation in our group. Both use advanced machine learning techniques to take large collections of visual data that were previously unsearchable and turn them into something structured and usable. MapSAM (2024) adapts Meta's Segment Anything Model to detect geographic features in historical maps, with the explicit goal of giving researchers access to a type of data that was essentially impossible to work with at scale before. Lee et al. (2020) does the same thing for 16.3 million newspaper pages, using a Faster-RCNN model to extract 7 categories of visual content, including comics, maps, and photographs. In both cases, the computation is not making an argument; it is building infrastructure that did not exist before.

*American Stories* (Dell et al., 2023) also belongs firmly in this category. The entire pipeline is designed to clean, structure, and improve OCR text extracted from historical newspaper scans so that the resulting data is actually usable for downstream research. Like MapSAM (2024) and Lee et al. (2020), the computation in *American Stories* exists to improve the data itself rather than to analyze it directly.

</details>

<details>
  <summary><strong>Analysis</strong></summary>

Card et al. (2022) and Gite et al. (2021) lean more toward analysis, though both have significant augmentation elements built in. In Card et al. (2022), the researchers first prepare and clean 17 million congressional speeches, then use human annotators to train a RoBERTa classifier, and finally apply that classifier at scale to find patterns in how political rhetoric around immigration shifted over 140 years. The augmentation work enables the analysis, but the real goal is making a historical and political argument about polarization and framing over time. Gite et al. (2021) similarly uses sentiment classification as a means to an end, feeding the output of that classification into an LSTM deep learning model to find patterns between news language and stock market behavior. The computation is oriented toward producing a finding rather than producing a dataset.

Miller and Sutherland (2023) also fits here. It uses regex parsing and keyword classification to detect and measure patterns of interruption across over 24,000 congressional hearing transcripts, with the goal of making an argument about gender dynamics in political speech rather than simply organizing the data.

</details>

<details>
  <summary><strong>Communication</strong></summary>

Lee et al. (2020) is the only article in our group with a strong and explicit communication orientation. The dataset, the trained model, and all source code are released into the public domain for unrestricted reuse. The authors also packaged smaller derivative datasets specifically for users without coding experience, and they describe plans to build a public-facing search interface. The goal of Lee et al. (2020) is not just to do research but to make visual history accessible to educators, historians, genealogists, and the general public. This sets it apart from every other article in our group, where the intended audience is primarily other researchers.

</details>

<details>
  <summary><strong>Does computation match how the authors describe their goals?</strong></summary>

Mostly yes, but there are some interesting gaps worth noting. MapSAM (2024) and Lee et al. (2020) both present themselves as augmentation tools built for future researchers, and that matches what the computation is actually doing. *American Stories* (Dell et al., 2023) is similarly honest about its purpose, framing itself clearly as a dataset-building project without overstating its analytical claims.

The more interesting cases are Card et al. (2022) and Gite et al. (2021). Card et al. (2022) is framed as a historical argument about polarization, but a large portion of the actual computational work is data preparation and model training, which looks much more like augmentation. The analysis emerges at the end of a long pipeline that is mostly about getting the data ready. Similarly, Gite et al. (2021) presents itself as a predictive tool for financial decision-making, but the more significant contribution may actually be the sentiment classification pipeline itself rather than the stock predictions it produces. In both cases, computation is doing more foundational work than the framing of the papers suggests.

</details>

## Step 3: Find Trends, Divergences, and Silences

<details>
  <summary><strong>Trends</strong></summary>

- All researchers leveraged a relatively large volume of data, ranging from over 20,000 transcripts to 16.3 million newspaper pages.
- Many of the research papers relied on pre-existing, well-digitized archives rather than digitizing their own cultural data. Examples include the Government Printing Office for congressional hearing transcripts and *Chronicling America* for historical newspapers.
- All researchers implemented classification models or classification-based tasks.
  - Miller & Sutherland classified whether a speech was interrupted.
  - Lee et al. classified visual media into categories.
  - Card et al. classified sentiment in text toward immigration.
  - MapSAM classified map features.
  - Dell et al. classified content regions and legibility in newspaper scans.
  - Gite et al. classified sentiment of news headlines.
- All researchers included data from a wide historical window of a decade or more.

</details>

<details>
  <summary><strong>Divergences</strong></summary>

- Miller & Sutherland, Card et al., and Gite et al. focused on textual data, while Lee et al. and MapSAM focused on multimodal data, especially images.
- Lee et al. and MapSAM leveraged neural networks, while Miller & Sutherland used a much simpler logistic regression model or other classification strategy. Card et al. also incorporated human annotators, and Lee et al. likewise relied on human annotation.
- Lee et al. (*Newspaper Navigator*) crowdsourced annotations, including the use of human annotators to help improve the model's ability to distinguish art and other visual categories.
- A key connection we found was between Daria's (Card et al.) and Vedha's (Lee et al.) articles: both rely on **human annotations** to create training data before scaling up with machine learning. Card et al. used 5 Princeton annotators labeling 7,626 speech segments to train the RoBERTa classifier. Lee et al. built on crowdsourced annotations from the Beyond Words project with approximately 10,000 verified annotations to train the Faster-RCNN model. Both demonstrate that even the most advanced ML pipelines depend on human judgment at the foundation — someone has to define what the categories mean before a model can learn them.

</details>

<details>
  <summary><strong>Silences</strong></summary>

Across the group’s articles, a major silence is how the categories get defined. A lot of the studies are dependent on labels, including positive/negative sentiment, pro/anti-ammigration, interruptions, or visual classes, but they don’t address how those categories were created and the wide range of material that gets lost when trying to fit into them, because they can be so broad. Additionally, a lot of data is excluded throughout the studies, since many are reliant upon archives, whose processes often involve many gaps and biases.

</details>

## Conclusion

Based on the conversation with the group about articles, we found that computation was used in two distinct but quite related ways across our 6 articles. Certain articles set clusters based on similarity of their computational methods, data analysis, and the data itself. One group used more text-based analysis through NLP and text classification (Card et al., Miller & Sutherland, Gite et al.) and the other cluster is based on computer vision and image segmentation (Lee et al., MapSAM, Dell et al.). Even though the approaches to work with data were different, there are strong similarities across all projects. For example, they all relied on historical archives (congressional speeches, news headlines, maps, newspapers, transcripts), all of them used some classification method for the data, and most of the projects relied on human judgment before applying computational technologies to scale the work. As a part of the findings from this assignment, my group concluded that computation bridges the human beginnings and initiative in the humanistic projects and serves as an efficient and feasible way to read and process large amounts of data.

## Contributors
- **Conversation:** Everyone
- **Scribing:** Trends / Divergences (Ananya), Overview (Daria), Silences (Christina), Computational Map (Vedha)
