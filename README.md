<H3>ENTER YOUR NAME</H3> PANDEESWARAN N
<H3>ENTER YOUR REGISTER NO.</H3> 212224230191
<H3>DATE:</H3> 20/05/2025
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
Perform sentiment analysis using your Facebook data and count the number of Occurrences of given word in the extracted text for the code given in the following link.
<H3>Program:</H3>

```
import pandas as pd
from textblob import TextBlob

data = pd.read_csv("fb_sentiment.csv")

# Given name to count occurrences

given_word = "kindle"

# Initialize counters for sentiment analysis and name occurrences

sentiment_counts = {'positive': 0, 'negative': 0, 'neutral': 0}
name_occurrences = 0

# Perform sentiment analysis and count occurrences of the given name

for index, row in data.iterrows(): # Perform sentiment analysis
blob = TextBlob(row['FBPost'])
polarity = blob.sentiment.polarity
if polarity > 0:
sentiment_counts['positive'] += 1
elif polarity < 0:
sentiment_counts['negative'] += 1
else:
sentiment_counts['neutral'] += 1

    # Count occurrences of the given name
    name_occurrences += row['FBPost'].lower().count(given_word.lower())

# Print sentiment analysis results

print("Sentiment Analysis Results:")

# Print occurrences of the given name

print(f"Occurrences of '{given_word}': {name_occurrences}")

```
<H3>Output:</H3>

![image](https://github.com/user-attachments/assets/7a744d29-8cee-4b8f-9e38-ba24c44312e0)


<H3>Inference:</H3>
Thus the sentiment analysis using your Facebook data is performed and the number of Occurrences of given word in the extracted text for the code is counted.


