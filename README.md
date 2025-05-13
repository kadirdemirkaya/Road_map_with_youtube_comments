# YouTube Comments Road Evaluation

This project analyzes YouTube video comments. The ultimate goal is to help creators make historically accurate, engaging, and audience-aligned videos by creating a **data-driven roadmap** based on viewer sentiment.


### 🎯 Project Objective

- **Input**: A YouTube video link
- **Output**: A structured roadmap based on clustered negative comments
- **Purpose**: Detect common complaints from viewers and guide future video production accordingly


### 🧠 Technologies Used

- **YouTube Data API v3**: To fetch video comments
- **Custom Text Cleaning Functions**: For multilingual pre-processing (English + Turkish)
- **Sentiment Analysis**:
  - Custom-trained **English sentiment model**
  - Language support for **both Turkish and English**
- **Embedding & Clustering**:
  - Sentence embeddings via paraphrase-MiniLM-L6-v2
  - Comment grouping with **K-Means Clustering**
- **Recommendation System**:
  - Powered by **Gemini (LLM)** to produce smart, human-like suggestions based on clustered comment content


### 🧪 Methodology

#### 1. **Comment Extraction**  
   - YouTube comments are retrieved using the YouTube Data API v3.

#### 2. **Cleaning & Preprocessing**  
   - All comments are cleaned using language-specific `clean_text` methods (e.g., punctuation removal, stopwords, etc.).

#### 3. **Sentiment Detection**  
   - A custom sentiment model filters out **negative comments** for further analysis.

#### 4. **Vectorization & Clustering**  
   - Remaining negative comments are embedded using SentenceTransformer.
   - K-Means clustering groups similar comments to detect common issues.

#### 5. **Recommendation Generation**  
   - Gemini LLM analyzes the themes from each cluster and generates improvement suggestions for the content creator.


### 🔍 Key Use Cases

- **Content Feedback Loop**: Provide YouTubers with actionable insights from negative feedback.
- **Multilingual Support**: Process both Turkish and English comments natively.
- **Roadmap Creation**: Help producers understand what to improve in the next video (e.g., historical accuracy, character development, tone).


### 📦 Dependencies

#### To run the project, make sure to install the following Python libraries:
- pip install sentence-transformers
- pip install scikit-learn
- pip install transformers
- pip install langid
- pip install nltk
- pip install stop-words



### 🚀 Future Work
- Support other languages to broaden reach
