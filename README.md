#  Mental Health Classifier from Facebook Posts (Depression vs Anxiety vs Stress)

This project allows you to fetch posts from any **public Facebook user or page**, and classify the mental health status (Depression, Anxiety, Stress, Normal) based on the post content using a trained machine learning model.

---

##  Features

-  Scrape latest Facebook posts from public profiles/pages (e.g., celebrities, public figures)
-  Classify posts using TF-IDF + Logistic Regression
-  Confidence score for each prediction
-  Works locally using your own Facebook session cookies

---

##  Demo Screenshot

![Screenshot](Screenshot.png)

---

##  How to Run

### 1. Clone the repo
```bash
git clone https://github.com/your-username/mental-health-fb-classifier.git
cd mental-health-fb-classifier
2. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
If requirements.txt is missing, install manually:

bash
Copy
Edit
pip install facebook_scraper scikit-learn pandas numpy
3. Get Facebook Cookies
To access posts from Facebook, use your own browser cookies:

Open facebook.com

Login and go to Developer Tools → Application → Cookies

Find and copy values for:

c_user

xs

Paste into the cookies dictionary in the Python script:

python
Copy
Edit
cookies = {
    "c_user": "YOUR_C_USER_HERE",
    "xs": "YOUR_XS_HERE"
}
4. Run the script
bash
Copy
Edit
python fb_classifier.py
Enter Facebook page name (e.g., IshaaSahaOfficial)

Enter number of posts to fetch (e.g., 5)

The script will:

Fetch the latest public posts

Classify them into Depression / Anxiety / Stress / Normal

Show prediction with confidence score

 File Structure
bash
Copy
Edit
mental-health-fb-classifier/
│
├── fb_classifier.py          # Main script
├── mental_model.pkl          # Trained ML model (TF-IDF + LogisticRegression)
├── tfidf_vectorizer.pkl      # TF-IDF vectorizer
├── Screenshot.png            # Demo screenshot
├── README.md                 # Project readme
└── requirements.txt          # Python dependencies
 Model Info
Model: Logistic Regression

Input: TF-IDF features from post text

Labels:

Depression

Anxiety

Stress

Normal
