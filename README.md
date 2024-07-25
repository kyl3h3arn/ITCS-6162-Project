# Does Increased Mobile Phone Use Impact Student Health & Academic Performance? Can This Be Predicted?

ITCS 6162 Summer 2024 Project \
Kyle Hearn, M.S. Computer Science Candidate

### Research Question: Does Increased Mobile Phone Use Impact Student Health & Performance?

As mobile phone usage is becoming ever more common in our personal and social lives, it is inevitable that the age of mobile phone use for learning is upon us as well. Is this necessarily a good thing? This project will seek to find and predict an answer to this question based on the Student Health & Academic performance.

## Project Description:

This is a diagnostic and predictive project. It aims to understand the impact of mobile phone usage on students' health and academic performance and to predict outcomes based on usage patterns. By analyzing patterns and relationships in the data, key factors that influence these outcomes can be identified. This understanding can inform educators, parents, and policymakers about the benefits and drawbacks of mobile phone usage in educational settings. 

Using supervised learning with a combination of classification and regression models will allow us to predict the impact of mobile phone use on student health and academic performance effectively. This approach provides a structured method to develop predictive models that can help students and educators make informed decisions based on data-driven insights.

#### Relevant Domain Information:

Two separate studies published in the National Library of Medicine both find correlation between increased mobile phone usage, and increased negative efects on physical and mental wellbeing, as well as performance in the classroom.

**Sources:** https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9368281/ | https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9676861/

## Data Information:

#### Student's Health & Academic Performance

This data set is a single .CSV file and consists of various aspects of mobile phone usage among students, along with their perceived impact on their health and performance. It provides valuable insights into how mobile phones affect students' health, academic performance, and daily activities. It can be used for further analysis to identify trends and correlations between mobile phone usage and its impacts on various aspects of students' lives. 

**Source:** https://www.kaggle.com/datasets/innocentmfa/students-health-and-academic-performance/data

#### Columns:

- Names: Student Names
- Age: Student Ages (Years)
- Gender: Male/Female
- Mobile Phone: Do students own a mobile phone? (Y / N)
- Mobile Operating System: Type of mobile operating system used (e.g. Android, IOS, other)
- Mobile phone use for education: Do students use their mobile phone for educational purposes? (Sometimes / Frequently / Rarely)
- Mobile Phone Activites: List of mobile phone activities used for educational purposes (e.g. Online Research, Educational Apps, Email, Online Learning Platforms)
- Helpful for Studying: Do students find mobile phone use helpful for studying? (Y / N)
- Educational Apps: List of educational apps used.
- Daily Usages: Average daily time spent using mobile phone for educational purposes (Hours)
- Performance Impact: How does mobile phone use impact academic performance? (Agree / Neutral / Strongly Agree)
- Usage Distraction: Does mobile phone use distract from studying? (During Exams / Not Distracting / During Class Lectures / While Studying)
- Attention Span: Has mobile phone use affected attention span? (Y/N)
- Useful Featuures: What features of mobile phones are useful for learning? (e.g. Internet Access, Camera, Calculator, Notes Taking App)
- Health Risks: Are students aware of the potential health risks associated with excessive mobile phone use? (Y / N / Only Partially)
- Beneficial Subject: Which subjects benefit most from mobile phone use? (e.g. Accounting, Bowsing Material, Research)
- Usage Symptoms: Are students experiencing any mental symptoms related to mobile phone use? (e.g. Sleep Disturbance, Headaches, Anxiety / Stress, All of These)
- Symptom Frequency: How often are symptoms experienced? (Sometimes / Never / Rarely / Frequently)
- Health Precautions: Are students taking precautions to mitigate potential health risks? (Taking Break During Prolonged Use / Using Blue Light Filter / Limiting Screen Time / None of the Above)
- Health Rating: How would students rate their overall physical and mental health? (Excellent / Good / Fair / Poor)

## EDA & Understanding:

First, all columns (besides 'Name') were visualized using a count plot. Upon viewing each plot, the following conclusions were made:
- 'Name' and 'Mobile Phone' columns are both revealed to be redundant, as each name is unique and all who participated in the study use a mobile phone.
- Nearly all students find mobile phones useful for studying.
- A majority of students beleive their mobile phones impact their academic performance, either positively or negatively.
- A majority of students beleive their mobile phones affect their attention span.
- A majority of students feel some type of negative symptoms at some point, at varying frequencies. \
**Visualizations:**
![image](https://github.com/user-attachments/assets/67dee11a-b5f6-4c81-bc62-429896271213)
![image](https://github.com/user-attachments/assets/6b0b6cb2-af5c-4588-ab6c-257bdd88b15d)
![image](https://github.com/user-attachments/assets/309ba3f2-ca5e-4b9a-af3e-21bb144f62ee)
![image](https://github.com/user-attachments/assets/aa7aa4e0-88b1-4956-8f8b-569f0cfd02f9)

Next, the 'Daily Usages' category was set against the 'Health Rating', 'Performance Impact', and 'Symptom Frequency' categories, respectively. The following conclusions were made:
- Daily Usage vs. Health Rating: Students with an "Excellent" health rating predominantly use their phones between 2-6 hours daily, with few exceptions going beyond 6 hours. Students with "Good" and "Fair" health ratings show varied usage, extending from less than 2 hours to over 6 hours. Those with a "Poor" health rating tend to use their phones for less than 4 hours daily.
- Daily Usage vs. Performance Impact: Students who "Strongly Agree" and "Agree" that mobile phone usage impacts performance have higher and more variable daily usage. Those who "Disagree" have more consistent and lower daily usage. The "Neutral" group falls in between, with some outliers indicating more than 6 hours of usage.
- Daily Usage vs. Symptom Frequency: Students who "Never" or "Rarely" experience symptoms have similar daily usage patterns, with medians around 4 hours and a wide range of usage times. Those who report experiencing symptoms "Sometimes" tend to have higher daily usage, with a median of around 5 hours and significant spread towards higher usage. \
**Visualizations:**

![image](https://github.com/user-attachments/assets/9d63a207-eb68-4300-a8ac-93ba771dac35)


Next, the 'Health Precautions' category was categorized into binary categories, "yes" or "no", declaring whether or not health precaution(s) were taken by a student. This new category was set against the 'Symptom Frequency' and 'Health Rating' categories, respectively. The following conclusions were made:
- Symptoms Frequency vs Taking Precautions: The median symptom frequency is "Rarely" for both groups, indicating that taking precautions does not significantly alter the frequency of symptoms experienced by students. The variability in symptom frequency is high for both groups, suggesting other factors might be influencing symptom frequency besides taking precautions.
- Health Rating vs Taking Precautions: The median health rating is "Good" for both groups, suggesting that taking precautions does not significantly alter the overall health ratings among students. The variability in health ratings is high for both groups, indicating that health ratings are influenced by multiple factors beyond just taking precautions. \
**Visualizations:**

![image](https://github.com/user-attachments/assets/cf8db57a-af34-496f-8b6a-39aa3217155c)


Finally, the "Mobile Phone Use for Education" category was set against the "Performance Impact" category. The following conclusions were made:
- Students who "Agree" and "Strongly Agree" that mobile phone use impacts performance tend to use their phones more frequently for educational purposes.
- Those who are "Neutral" or "Disagree" show varied and generally lower usage patterns for educational purposes.
- The median usage for education decreases as the agreement with the performance impact statement decreases, suggesting a correlation between higher educational usage of mobile phones and perceived performance impact. \
**Visualization:**

![image](https://github.com/user-attachments/assets/68433043-06a0-4a58-b1a5-3ca6e419a095 )


After the initial data exploration process, the following conclusions can be made about the data set:

**Health:** 
- Increased mobile phone use, particularly more than 4-6 hours daily, is associated with poorer health ratings and more frequent symptoms. 
- Students who take health precautions do not significantly differ in health outcomes from those who do not, suggesting the need for more effective strategies or other influencing factors.

**Academic Performance:** 
- High and variable mobile phone usage correlates with a stronger perception of performance impact, whether positive or negative. 
- Students who use their phones more frequently for educational purposes are more likely to perceive a significant impact on their academic performance.

**Predictability:** 
- Based on the findings above, both health ratings and academic performance impacts could be reasonably predicted. See below for results.

#### Overall Reccomendations:

- Encouraging moderate phone usage (2-4 hours) could potentially lead to better health ratings and lower symptom frequency among students.
- Awareness programs about the impact of high mobile phone usage on health and performance might help students manage their usage better.
- Implementing and promoting health precautions like using blue light filters, taking breaks during prolonged use, and limiting screen time could mitigate health risks associated with mobile phone usage.

## Data Preparation:
The following were made to prepare the data before applying machine learning:
1. Cleaned the column names by stripping leading and trailing whitespace
2. Filled in missing data entries with 'unknown'.
3. Changed data type of all columns to 'category' for easier manipulation.
4. Removed 'Name' column.
5. Removed 'Mobile Phone' column.
