# Student Mental Health Risk

## The Problem

A lot of college students deal with depression, and it affects their grades, motivation, and overall well-being. The hard part is that many of them never reach out for help. The goal was to see if basic info like age, gender, year of study, and GPA could help predict which students might be at risk, so schools could reach out earlier.

This isn't meant to diagnose anyone. It's meant to help counseling centers and advisors spot patterns and plan support.

## The Data

An anonymous survey of 101 university students from Kaggle, with 11 columns covering demographics (gender, age, marital status), academics (course, year, GPA), and mental health (depression, anxiety, panic attacks, and whether they sought treatment).

## What I Found

- About 35% of students said they have depression
- Only 6 out of 101 students had ever seen a specialist for treatment, which really stood out to me
- Most students were in their first year, and the most common GPA range was 3.50 to 4.00
- A chi-square test showed gender was not significantly linked to depression (p = 0.23)
- No single feature had a strong link to depression on its own

## What I Did

- Explored the data with charts on gender, age, GPA, and mental health
- Ran a chi-square test to check if gender and depression were related
- Converted the survey answers into a format the models could use with one-hot encoding
- Split the data 80/20 for training and testing
- Trained and compared four models: Logistic Regression, Decision Tree, Random Forest, and KNN

## Results

| Model | Accuracy |
|---|---|
| Random Forest | 76% |
| Logistic Regression | 71% |
| KNN | 71% |
| Decision Tree | 62% |

Random Forest performed best, so I picked it as the final model.

## Recommendation

Use a model like this once a semester to help counselors spot student groups who may need extra support, with a person always reviewing the results. The bigger takeaway is the treatment gap: most students who struggle never get help, so outreach matters as much as prediction.

## What I'd Improve

- Collect a much bigger dataset, since 101 students is small
- Add features like sleep, workload, and stress levels
- Balance the classes and try models like Gradient Boosting
- Tune each model's settings

## Tools

Python, Pandas, Scikit-learn, Seaborn, Matplotlib, SciPy, Google Colab
