# Individual Articles
<details>
  <summary><strong>Jasmitha: American Stories: A Large-Scale Structured Text Dataset of Historical U.S. Newspapers</strong></summary>
  
  ## Bibliography
    Title: American Stories: A Large-Scale Structured Text Dataset of Historical U.S. Newspapers

    Authors: Melissa Dell, Jacob Carlson, Tom Bryan, Emily Silcock, Abhishek Arora, Zejiang Shen, Luca D’Amico-Wong, Quan Le, Pablo Querubin2, Leander Heldring

    Publication Venue: Published on Cornell University's arxiv.org
    Year: 2023
    DOI/URL: https://doi.org/10.48550/arXiv.2308.12477
    Link to code repository: https://github.com/dell-research-harvard/AmericanStories

  ## AI Summury
    - prompt:
    
    summurize this article for me:
    American Stories: A Large-Scale Structured Text
    Dataset of Historical U.S. Newspapers

    - response:

        American Stories: A Large-Scale Structured Text Dataset of Historical U.S. Newspapers introduces a new dataset designed to make historical newspapers easier to analyze at scale. Built from sources like Library of Congress’s Chronicling America collection, the project uses improved OCR and document processing techniques to extract cleaner, more structured text from scanned newspaper pages. Unlike prior datasets that often treat pages as unorganized text blocks, American Stories identifies meaningful units—such as articles, headlines, and sections—making it far more useful for research in history, economics, and data science. A key contribution of the dataset is its emphasis on text quality and usability. The authors apply filtering methods to remove illegible or low-quality regions and evaluate performance using metrics like the non-word rate, showing substantial improvements over existing archives. This combination of higher OCR accuracy and smarter content selection results in a dataset that is both large-scale and reliable, enabling more precise analysis of long-term trends in American society, language, and media.

## Part Two
**What is the Data?**

    The data is U.S. public domain newspapers that readable quality might be low. The newspapers are  different  from the usual format of newspapers. The newspapers are from Library of Congress’s Chronicling America and contains almost 20 million scans in a dataset called American Stories.There’s always going to be some lines the OCR won’t be able to pick up, so we lose historical data. The captures the complexity as article’s who’s format and texts weren’t understood before are now able to analyzed and used digitally.

**How is Computation Used and Why?**

    They created a pipeline to extract high quality digitized article text and layout regions from the scans. The computation is detecting the content regions and then an image classifier to removing illegible text bounding boxes and then digitized with OCR. The primary purpose of the computation is to make it the articles more legible, so there’s augmenting and then reading the data. The article is filtering out and scanning American Stories and it shows the non-word rate to be less likely as high as Chronicling America’s. Yes, they need the computation to read the amount of articles in American Stories. They could transcribe it, which they did for a few randomly selected ones.

## Part Three: What AI Missed.

    I think ChatGPT gave me a decent summary about the article. It talked about the how American Stories makes “meaningful units” which is what the article’s main way of extracting the OCR was, understanding the newspaper format. It also talked about the dataset and it’s emphasis on text quality and usability. 

</details>

<details>
  <summary><strong>Ananya</strong></summary>
  
## Bibliography
**Article:** Miller, M. K., & Sutherland, J. L. (2023). *The Effect of Gender on Interruptions at Congressional Hearings*. *American Political Science Review*. [https://doi.org/10.1017/S0003055422000260](https://doi.org/10.1017/S0003055422000260)

**Code/Data:** Harvard Dataverse. [https://doi.org/10.7910/DVN/5PEQSS](https://doi.org/10.7910/DVN/5PEQSS)


## AI Summury
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

## Part Three: What AI Missed.

Overall, the AI was good at capturing the high-level details of the research, including the general research question, the factors considered, and the results. However, it missed numerous crucial details that were requested in the prompt for the summarization. One issue is that while the summary noted that the authors controlled for factors such as seniority or party affiliation, it did not mention that this was done with the help of supplemental databases, even though the prompt explicitly asked for data sources rather than only a singular primary data source.

Beyond this, the AI was also vague in its description of the methods and did not specifically identify regex parsing and logistic regression as part of the computational approach. Instead, it simplified the method to "computational text analysis," which does not provide a reasonable level of detail. Although there do not appear to be clear hallucinations, the summary still oversimplified the article in ways that left out important methodological specifics.


</details>

<details>
  <summary><strong>Adin: MapSAM: Adapting Segment Anything Model for Automated Feature Detection in Historical Maps</strong></summary>
  
## Bibliography
Title: MapSAM: Adapting Segment Anything Model for Automated Feature Detection in Historical Maps
Authors: Xue Xia, Graduate Student Member, IEEE, Daiwei Zhang, Wenxuan Song, Wei Huang, Lorenz Hurni

## AI Summury
 Prompt: In 1-2 paragraphs summarize this article: https://huggingface.co/papers/2411.06971
 Summary: **MapSAM** is a framework that adapts Meta's Segment Anything Model (SAM) for automated feature detection in historical maps. [huggingface](https://huggingface.co/papers/2411.06971) The core motivation is that automated feature detection could greatly speed up the reconstruction of geospatial history, but the process is typically bottlenecked by the labor-intensive task of manually creating high-quality training data. While SAM offers strong generalization abilities, applying it directly to historical maps in a zero-shot manner struggles with recognizing certain geospatial features and requires manual input prompts, limiting full automation. [huggingface](https://huggingface.co/papers/2411.06971)

To overcome these limitations, MapSAM introduces a parameter-efficient fine-tuning strategy using Weight-Decomposed Low-Rank Adaptation (DoRA) to inject domain-specific knowledge into SAM's image encoder, along with an automatic prompt generation process that removes the need for manual prompting. The framework also upgrades SAM's positional prompts into richer positional-semantic prompts and modifies the mask decoder's cross-attention with masked attention for better feature aggregation. Experiments show MapSAM performs well across both linear and areal historical map segmentation tasks, and notably adapts effectively even when fine-tuned on very limited data — as few as 10 examples. [huggingface](https://huggingface.co/papers/2411.06971)

## Part Two
This article discusses a relatively new way to process Historical Map Data, which is called the Segment Anything Model (SAM). SAM has been designed to help the process of digitizing maps and understanding the data that they produce. SAM is a "vision foundation model" used for image segmentation. The SAM model was not specifically created for Map data and still struggles with some prompting, so this article discusses MapSAM, a model they created that is more fine-tuned for this specific use case. The researchers ran an experiment comparing their model to existing models. They tested two different datasets to compare the detection of different types of topographic features, railroads, and vineyards. Both datasets were maps collected from the Swiss Sigfried map(s), which is a complete topographic map of Switzerland compiled between 1870 and 1926.

This article is all about a relatively new development in computational humanities: using computer vision. Computer vision as a whole has been making great strides in recent years, making it much easier to digitize records like maps, which otherwise are much more difficult than text-based documents. While this technology is extremely promising for allowing us to further our understanding of map data, since it is so new, we are still learning about its efficacy, which is both exciting and challenging for researchers. While MapSAM is a step in the right direction, there's still a long way to go to create fully accurate maps, and researchers are still working to find better methods

## Part Three: What AI Missed.
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

## 1. Methodology and Scope
The researchers used advanced computational tools to analyze a massive dataset:
The Corpus: Over 17 million congressional speeches (of which ~200,000 were immigration-related) and 5,000 presidential communications.
Techniques:
Machine Learning (RoBERTa): Trained to classify the "tone" (pro-immigration, anti-immigration, or neutral).
Lexicons: 14 specific "frames" (e.g., crime, family, labor) were curated to see how immigrants are characterized.
Contextual Embeddings (BERT): Used to identify "implicit dehumanizing metaphors"—language that sounds like it refers to things like "animals" or "cargo" without using those exact labels.

## 2. General Historical Trends
The study identifies three distinct eras in political immigration rhetoric:
1880–1940 (The Negative Era): Tone was consistently negative across both parties. Interestingly, there was no "spike" in negative rhetoric leading up to the strict 1920s quotas; rather, the sentiment had been staunchly anti-immigrant for decades.
1940–1965 (The Humanitarian Shift): Sentiment improved dramatically during and after WWII. This shift was driven by humanitarian concerns and a reframing of the U.S. as a "nation of immigrants," peaking around the passage of the 1965 Immigration and Nationality Act.
1970s–Present (The Polarization Era): While the average tone remains more positive than a century ago, a massive partisan divide began in the late 1970s.

## 3. Key Findings on Polarization and Partisanship
The research reveals a linear increase in polarization that predates general political polarization by a decade:
Democrats: Currently express unprecedentedly positive attitudes toward immigration.
Republicans: Their rhetoric has declined steadily since the late 1970s. Today, Republican speeches are as negative as the average congressional speech was in the 1920s, an era defined by extreme isolationism and quotas.
Presidents: Modern presidents have historically been more pro-immigration than the average member of Congress. However, Donald Trump is the stark exception, identified as the most anti-immigration president in the 140-year record.

## 4. Framing and Dehumanization
The study highlights how the two parties use different "frames" to discuss the topic:
Republican Framing: Disproportionately uses frames related to "crime," "legality," "threats," "deficiency," and "flood/tide."
Democratic Framing: Focuses on "family," "victims," "contributions," and "culture."
Implicit Dehumanization: Republicans are significantly more likely to use language suggestive of metaphors like "animals," "cargo," "vermin," and "disease." This language has become more common in Republican rhetoric in recent decades.

## 5. The Persistence of Nationality Bias
Even after the formal elimination of race-based quotas in the 1960s, the tone of speeches varies wildly based on which nationality is mentioned:
The "European" Advantage: Speeches mentioning European groups (e.g., Italians, Irish) shifted to positive earlier and remain overwhelmingly positive.
The Mexican/Chinese Parallel: There is a "striking similarity" between how Mexican immigrants are framed today and how Chinese immigrants were framed during the exclusion era (1882–1943). Both groups are uniquely associated with "crime," "labor," and "legality" frames.
The Outlier: Mexican immigration is the strongest outlier today; the gap in tone between how politicians discuss Mexican versus European immigrants is as wide as the gap between Democrats and Republicans.

## 6. Conclusion
The authors conclude that while the U.S. has nominally moved away from race-based exclusion, nationality and geography remain central factors in how politicians characterize immigrants. Despite high public approval for immigration in modern polls, the political discourse—especially on the right—has regressed to 1920s-level negativity for specific groups.


## Part Two
----
The data in this research are congressional and presidential speeches. In the congressional record, speeches from 140 years might be missing or taken out of context: without mentioning what historical events were happening locally and globally, it's hard to understand what influenced the sentiment of these speeches. Considering that researchers used a keyword-based approach to filter 17 million congressional speeches to detect immigration speeches, some of the keywords, specifically different variations of the words, might be missing from the filtration context. Based on the lecture that we learnt today about lemmatization and stemming of words, and how 'running' and 'run' and 'runners' might be considered as different words and might be omitted from the context if it doesn't exactly match the spelling, which all depends on the decision that is made by a data scientist. In addition, considering the samples of the project that this research looked at (from Congress and the president), it doesn't include media and activists' voices and speeches. Also, we should keep in mind that the Congressional Record also gets edited sometimes.  Overall, while this research offers one of the most comprehensive quantitative analyses of U.S. political speech on immigration to date, its findings should be read as one lens, not the full picture.

In computational analysis research they used human annotations to train the Roberta classifier, NLP model that detected the tone of the speech for immigration later in the research, and then applied it at scale. Considering the scale of 200,000 of speeches that were analyzed, I feel a computational approach was necessary here. It took 5 annotators to complete only 7626 segments to analyze these speeches for tone and framing. So, this is a perfect case when computation is necessary. In terms of what might get lost, again referring to the lemmatization process, depending on how the author of the analysis scanned the text, some of the word formation might be lost; consequently, some sentences and speeches might not be taken for this simple reason. They used human annotations to train the Roberta classifier and then applied it at scale.

Their research splits the augmentation and analysis. Firstly, researchers prepare the data, which is a part of the augmentation process: download 17M speeches, extract speakers, year, party for each, clean immigration speeches based on wording, used human annotation from 5 researchers to train the Roberta model. The analysis part gets blended at the point when human annotators analyze and classify the content. After NLP classification gets to work, they track trends in the tone of 140 years, comparing the parties' tone (Democrats vs Republicans)
Identifying specific keywords usage frequency used by each party, such as 'crime', 'families', economy', etc). The main purpose of combining these 2 methods was to actually firstly teach NLP on what the guidelines and rules are that it should follow, and apply computational analysis after (NLP text analysis) to speed the process of labeling 200'000 speeches. 


## Part Three: What AI Missed.

After looking over the Gemini summary and reading the article, I realized that Gemini missed a lot of the statistical and visual table results. For example, dehumanization ratios (under Fig.3) were missing, and the most influential words by era in Table 1 were not mentioned anywhere (under the title 'Language, Framing, and Dehumanization'). It wasn't stated how China, from 1880 to 1900, was mentioned in 20% of all of the congress speeches ( "China occupied an especially prominent place in 19th-century congressional debates on the issue, being mentioned in more than 20% of the immigration related speeches in Congress over the years 1880 to 1900."). Also, Gemini didn't get the statement about dehumanization correctly - it didn't add the comparison with democrats in this statement, which 'has become more common in Republican rhetoric in recent decades'. Overall, Gemini captured the general picture and findings of the research, but omitted most of the visual table details.
</details>

<details>
  <summary><strong>Christina: Explainable stock prices prediction from financial news articles using sentiment analysis</strong></summary>
  
## Bibliography
Authors: Shilpa Gite, Hrituja Khatavkar, Ketan Kotecha, et al.
Title: Explainable stock prices prediction from financial news articles using sentiment analysis
Venue: PeerJ Computer Science (peer-reviewed journal)
Year: 2021
DOI: https://doi.org/10.7717/peerj-cs.340
Article Link:https://pmc.ncbi.nlm.nih.gov/articles/PMC7924447/
Code Repository: https://github.com/Hrituja/Stock-Market-Prediction


## AI Summury
 This paper explores how sentiment analysis of financial news can improve stock price prediction. The authors combine historical stock price data with sentiment extracted from news headlines to build a predictive model. They collect over 200,000 financial news headlines and pair them with stock market data from sources like Yahoo Finance. The idea is that investor sentiment, influenced by news, plays a major role in stock price movements.
To model this relationship, the authors use a deep learning approach based on Long Short-Term Memory (LSTM) networks, which are well-suited for time-series data. They also incorporate Explainable AI (XAI) techniques, specifically LIME, to interpret the model’s predictions. This allows users to understand which words in news headlines contribute to predicted stock movements. The goal is not only to improve prediction accuracy but also to make the model more transparent and trustworthy for decision-making.


## Part Two
The data in this study consists primarily of financial news headlines and stock market data, reflecting how financial events are communicated and interpreted by the media. The news headlines were collected from Pulse, an aggregator that gathers articles from sources like Reuters and Business Standard, with over 210,000 headlines. 

The authors use sentiment analysis and deep learning to analyze how news influences stock prices. The LSTM model learns patterns over time by combining text-based sentiment with numerical stock data, allowing it to capture how past events influence future prices . Additionally, the paper uses Explainable AI to interpret the model. Without machine learning, it would be nearly impossible to process such a large dataset or identify any subtle patterns between language and market behavior. Since the model assumes that sentiment directly impacts prices, it may overlook other factors like certain policies or insider trading. Additionally, since only headlines are used, it could miss a lot of deeper context that sentiment analysis could get from a full article.

## Part Three: What AI Missed.
The AI summary was generally accurate in describing the main idea of combining sentiment analysis with stock prediction and mentioning LSTM and explainability. But it did oversimplify how the data works and shapes the results, as it did not mention any limitations, such as the fact that only headlines are used, which reduces complex financial narratives into simplified text. Additionally, the AI made the method seem more straightforward than it is, ignoring tradeoffs like bias in news sources.
</details>


# Group Part
## Step 1: Share Your Critical Findings

## Step 2: Map How Computation Is Being Used
<details><summary><strong>Augmentation</strong></summary></details>
<details><summary><strong>Analysis</strong></summary></details>
<details><summary><strong>Communication</strong></summary></details>

## Step 3: Find Trends, Divergences, and Silences

Silences: 

Across the group’s articles, a major silence is how the categories get defined. A lot of the studies are dependent on labels, including positive/negative sentiment, pro/anti-ammigration, interruptions, or visual classes, but they don’t address how those categories were created and the wide range of material that gets lost when trying to fit into them, because they can be so broad. Additionally, a lot of data is excluded throughout the studies, since many are reliant upon archives, whose processes often involve many gaps and biases.


____
Based on the conversation with the group about articles, we found that computation was used in two distinct but quite related ways across 5 articles. certain articles set clusters of based on similarity of their computational methods, data analysis, and the data itself. One group used more text-based analysis through NLP and text classification and the other cluster is based on computer vision and image segmentation. Even though the approaches to work with data were different, there are so many similarities across 5 projects. For example, they all relied on historical archives (congressional speeches, news headlines, maps, newspapers, transcripts), all of them used some classification method for the data, and most of the projects relied on human judgment before applying computational technologies to scale the work. As a part of the findings from this assignment, my group concluded that computation bridges the human beginnings and initiative in the humanistic projects and serves as an efficient way to read and process large amount of data.
