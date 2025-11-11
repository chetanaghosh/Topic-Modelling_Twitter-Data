# Captioning the Discourse : A Proposed Approach to Detect Topics in Tweets concerning the Nirbhaya Rape Case 2012

## 📘 Overview
This project explores public discourse surrounding the 2012 Delhi Nirbhaya case through Twitter data.  
Using computational linguistics and basic natural language processing (NLP) methods, the project examines  
how social media users expressed emotions, attitudes, and key themes over time.

---

## 📊 Data
- **File:** `tweets.json`  
- **Structure:** JSON file containing tweet objects with fields such as `text`, `author`, `createdAt`, and `likeCount`.  
- **Period Covered:** 2012–2013  
- **Source:** X data collected using a free api (twitterapi.io) 

---

## ⚙️ Methodology
1. **Data Loading and Cleaning**
   - Parsed and merged multiple JSON fragments into a single valid dataset.
   - Removed duplicates and null entries.
2. **Preprocessing**
   - Removed links, emojis, punctuations, usernames, numbers, extra spaces, stopwords.
   - Basic language filtering for English tweets.
3. **Exploratory Analysis**
   - Frequency counts and visualization using wordcloud.
4. **Topic Modelling**
   - Used tfidf vectorizer to represent the text in vector format
   - Used KMeans Clustering to cluster tweets around a centroid
  Code for all of the above can be found in the file 'topic_modelling.ipynb'

---

## 🧰 Libraries Used
- `pandas` — data manipulation and cleaning  
- `json` — parsing tweet data  
- `matplotlib` / `seaborn` — visualization  
- `nltk` / `re` — text preprocessing  
- `wordcloud` — visual representation of frequent terms  
- `sklearn` -- vectorization of text and KMeans clustering  

---


## ▶️ How to Run This Project?
- You have to upload the data file to your Google Drive and run the code accordingly
- I tried making a code to fetch data directly using the API key. It only worked for a limited number of tweets. The code is in the Scraping_Twitter_Data file


  ---
  
## 💡 Key Insight and Challenges
- I found each datapoint was assigned a unique cluster and therefore the number of clusters was coming close to 50. We realised this was due to the small size of the dataset. Since our approach included using a free API, we could only collect limited data.
- I have run the code using 6 as our optimal cluster number and identified the top words per cluster


---


## 🔮 Future Work
- It is my intention to run this project with more data
- I also intend to extend this work to create a victim blaming marker that can be used to identify victim blaming in similar discourses


---

## 👩‍💻 Author and Contact

Author: Chetana Ghosh
Email: chetanaghosh7141@gmail.com

----
