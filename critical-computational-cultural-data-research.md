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


## AI Summury
 

## Part Two

## Part Three: What AI Missed.


</details>

<details>
  <summary><strong>Adin</strong></summary>
  
## Bibliography


## AI Summury
 

## Part Two

## Part Three: What AI Missed.


</details>

<details>
  <summary><strong>Daria</strong></summary>
  
## Bibliography
Title: MapSAM: Adapting Segment Anything Model for
Automated Feature Detection in Historical Maps
Authors: Xue Xia, Graduate Student Member, IEEE, Daiwei Zhang, Wenxuan Song, Wei Huang, Lorenz Hurni


## AI Summary
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
