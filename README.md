# COMP 247 Project

Created by Group 1:
- Ayman Yasin
- Daniil Velykyi
- Garnett Grant
- Julian Gomez

---

**Group Project &ndash; Developing a predictive machine learning model (classifier) and deploy it as a web API for inference**

## 1. Purpose

The purpose of this project is to:

1. Pre-processing - Retrieve & prepare the data:
    1. Load and explore the dataset referenced in section 4 in this document using techniques learnt during this course.
    2. Visualize the data and describe it thoroughly, identify correlations, etc.
    3. Clean, transform categorical data and model the dataset using the techniques learnt throughout the course in preparation for building a predictive model.
2. Model building & fine tuning
    1. Build a supervised predictive model based using a suitable classification algorithm(s) in Python, utilizing scikit-learn, pandas, numpy, etc., to provide predictions as specified in project specification, section 3 of this report.
    2. Validate / score and evaluate the models and choose the best model after carrying out hyper-parameter tuning.
3. Model deployment
    1. Build an API for the model using Python Flask framework.
    2. Deploy the model on local host.
    3. Build a simple front end to access the API and pass new feature values to the prediction model for inference.

## 2. Guidelines & Instructions

Be sure to read all the guidelines and instructions.

### General

- This Project is to be completed in groups of 5 students.
- Read the textbook, course lecture content, class examples, and additional references provided here. Each team are free to research and use more materials and tools to implement a good solution, just make sure to reference it in your solution and your report.

### Presentation

- Each group will have to present and demonstrate their solution in Week 14 or as agreed with their professor.
- During the presentation, each group needs to demonstrate the solution i.e. live code execution and as needed illustrate part of the code. In addition, the group needs to present all key findings, assumptions, constraints, and the list of technologies used clearly.

### Submission

- All code developed in Python and any other language should be part of the submission.
- The submission should be accompanied with a report prepared as a Microsoft document or a pdf explaining the project and detailing all the assumptions, constraints applied. (Details in section 3).
- Name the project submission *KSI_Group_Group#_section_section#COMP247Project*, where *Group#* is the assigned group number and *section#* is the group's section number.
- The submission should be a zipped file containing the code and the written report.

Two submissions are required as follows:

- Part #1: Due week #10, this will include deliverables #1 & 2 (Data exploration & Data modeling). Worth 13%
- Part #2: Due week #14 this will build on part #1 and will include a full report & demonstration of all the deliverables. Worth 13%

### Peer Evaluation

- Each team member will complete a peer evaluation form relating to other team members and this will count in the final grade.
- Grades are issued based on contribution to the project work.

## 3. Project Specifications & deliverables

Both the police department and the "general public" would make use of a software product that can give them an idea about the likelihood of fatal collisions that involve loss of life. For the police department, it would assist them in taking better measures of security and better planning for road conditions around certain neighborhoods. For public individuals, it would help them assess the need for additional precautions at certain times and weather conditions and neighborhoods.

Based on the dataset described in point four below, which is actual data collected over the period of five years by the Toronto police department. You need to build a predictive service that based on certain features would provide a classification of either <u>**the incident would result in fatality or not**</u>.

Please arrange to provide the following deliverables for your project.

1. Data exploration: a complete review and analysis of the dataset including:

    - Load and describe data elements (columns), provide descriptions & types, ranges and values of elements as appropriate. – use pandas, numpy and any other Python packages.
    - Statistical assessments including means, averages, correlations
    - Missing data evaluations – use pandas, numpy and any other Python packages
    - Graphs and visualizations – use pandas, matplotlib, seaborn, numpy and any other Python packages, you also can use power BI desktop.

2. Data modelling:

    - Data transformations – includes handling missing data, categorical data management, data normalization and standardizations as needed.
    - Feature selection – use pandas and sci-kit learn. (The group needs to justify each feature used and any data columns discarded)
    - Train, Test data splitting – use numpy, sci-kit learn.
    - Managing imbalanced classes if needed. Check here for info: https://elitedatascience.com/imbalanced-classes
    - Use pipelines class to streamline all the pre-processing transformations.

3. Predictive model building

    - Use logistic regression, decision trees, SVM, Random forest and neural networks  algorithms as a minimum– use scikit learn
    - Fine tune the models using Grid search and randomized grid search.

4. Model scoring and evaluation

    - Present results as accuracy , precision, recall, F1 scores, confusion matrices and plot the ROC curves of the models - use sci-kit learn
    - Select and recommend the best performing model

5. Deploying the model

    - Using flask framework arrange to turn your selected machine-learning model into an analytics  API.
    - Using pickle module arrange for Serialization & Deserialization of your model.
    - Deploy your model on local host.
    - Build a client to test your model API service. Use the test data, which was not previously used to train the module. You can use simple Jinja HTML templates with or without Java script, REACT or any other technology but at minimum use POSTMAN Client API.

6. Prepare a report explaining your project and detailing all the assumptions, constraints you applied should have the following sections:

    - Table of contents
    - Executive summary (to be written once nearing the end of project work, should describe the problem/solution and key findings)
    - Overview of your solution(to be written once nearing the end of project work)
    - Data exploration and findings (dataset field descriptions, graphs, visualizations, tools and libraries used….etc.)
    - Feature selection (tools and techniques used, results of different combinations…etc.)
    - Data modeling (data cleaning strategy, results of data cleaning, data wrangling techniques, assumptions and constraints)
    - Model building (train/ test data, sampling, algorithms tested, results: confusion matrixes ...etc.)

## 4. Data Set

This dataset includes all traffic collisions events where a person was either Killed or Seriously Injured (KSI) from 2006 to 2020  in the city of Toronto. (might change to 2021 depending on frequency of update)

In accordance with the Municipal Freedom of Information and Protection of Privacy Act, the Toronto Police Service has taken the necessary measures to protect the privacy of individuals involved in the reported occurrences. No personal information related to any of the parties involved in the occurrence will be released as open data.
The location of the incident occurrences have been deliberately offset to the nearest road intersection node to protect the privacy of parties involved in the occurrence. All location data must be considered as an approximate location of the occurrence and users are advised not to interpret any of these locations as related to a specific address or individual.
The reported  dataset is intended to provide communities with information regarding public safety and awareness. The data supplied to the Toronto Police Service by the reporting parties is preliminary and may not have been fully verified.

[KSI dataset](https://data.torontopolice.on.ca/datasets/TorontoPS::ksi/about)

Use the download tab and select spreadsheet to download the dataset as a csv file, also download the pdf guide the describes the metadata and navigate to the specific section that describes the KSI dataset. You can find the guide at this link [PUBLIC SAFETY DATA PORTAL: OPEN DATA DOCUMENTATION](https://ago-item-storage.s3.us-east-1.amazonaws.com/c0b17f1888544078bf650f3b8b04d35d/PSDP_Open_Data_Documentation.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEMb%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJGMEQCIA1YfDmhR6VtaBTbCOhwMBzSsTwBce1bePd1G23AWmrrAiAyHhceE1GTfVO2XcMQWbSZZf3uoZKcjGaeQL8A5qSYgCrcBAiO%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYwNDc1ODEwMjY2NSIMIQZGPu6c9Ej7aeBeKrAEcHgQKG4roAZyVAloJwVxhiCK%2FikUQfI280kGdp48jqHC2TobFBh5PfpRPryD%2BYchNXLg%2BJ8OexcLuk6iinRj6bcJGZcvoMRSdBbRx3dKJJdGHYCz6VNT0%2BIADpePEN0792YhRQsjcvTNm%2FuKuqJcFxO60GSvAfPMtMLEMESwoZ3NWRcpzQk7DhjH7gaCNZYNNP6t%2FFpHoalNmNH8nMmzZmbeRy1MaEEUedGtbYRTdYFeewxCq3JjuRvBRl7HM%2B7wlwDlsu2l%2FYCvITEFKhAwvFgTdT4tOtMJHzisP5LeHlvFPWSmGhrEO9lJx7HkWk2bE8i4K7r4GZc5DR2UdEtr%2FIePoUElXVqZk8yRt9dA22mZr846%2FzCA3XsG4y9G%2BJv1fsZqSGZZp5j5ba%2BVDJiKatwv6bIGEXDaXnynrqFNwe%2F59kosLH7jecg1canrm0BB6fk0vbHPgH%2FJXRbNZfteSj6mdpx3wlYyePq0eSvhOZdhJdw7PRiQUOHwtIHzQ7XTvYBqlgSJlVsCQwJNfTbn%2BzH6x5Q0%2BC6w4yZ%2FkrfPRDM55qOOJgrfHfuGS4IWaoNN3sJCMCbyLW7nyFDQLHxXsRjGttMwebAEnKq0JjLDdowf1AzGhObpPwYkkcYaO9Nq0f8sBEcFZBIlWHa35dY83O3WBPRsktlFpMRlv4gQbRQTAYN9Vyf4LkrDJ%2FXzaS4nnvexTQ3wNqEnl7FHMuAl%2BiEHYZiyevCrfPw%2FCXeXPTIw8ZrPkwY6qgGavDRPQB8paix69lnZqSD6GVGCWiCipLSLZjqeg1fcY3w4U82btiRDgyC%2BYLcpx%2BMBG7vfYPjPEWmzpDXHwNokTSSuwsF8wFsSDR%2FZaRZY%2FPR8gOE5gbC%2Fa%2Bw6t345C%2Bky9N7hUC0BXAuzY%2Bg9R%2B%2BA69YF5Rm8eHv2FRr%2BBYyQ6rwS5eVcTDVJnDOO6Gr4gbBq7x1oTN9jMVtkgkgBTCOivQdwNAwwQN%2FwaQ%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20220505T144248Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAYZTTEKKEQLTJ47HU%2F20220505%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=bc3783b540bdee4bcb6d8e6924a096d4da4f271180c8aa32fde7d560aec2c824)
