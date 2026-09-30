# Project Overview

> **AI Notice**
>
> This learning experience may include AI-generated images, audio, and/or video. All content is reviewed and approved by Udacity learning and subject matter experts.

## Project Overview Video Transcript

> So, I'm here with Robert from Airbnb. Robert, thanks so much for joining us.
>
> Thank you for having me.
>
> So, I know that you have actually quite a few posts on Medium that have a lot of people who read them and follow your work. Can you talk about how you got started with that? What are some of the ways that you go about sharing your information? Things like that.
>
> So, I wrote my first public posts in 2015, and it was about my experience working as a data scientist at Twitter, and it was meant to be a reflection of my journey for myself, but then eventually it got retweeted by a famous data scientist, and then it went viral, unexpectedly. I think that gave me some courage to keep writing, and what I've noticed so far in all my pursuit in writing about data science is I generally write about subjects that I struggled to learn in the past.
>
> For example, I am very passionate about data engineering, but a few years back, it's very hard for me to find useful information. But then I am very fortunate to work at Airbnb, work with many very smart data engineers, and I've learned a lot from them. So, I decided to just synthesize and write down everything that I know about the subject.
>
> One is to, for me, for myself, internalize what I've learned and to celebrate it a little bit, and then the second part is just to make information more available to other people.
>
> Yeah, I think Hadley Wickham had a quote—not a quote, sorry—had a tweet in which he said things are useful, doesn't have to just be a complete new software; sometimes it's documentation. Sometimes there's just explaining how things work. I really echo with that, because I really benefit a lot from people who can explain things really well, and who can articulate things really well to me so that I can learn this stuff.
>
> Then you do it to a whole broad audience.
>
> Yeah, I hope I contribute a little bit to that, yeah.
>
> So, do you have any advice for people who are just getting started with writing their own post?
>
> There's a lot of benefits of putting your work out there, because you will get unexpected feedback and sometimes you will get unexpected attention or opportunities. So, I think this is true if you're early in your career, or you had been in industry for a few years. Just sharing stuff in general I think it's really valuable, and it's something that's generally—I think that's something that's quite special about Tech in Silicon Valley in general—just like people are very willing to share information, and there's a lot of benefits from that.

## Introduction

During this project, you will write a blog post that answers the following questions from your chosen data set.

Questions:

1. What are the most important features of the data set, what do they mean, and how do they drive the predicted outcome?
2. What unusual, or creative, insights are you able to gather from the data set?
3. How accurate is the model that you have trained to predict the data in the data set?
4. What will happen in a creative, predictive, scenario using the model that you have trained?

The purpose of the project is to show that you understand the information presented to you and can explain it in a clear way to an audience.

---

# Project Dataset Options

## Data

For the project, you will choose data from one of the data sources listed below. Data scientists work in all different domains, so choose the dataset that interests you most!

Your main constraint is that you have only learned how to work with tabular, numeric data so far. You will have the easiest time if you look for CSV datasets that primarily contain numbers. It's ok if you only have a few features and a target variable.

Avoid datasets that are primarily composed of text or image data; working with these data types in scikit-learn is out of scope for this course.

### Tech Careers: StackOverflow Developer Survey

Visit the [developer survey homepage](https://survey.stackoverflow.co/) to download survey results from this year and past years, dating back to 2011. For inspiration, check out some of the [findings that StackOverflow put together for the 2024 survey](https://survey.stackoverflow.co/2024/).

### Credit and Economic Data: The World Bank Databank

[World Bank Databank Website](https://databank.worldbank.org/)

The World Bank is an institution that provides much needed credit and economic management for countries around the world. As part of their duties, they have comprehensive forms of economic data on their partners.

### History: The Roman Empire Data

[Project Mercury – Computational Modeling in Roman Studies](https://projectmercury.eu/datasets/)

The Roman Empire was the world's preeminent center of culture, commerce, and high civilization for thousands of years. Curious archaeologists have compiled comprehensive data on Roman Civilization that we can learn from. Using new, advanced, machine learning tools, be one of the first to analyze data from the Roman Empire and explore Roman Civilization.

### Economic and Business Data: United States of America Business Formation Statistics

[Business formation statistics – US Census Bureau](https://www.census.gov/econ/bfs/index.html)

The United States of America is the world's leading economy and uses bureaucratic staff to manage its economic activities. One of these organizations, the Census Bureau of the United States, compiles statistics on new business formation within the country to understand the flow of economic activity.

### Healthcare: Centers for Medicare & Medicaid Services (CMS)

[CMS dataset search](https://data.cms.gov/provider-data/search)

The United States CMS is a federal agency that provides health coverage to millions of Americans. Their datasets primarily focus on medical facilities that accept Medicare and Medicaid patients.

### Education: DataShop

[DataShop landing page](https://pslcdatashop.web.cmu.edu/)

DataShop is a repository of datasets related to the learning sciences. It is maintained by Carnegie Mellon University.

---

# Project Steps and Instructions

## Key Steps for the Project

Feel free to be creative with your solutions, but do follow the **CRISP-DM process** in finding your solutions.

1. Begin the project by conducting an exploratory data analysis. Common forms of exploratory data analysis include generating distribution plots to understand the skewness of different variables or generating histograms to understand how data is distributed. Alternatively, some data scientists like to perform principal component analyses to better understand the underlying structure of the data.
2. Next, summarize the findings of your exploration. Explain whether the data needs to be cleaned based on your findings. If it does, perform the data cleaning. If not, move on with selecting the type of machine learning model that is appropriate for predicting from your data.
3. Train the machine learning model on your data. Evaluate the model for overall accuracy, recall, and other evaluation scores. Explain what the measures tell us about the model and how it works.
4. Imagine a new scenario that requires a prediction from your model to answer. Describe the scenario in your post and run a prediction from the model. Explain the meaning of this prediction and what it tells a reader.

## Project Deliverables

There are two **deliverables** that are required for project completion:

- A **GitHub repository** for your code.
- A **blog post** of your findings.

Your **GitHub repository** must have the following contents:

- A README.md file that communicates the libraries used, the motivation for the project, the files in the repository with a small description of each, a summary of the results of the analysis, and necessary acknowledgments.
- Your code in a Jupyter notebook, with appropriate comments, analysis, and documentation.
- You may also provide any other necessary documentation you find necessary.

For the **blog post**, pick a platform of your own choice. For example, it can be on your website, a Medium post (Josh's sample [report](https://medium.com/@josh_2774/how-do-you-become-a-developer-5ef1c1c68711) on *How Do YOU Become A Developer?*), or a GitHub blog post. Your **blog** must provide the following:

- A clear and engaging title and image.
- Your questions of interest.
- Your findings for those questions with a supporting statistic(s), table, or visual.

**Note:** The post should not dive into technical details or difficulties of the analysis; this should be saved for GitHub. The post should be understandable for non-technical people from many fields.

## Logistics Reminders Video Transcript

> Here are a few other helpful points that are necessary for writing a great post, but are aimed more at the logistics of creating your post.
>
> First, being short and sweet wherever possible will increase the number of viewers. Try to limit your posts between 1–2 pages or 200–500 words, not including the images.
>
> Second, create an outline. In the case of the post you're making for this project, your questions will serve as a great outline. I imagine an outline from my post as introduction, Take Away 1, Take Away 2, Take Away 3, and then a conclusion. This outline will make sure that everything I write is tied to one of these points and that I don't get too far off track.
>
> Finally, reviewing your work is important. The more you and others can review the work, the better it will become. Not only will you catch small mistakes, but you'll also be able to make sure that you're writing in a way that's relatable and easy to understand for your readers.
>
> This part is imperative for successful posts. But don't be afraid to post unfinished thoughts or questions and challenges that you're still pondering. Sometimes the feedback process can help spark new ideas that you otherwise wouldn't have looked into.

## Keeping Yourself and Your Reader Motivated

- Keep your post short and sweet. Short posts will increase audience engagement, as well as the likelihood you complete the writing of your post. Try to limit your post to 200–500 words.
- Create an outline. A useful outline for your post could just include an introduction, each of your questions or takeaways, and then a conclusion. This will help you stay focused when writing your post.
- *Review. Review. Review.* When you think you have reviewed enough, find someone else to review. The more review you have of your work, the better it will become. Also, don't be afraid of posting your unfinished thoughts and questions that you are still pondering.

> ## 📝 Task List
>
> - [ ] Create GitHub repo
> - [ ] Select platform for blog post and create account if needed
> - [ ] Create README for Github repo
> - [ ] Write code in a Jupyter notebook
> - [ ] Push your README and code to the Github repo
> - [ ] Write and publish your blog post
> - [ ] Check your work against the rubric to ensure you meet all of the necessary criteria for the project

---

# Environment Setup

## Project Environment

Use the following Python packages in a Jupyter Notebook environment to complete the code portion of this project:

- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`

---

# Rubric

Use this project rubric to understand and assess the project criteria.

## Code Functionality and Readability

| Criteria | Submission Requirements |
|---|---|
| Code is readable (uses good coding practices – PEP8) | Code has a logical structure and uses comments with markdown effectively. The steps of the data science process (gather, assess, clean, analyze, model, visualize) are clearly identified with comments or Markdown cells, as well. The naming for variables and functions should be according to PEP8 style guide. |
| Jupyter Notebook is executable and correct | All the project code is contained in a Jupyter notebook which can be successfully executed to generate the correct output. |
| Contains code that is well documented and uses formal code conventions | Code is well documented and uses functions and classes as necessary. All functions include document strings. DRY principles are implemented. |

## Data

| Criteria | Submission Requirements |
|---|---|
| Project follows the CRISP-DM Process while analyzing their data. | Project follows the CRISP-DM process outlined for questions through communication. This can be done in the README or the notebook. If a question does not require machine learning, descriptive or inferential statistics should be used to create a compelling answer to a particular question. |
| Proper handling of categorical and missing values in the dataset. | Categorical variables are handled appropriately for machine learning models (if models are created). Missing values are also handled appropriately for both descriptive and ML techniques. Document why a particular approach was used, and why it was appropriate for a particular situation. |

## Analysis, Modeling, Visualization

| Criteria | Submission Requirements |
|---|---|
| There are 3–5 business questions asked and answered. | In the Jupyter Notebook, there are between 3–5 questions asked, related to the business or real-world context of the data. Each question is answered with appropriate visualization, table, or statistic. |

## GitHub Repository

| Criteria | Submission Requirements |
|---|---|
| Student must publish their code in a public Github repository. | Student must have a Github repository of their project. The repository must have a README.md file that communicates the libraries used, the motivation for the project, the files in the repository with a small description of each, a summary of the results of the analysis, and necessary acknowledgements. Students should not use another student's code to complete the project, but they may use other references on the web including StackOverflow and Kaggle to complete the project. |

## Blog Post

| Criteria | Submission Requirements |
|---|---|
| Communicate their findings with stakeholders. | Student must have a blog post on a platform of their own choice. The post should communicate the data science performed and provide non-technical summaries that explain the findings. The post should clearly communicate the important inferences of the analyses. |
| There should be an intriguing title and image related to the project. | Student must have a title and image to draw readers to their post. |
| The body of the post has paragraphs that are broken up by appropriate white space and images. | There are no long, ongoing blocks of text without line breaks or images for separation anywhere in the post. |
| Clearly state the business questions and the corresponding solutions. | Each question is clearly stated and each answer includes a clear visual, table, or statistic. |