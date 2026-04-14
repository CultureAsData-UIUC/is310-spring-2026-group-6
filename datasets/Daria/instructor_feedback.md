# Instructor Feedback for Initial Dataset

Hi Daria,

I think this topic has a lot of potential as the study of immigration laws are important for understanding American politics and culture.

Here are a few suggestions for your dataset and documentation:

1. Are you performing sentiment analysis on the LLM generated summary of the law or the law itself? This is not clear. If you are doing this on the summary, then you are effectively studying the sentiment of the LLM and not the law. I would recommend including the text of the laws as well and performing sentiment analysis on that text directly.
2. You need to be clear about how you label "pro-immigration" and 'anti-immigration'. How are you making this determination? The dataset as it is only includes a few justifications for these labels.
3. Emphasis on the LLMs in your workflow effectively creates two research questions. You are trying to answer a question about immigration and also answer a question about how LLMs perform on classification tasks. This dilutes both questions and reduces the effectiveness of your analysis.
4. You need to have a clear plan for how to scale this project. It is not feasible for you to collect hundreds of laws by hand. It looks like the websites you are pulling your information from are not government websites, so you should look into whether these sites can in fact be scraped. In any case, you will need a concrete plan for the computational component of the final project.

Please reach out to me if you have any questions.
