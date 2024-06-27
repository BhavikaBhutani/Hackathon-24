# Hackathon-24

PsychAI
Team Members: Bhavika, Janhavi, Saloni, Sejal, Bhanu 
# Introduction
Mental health is a crucial aspect of overall well-being, encompassing a wide range of conditions such as depression, anxiety, trauma, bipolar disorder, and many others. These conditions can significantly impact an individual's daily life, relationships, and productivity. Despite the growing awareness, many people still struggle to find appropriate and timely mental health care. 

Various Kinds of Mental Health Issues
1. Depression: Characterized by persistent sadness, lack of interest, and various physical and cognitive impairments.
2. Anxiety: Involves excessive worry, nervousness, and fear that interfere with daily activities.
3. Trauma: Results from experiencing or witnessing distressing events, leading to post-traumatic stress disorder (PTSD) and other related conditions.
4. Bipolar Disorder: Includes extreme mood swings between mania (highs) and depression (lows).

Early intervention and specialized treatment are essential for managing these conditions effectively. However, the process of finding the right therapist who specializes in specific mental health issues can be daunting and inefficient.

# Objective
Our objective is to create a tool that interprets the conversations between patients and mental health professionals and diganose them appropriately based on their specific symptoms. Additionally, the tool aims to assist therapists by recording and analyzing therapy sessions, tracking patient mood, signs, and progress over time.

Problem 1: The Emergency Room Situation
ER specialists often face challenges in accurately directing patients to the right therapist who specializes in conditions such as depression, trauma, or anxiety. Misdiagnosis or incorrect referrals can lead to ineffective treatment and prolonged suffering for patients.

Problem 2: Tracking Therapy Sessions
Therapists need efficient tools to record and analyze therapy sessions. Manual note-taking can be distracting and time-consuming, making it difficult to capture all the nuances of a session. A tool that tracks patient mood, signs, and progress can significantly enhance the quality of care.

# Solution
Our tool addresses the above problems by leveraging advanced natural language processing (NLP), Large language models (LLMs) and machine learning techniques.

Features
Conversation Analysis: The tool can be leveraged to record, create transcript of conversations between patients and physicians, analyze the conversation and  finally predict the mental disorder along with the symptom breakdown according to the Diagnostic and Statistical Manual of Mental Disorders. This will aid the medical professionals to also verify their findings. The tool will also display percentage overlap of various disorders that a patient can have. This feature will help physcians pay more attention to correctly diagnosing such patients.
Specialist Matching: Based on the conversation analysis, the tool can suggest therapists/therapy to the patients to treat conditions such as depression, trauma, and anxiety.
Session Recording: The tool records therapy sessions, allowing therapists to focus on the interaction without the distraction of taking notes.
Mood Analysis: Analyzes the recorded conversations to gauge the patient's mood and emotional state throughout the session.
Condition Prediction: By analyzing the dialogue, the tool can predict the type of mental health issue the patient is dealing with.
Comprehensive Dashboard: Provides therapists with a detailed dashboard to track session summaries, patient progress, and historical data from the first visit to the current state.

# Implementation

The following is the POC that we have developed for the hackathon

1. Dataset(s)

Our project utilizes a combination of multiple datasets to provide a comprehensive perspective on various mental disorders. Due to the lack of a consolidated dataset covering a range of disorders, we identified individual datasets dedicated to anxiety [1], bipolar disorder [2], and depression [3]. Each dataset contains textual data with corresponding labels indicating the presence or absence of the disorders. We amalgamated these datasets into a unified training set to develop a robust classification model. For testing, we used a separate dataset comprising conversations between patients and psychiatrists. By leveraging our trained model, we predicted the specific mental disorder present in each patient based on their dialogue. Additionally, we employed a third dataset for Exploratory Data Analysis (EDA) to discern the most influential features associated with each mental disorder, enhancing our understanding of their underlying characteristics.

2. Proposed Method(s) Applied
We propose a machine learning approach to classify mental health states from textual data using Natural Language Processing (NLP) techniques.

Pre-processing and Feature Engineering:
1. Text Cleaning: Removed irrelevant symbols, URLs, stop words, converted text to lowercase, and removed punctuations.
2. Lemmatization: Normalized words to their base form.
3. Word Embeddings/Tokenization: Explored TF-IDF (Term Frequency-Inverse Document Frequency).
4. Sentiment Analysis: Captured emotional cues within the text data to identify positive, negative, or neutral sentiment.
5. Cosine Similarity: Measured similarity between documents.
6. Feature Extraction: Explored additional features like conversation length, specific keywords, or POS tagging.
7. SMOTE: Used to balance the imbalanced depression dataset.

Classification Models:
1. Multinomial Naive Bayes (MNB)
2. Random Forest (RF)
3. Support Vector Machine (SVM)
4. EXtreme Gradient Boosting (XGBoost)
5. Decision Tree

We conducted Exploratory Data Analysis (EDA) using various visualization techniques and statistical analyses to gain insights into the data:

1. Data Visualization: Created plots to represent the distribution of mental health diagnoses and symptoms.
2. Feature Importance Analysis: Determines the relative importance of different symptoms in predicting mental health conditions.
3. Correlation Analysis: Identified potential associations and patterns between symptoms.

3 Evaluation Metric(s)
We used metrics like accuracy, F1-score, macro-averaging, micro-averaging, AUC-ROC, and Matthews Correlation Coefficient to evaluate our NLP models. For EDA, we focused on interpretability of visualizations, identification of potential predictors, and examination of correlation strengths between symptoms.


# Use Cases
The tool has broad applications in various settings to support mental health care:

Colleges
Counseling Centers: Helps counselors accurately direct students to the right mental health professionals based on their needs. Tracks student progress and provides insights into common mental health issues among the student body.

Organizations
Employee Assistance Programs (EAPs): Assists in directing employees to specialized therapists for issues like workplace stress, anxiety, and depression. Tracks employee mental health trends and progress over time, aiding in creating better workplace wellness programs.

Healthcare Facilities
Hospitals and Clinics: Supports ER specialists and therapists in providing accurate referrals and tracking patient progress. Enhances the overall quality of mental health care by ensuring patients receive specialized treatment.

# Future Work
Broader Condition Coverage: Expand the tool to include more mental health conditions and tailor recommendations accordingly.
Mobile and Web Applications: Create accessible applications for patients and therapists to use the tool on-the-go.
