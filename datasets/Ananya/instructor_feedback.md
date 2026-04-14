# Instructor Feedback for Initial Dataset

Hi Ananya,

I appreciate the amount of detail you put into your documentation and the fact that you are aware and taking steps to avoid LLM classification issues.

There are a few issues with your dataset that need to be addressed before you can start attempting to scale up:

1. You are adding professional background and highest degree held to the data, but what does this tell us about the politicians you are trying to study? You do not include any information about the political stances, laws passed, etc. It is difficult to tell how you are going to answer your questions based on the current data. I would recommend adding textual data of some of the laws they are associated with so that we can get a clearer idea about their political activity and how their backgrounds may correspond.
2. Like I mentioned before, you did a great job accounting for any errors in LLM classification tasks. However, your immigration_visibility column, as it stands, does not provide any useful information. Nearly every row is labeled no public evidence. Moving forward, it would be best to think about how this column contributes and if it is providing any meaningful data that can be used for an analysis.
3. Including the LLM workflow you have implemented here is essentially creating a second research question in your project and dilutes both questions. This iteration of the LLM workflow seems unproductive. If you want to continue using the LLM for your project, you could simplify its role.

If you have any questions feel free to reach out to me.
