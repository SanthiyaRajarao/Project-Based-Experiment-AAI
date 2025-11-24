<H3>ENTER YOUR NAME: SANTHIYA R</H3>
<H3>ENTER YOUR REGISTER NO.: 212223230192</H3>
<H3>DATE:24-11-2025</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
Type your objective based on the question
<H3>Program:</H3>

```python
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

df = pd.read_csv('fb_sentiment.csv')

def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

print(df.head())

positive_feedback = df[df['Label'] == 'P']

print(positive_feedback) 
```
<H3>Output:</H3>
<img width="623" height="754" alt="image" src="https://github.com/user-attachments/assets/8c748f4b-f96d-4e21-b9a9-5379327cec9c" />
<H3>Inference:</H3>
Thus sentiment analysis using Facebook data is done and filtering the data that has only positive feedback for the code is executed successfully.
