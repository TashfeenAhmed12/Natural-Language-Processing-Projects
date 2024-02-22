# Predicting Job Salary from Job Description

[Streamlit App Link](https://nlp-predicting-job-salary-from-job-description-8oqhqxsvkzpywcm.streamlit.app/)

# Objective

The project undertaken here endeavors to predict job salaries from job descriptions using text analytics. I aim to construct a Naive Bayes classification model that discerns between high (above the 75th percentile) and low (below the 75th percentile) salary positions based solely on the textual data provided within job descriptions. Salaries above $43000 are classified as High Salary

# Data Source and Description

The data, retrieved from the ["Job Salary Prediction"](https://www.kaggle.com/c/job-salary-prediction) competition on Kaggle, consists of a diverse array of job listings compiled in "Train_rev1.csv". For manageability and efficiency, I randomly sampled 2500 data points from this dataset. These were then divided into training (80%) and testing (20%) subsets to facilitate the development and validation of the predictive model. Sampled dataset has equal proportion of High and Low salary to not introduce bias in model

# Methodology

I initiated the process by implementing a series of preprocessing steps on the job descriptions, including lowercasing, punctuation and whitespace removal, and lemmatization to normalize the text. Subsequently, I employed the TfidfVectorizer to transform the cleaned text into a matrix of TF-IDF features, which served as inputs for the Naive Bayes classifier. A grid search was conducted to fine-tune the model parameters, enhancing the accuracy of salary predictions.

# Results and Insights

The resulting model demonstrated a reasonable degree of accuracy in classifying the salary categories. A confusion matrix was generated to evaluate the performance further, and the model's precision was assessed. Through analysis, I identified the top ten words that were most indicative of high and low salaries, excluding common stopwords. These words provided clear insights into the attributes and skills associated with different salary levels

**High Salary Unique Words:**

Unique words associated with high salary jobs include "commercial", "design", "develop", "ensure", "finance", "financial", "lead", "manage", "project", "senior", "strong", and "system". These terms suggest a significant emphasis on roles that demand not only technical and design expertise but also a strong grasp of commercial and financial strategies. Words like "lead", "manage", and "senior" underscore leadership roles, indicating positions of authority and responsibility that likely involve guiding teams or projects towards success. "Develop", "design", and "system" reflect the innovation and technical skill required in these roles, highlighting a need for individuals capable of creating or improving systems, products, or processes. The presence of "financial" and "finance" points towards roles where financial oversight, investment acumen, or economic analysis plays a critical part

**Low Salary Unique Words:**

For low salary jobs, unique words include "company", "customer", "excellent", "look", "must", "provide", "recruitment", "require", "school", "support", "teacher", and "year". This set leans heavily towards roles centered around support, customer service, and education. "Customer", "support", and "service" suggest positions focused on direct interaction with customers or clients, providing assistance and ensuring satisfaction. The inclusion of "school", "teacher", and "recruitment" highlights the educational and human resources sectors, indicating roles essential for organizational support and educational development but perhaps not as highly compensated as those requiring specialized technical or leadership skills. 
