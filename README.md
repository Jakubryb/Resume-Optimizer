# Resume Optimizer

##### Scraper Files and Scraped Data will be uploaded soon

## Overview
The goal of the project is to tailor a resume to the data science field to improve it's rating in a compnaies applicant tracking system to increase the odds of scoring an interview. This was done by scraping resumes from Indeed and recent job posts for data scientists/analysts positions from Indeed and Glassdoor. NLP preprocessing was applied to the resumes as well as my own. Modeling was done through TF-IDF and Latent Dirichlet Allocation. From there I measured the cosine similarity using TF-IDF between my resume and the target fields, the first being the resumes of other data scientist and then against the scraped job posts. By identifying key words and skills and then incorporating them into my resume, the cosine smilarity score increases which in turn should increase my ranking within a companies tracking system.

![](data/pics/TitlePage.jpg)

---

## Business Understanding

Most companies, especially the big ones, don’t read every resume that they receive. They usually rely on an Applicant Tracking system that will rank applicants for a specific job opening and usually focus on the ones most fitting for the job. As someone who has just completed a data science bootcamp and is undergoing a pretty big career change, It is my hope that I can use what I learned to make my self more hirable by tailoring my resume towards this new field.

---

# Data Sources

The data for the project was scraped using mostly selenium, beautiful soup, and APIs.

In total I was able to scrape over 8000 Data Scientist Resumes from Indeed, however only about 4,000 were usable. There were many that were just the skeleton of a resume, and others were resumes of people that are in a completely unrelated field.

Approximately 600 recent job posts for entry and junior level data scientist were also sccraped from Glassdoor.

NLP Preprocessing was conducted to extract key words or phrases and their significance throughout all the files to the best of my abilities.


---

# Methods and Process

1. Scrape Indeed for Resumes using sellenium. To do this I had purchased Indeeds "For Employers' subsription for one month in order to have access to candidate resumes
2. Use sellenium and beautiful soup to scrape the most recent entry level and junior data scientist/analyst job posts from Glassdoor and Inded.
3. Preprocess and clean data by removing stop words,apply stemming etc. This goes for the resumes, job posts and resume being optimized
4. TF-IDF and LDA modeling
5. Determine Cosine Similarity between my resume and the ones scraped from indeed.
6. Modify my resume by adding or modifying key words synonymous with the other resumes
7. Determine Cosine Similarity between my resume and the job posts.
8. Once again modify my resume to increase the similarity score when scored against the job post data

---

## Evaluation

Without making changes or looking at other applicants then scoring the resume against all the others resulted in a similarity score of approximately 0.7093

Upon modifying against my resume against other data scientist/analyst CV's I was able to raise my similarity score to above 0.8019.


---
## Conclusion

The increase in similarity scores against other applicants builds a good initial resume, however my goal is not to become identical to another candidate. The purpose of this project is to try and appear as an ideal candidate for the  data scientist jobs I will be applying to. 

Therefore, we basically have to repeat the entire proces with our new modified resume and tailor it further against the 700 job posts that were scraped

Upon scoring the previous resume against these job descriptions, I had wound up with a cosine similarity of 0.7840.

Once again modfying my resume so it is more synonymous with the job I am going for, the cosine similarity score rose to a 0.8431. 

This is at least higher than what I had started with and should make me look as a more favorable applicant when put through a companies ATS system.


## Future Improvements

Programs that make this process very user friendly and effective already exist such as jobscan.co. Regardless I would still like to try my hand at making a program where a user can upload their resume and have it suggest changes based on an interested job listing.

## Additional Contents
PDF of the Jupyter Notebook.

PDF of Presentation Presentation

Repository Structure
├── data
│   ├── app_list.csv
│   ├── big_rating_df.pickle
│   ├── data_harvest.ipynb
│   ├── library_data.csv
│   ├── library_index.txt
│   ├── mfui.pickle
│   ├── modded_library_df.pickle
│   ├── most_followed_games_users.py
│   ├── most_played_games_users.py
│   ├── mpui.pickle
│   ├── steamid_list.pickle
│   ├── steamspy_data.csv
│   ├── steamspy_index.txt
│   ├── top_rated_games_users.py
│   └── trui.pickle
├── images
│   ├── hidden.png
│   └── steam_bg.jpg
├── jupyters
│   ├── .ipynb_checkpoints
│   └── workspace.ipynb
├── .gitignore
├── Steam_Rek_System.pdf
├── Steam_Rek_System.ipynb
├── environment.yml
└── README.md