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


## AI Summury
 

## Part Two

## Part Three: What AI Missed.


</details>
