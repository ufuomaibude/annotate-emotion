# annotate-emotion
Project Title: Annotation Project on Emotion - Based Sentiment Classification Using Social Media Data.

# Project Overview
This project focused on building a high-quality annotated dataset from social media comments, specifically YouTube, for the purpose of training and evaluating sentiment classification models. The objective was to identify emotional states; specifically, 'happy' and 'sad' expressed in user-generated text using both distant and manual annotation strategies. The project aimed to demonstrate the effectiveness of machine learning in natural language processing (NLP), while emphasizing responsible AI practices throughout the annotation and model evaluation lifecycle.

# Project Objectives
•	To build a sentiment-annotated dataset using a combination of distant and manual annotation techniques.
•	To predict emotional states (happy or sad) in social media comments using machine learning models.
•	To compare the performance of distant annotation with manual annotation using inter-annotator agreement (IAA) and Kappa statistics.
•	To ensure responsible data handling through privacy preservation, fairness, and human oversight.
•	To apply annotation guidelines consistently to support transparency and reproducibility in sentiment classification tasks.

# Methods and Tools
1.	Data Collection: YouTube API (via Google Cloud) was used to extract 4,217 comments across four videos representing happy and sad sentiments.
2.	Annotation Techniques:
2.1.	Distant annotation was performed using a pre-trained English word vector library to match sentiment keywords.
2.2.	Manual annotation was also done by human annotators on a subset of 1,000 comments (two groups of 500), with inter-annotator agreement calculated.
3.	Annotation Guidelines: Defined and applied consistently throughout the project to guide label accuracy and fairness.
4.	Data Preprocessing: Implemented in Python (Google Colab) using libraries such as pandas and NumPy. This involved:
4.1.	Removal of duplicates and irrelevant columns (e.g., timestamp, username, video ID).
4.2.	Cleaning null values, tokenizing text, and standardizing format.
5.	Model Training and Evaluation:
5.1.	Employed Random Forest Classifier using scikit-learn.
5.2.	Used train_test_split (80/20 split), fit() for training, and predict() for testing.
5.3.	Evaluation metrics: Precision, Recall, F1-score, Confusion Matrix.
5.4.	Applied LIME (Local Interpretable Model-Agnostic Explanations) for model explanability.
6.	Visualization Tools: matplotlib and seaborn were used for heatmaps and result illustrations.
7.	Data Storage: Structured Excel workbook with four sheets:
7.1.	Raw YouTube Dataset
7.2.	Machine-Annotated Dataset
7.3.	Manual Annotation Group 1
7.4.	Manual Annotation Group 2

# Key Findings
•	The Random Forest model demonstrated reasonable performance, but manual verification showed misclassifications. LIME revealed that some key terms were wrongly labeled due to model misinterpretation.
•	Manual annotation significantly outperformed distant annotation in label reliability.
o	Group 1 IAA: 78.20% agreement
o	Group 2 IAA: 68.80% agreement
•	Kappa Test Results: Indicated fair agreement for human annotators vs slight agreement for the machine, reinforcing the importance of human oversight.
•	The machine learning model failed to correctly classify sarcastic or emoticon-heavy comments, confirming the importance of linguistic context in sentiment analysis.
Achievements
•	Successfully built and annotated a new dataset with clear sentiment labels.
•	Demonstrated the practical and ethical complexities of applying machine learning to subjective human expression.
•	Integrated AI explanability (LIME) into the evaluation workflow.
•	Contributed to understanding gaps between automated and human-level annotation reliability.
Impact and Practical Implications
•	Research Impact: Enhances the understanding of emotional AI and real-world NLP applications, particularly in sentiment-based recommender systems and behavioral analytics.
•	Social Impact: Supports the development of mental health tools, customer satisfaction systems, and digital well-being platforms that rely on emotion detection.
•	Ethical AI Development: Highlights the necessity of manual verification, annotation guidelines, and responsible data handling in building AI systems that interact with human expression.

# Conclusion and Recommendations
This project demonstrated the complexities and nuances involved in emotion-based sentiment classification from unstructured social media text. While distant annotation enabled rapid data labeling, manual annotation proved more reliable, as confirmed by IAA metrics and Kappa statistics. The findings underscore the importance of consistent annotation guidelines, ongoing model improvement, and human validation in the machine learning pipeline. Responsible AI practices, including data privacy, fairness, and oversight were integrated throughout the process, making this project not only technically sound but also ethically aligned. Moving forward, we recommend expanding the annotation scope to include more emotions, refining pre-trained libraries to capture nuanced expressions (e.g., sarcasm, cultural context), and exploring more advanced NLP architectures such as transformers for improved sentiment classification.


































