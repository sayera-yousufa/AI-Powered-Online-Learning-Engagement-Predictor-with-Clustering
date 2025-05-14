# AI-Powered-Online-Learning-Engagement-Predictor-with-Clustering
In online learning environments, student engagement significantly impacts academic success. However, educators struggle to identify students with low engagement (e.g., minimal participation in forums or resources) in real-time, hindering timely interventions. The challenge is to predict student engagement levels (low, medium, high) based on behavioral patterns, such as resource access and discussion posts, and to profile students for personalized support, ensuring improved learning outcomes in virtual education systems.

# DATASET
* Source: STUDENT_DATA.csv (~480 rows).
* Features:
    * Numerical: raisedhands, VisITedResources, AnnouncementsView, Discussion.
    * Categorical: StudentAbsenceDays, Relation, ParentAnsweringSurvey (one-hot encoded).
    * Target: Class (0=low, 1=medium, 2=high engagement).


# FEATURES
* Engagement Prediction: DNN predicts engagement levels using behavioral features.
* Student Profiling: K-Means clusters students into 3 profiles for targeted interventions.
* Interactive Dashboard: Plotly visualizes DNN accuracy and clusters (engagement_dashboard.html).
* Intervention Suggestions: Generates educator recommendations (e.g., "Encourage forum posts") in student_suggestions.csv.
* Performance Evaluation: Accuracy and confusion matrix assess model performance.

# REQUIREMENTS
* System: Standard laptop (e.g., 8GB RAM, Intel i5).
* Software: Python 3.8+, Jupyter Notebook, web browser.
* Libraries:
    * pandas==1.5.3
    * numpy==1.23.5
    * scikit-learn==1.2.2
    * tensorflow==2.12.0
    * plotly==5.14.1
    * seaborn==0.12.2
    * matplotlib==3.7.1

# OUTPUT
* engagement_dashboard.html: Interactive Plotly dashboard with:
* Training/validation accuracy over 50 epochs.
* Scatter plot of VisITedResources vs. Discussion, colored by cluster.
* engagement_predictions.csv: Actual vs. predicted engagement for test set.
* student_suggestions.csv: Suggestions for 5 students (e.g., "Encourage forum participation").
* Console: Accuracy, confusion matrix, and cluster statistics.
  
<img width="838" alt="Image" src="https://github.com/user-attachments/assets/74d32003-218d-47ff-bc28-06e09cc49e90" />

# RESULTS
* DNN achieved ~80% accuracy , predicting engagement (low, medium, high) with deeper model (16+8 neurons, 20% dropout), 50 epochs, categorical features (StudentAbsenceDays, Relation). Confusion matrix showed fewer misclassifications . K-Means clustered students: active (high VisITedResources, ~80), moderate (~50), struggling (~20). Plotly dashboard visualized accuracy, clusters. student_suggestions.csv gave recommendations (e.g., “Encourage forum posts”).

# FUTURE SCOPE
Add quiz response data, use Random Forest, deploy on cloud, create adaptive learning plans, expand to multiple institutions.

# CONCLUSION
System predicts engagement at ~80% accuracy, clusters students, and supports educators with targeted interventions, enhancing online education.

# ACKNOWLEDGEMENTS
* Edunet Foundation for mentorship.
* Open-source libraries: TensorFlow, Scikit-learn, Plotly.
