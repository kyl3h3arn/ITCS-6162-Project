# Does Increased Mobile Phone Use Impact Student Health & Academic Performance?

ITCS 6162 Summer 2024 Project \
Kyle Hearn, M.S. Computer Science Candidate

### Research Question: Does Increased Mobile Phone Use Impact Student Health & Performance?

As mobile phone usage is becoming ever more common in our personal and social lives, it is inevitable that the rise of mobile phone usage for learning is upon us as well. However, is this necessarily a good thing? This project will seek to predict an answer to this question based on the Student Health & Academic performance.

## Project Description:

This is a diagnostic and predictive project. It aims to understand the impact of mobile phone usage on students' health and academic performance and to predict outcomes based on usage patterns. By analyzing patterns and relationships in the data, key factors that influence these outcomes can be identified. This understanding can inform educators, parents, and policymakers about the benefits and drawbacks of mobile phone usage in educational settings. 



#### Relevant Domain Information:

(links to two or more articles that relate to your research question; one will most likely come from the link to the data)

## Data Information:

#### Student's Health & Academic Performance

This data set is a single .CSV file and consists of various aspects of mobile phone usage among students, along with their perceived impact on their health and performance. It provides valuable insights into how mobile phones affect students' health, academic performance, and daily activities. It can be used for further analysis to identify trends and correlations between mobile phone usage and its impacts on various aspects of students' lives. 

**Source:** https://www.kaggle.com/datasets/innocentmfa/students-health-and-academic-performance/data

#### Columns:

- Names: Student Names
- Age: Student Ages (Years)
- Gender: Male/Female
- Mobile Phone: Do students own a mobile phone? (Y / N)
- Mobile Operating System: Type of movile operating system used (e.g. Android, IOS, other)
- Mobile phone use for education: Do students use their mobile phone for educational purposes? (Sometimes / Frequently / Rarely)
- Mobile Phone Activites: List of mobile phone activities used for educational purposes (e.g. Online Research, Educational Apps, Email, Online Learning Platforms)
- Helpful for Studying: Do students find movile phone use helpyful for studying? (Y / N)
- Educational Apps: List of educational apps used
- Daily Usages: Average daily time spent using mobile phone for educational purposes (Hours)
- Performance Impact: How does mobile phone use impact academic performance? (Agree / Neutral / Strongly Agree)
- Usage Distraction: Does mobile phone use distract from studying? (During Exams / Not Distracting / During Class Lectures / While Studying)
- Attention Span: Has mobile phone use affected attention span? (Y/N)
- Useful Featuures: What features of mobile phones are useful for learning? (e.g. Internet Access, Camera, Calculator, Notes Taking App)
- Health Risks: Are students aware of the potential health risks associated with excessive mobile phone use? (Y / N / Only Partially)
- Beneficial Subject: Which subjects benefit most from mobile phone use? (e.g. Accounting, Bowsing Material, Research)
- Usage Symptoms: Are students experiencing any mental symptoms related to movile phone use? (e.g. Sleep Disturbance, Headaches, Anxiety / Stress, All of These)
- Symptom Frequency: How often are symptoms experiences? (Sometimes / Never / Rarely / Frequently)
- Health Precautions: Are students taking precautions to mitigate potential health risks? (Taking Break During Prolonged Use / Using Blue Light Filter / Limiting Screen Time / None of the Above)
- Health Rating: How would students rate their overall physical and mental health? (Excellent / Good / Fair / Poor)

## EDA:

All columns (besides 'Name') were visualized using a count plot. Upon viewing each graph, the 'Name' and 'Mobile Phone' columns are both revealed to be redundant, as each name is unique and all who participated in the study use a mobile phone.

## Understanding:



## Data Preparation:

1. Cleaned the column names by stripping leading and trailing whitespace
2. Filled in missing data entries with 'unknown'.
3. Changed data type of all columns to 'category' for easier manipulation.
4. Removed 'Name' column.
5. Removed 'Mobile Phone' column.
