# clustering-Text-Mining

### Text Mining and Analysis with NLTK and Scikit-learn

This Jupyter Notebook, `text_mining.ipynb`, is a Python script that performs text mining and analysis on a dataset of comments. The main goal is to preprocess the text and identify the most important and frequently occurring words using techniques like TF-IDF and Count Vectorization.

#### Project Overview

The script is designed for a basic Natural Language Processing (NLP) pipeline. It takes raw text data, cleans it, and then applies two different methods to analyze the content:

  * **TF-IDF (Term Frequency-Inverse Document Frequency):** This method is used to determine the importance of words in a document relative to a collection of documents. The script finds and prints the most important words based on their TF-IDF scores.
  * **Count Vectorization:** This approach simply counts the occurrences of each word in the text. The script uses this to find the most common words.

#### How it Works

1.  **Data Loading:** The script reads a dataset from an Excel file named `Comments.xlsx` using the pandas library.
2.  **Text Preprocessing:** The text data undergoes several cleaning steps:
      * Special characters, punctuation, and numbers are removed.
      * The text is converted to lowercase.
      * Stop words (common words like "the," "is," "and," etc.) are removed using the NLTK library.
      * The remaining words are tokenized and stemmed to their root form.
3.  **Vectorization:** The cleaned text is converted into numerical feature vectors using `TfidfVectorizer` and `CountVectorizer` from scikit-learn.
4.  **Analysis:** The script then analyzes the resulting vectors to identify and print the most important words (from TF-IDF) and the most frequent words (from Count Vectorization).

#### Dependencies

To run this notebook, you need to install the following Python libraries:

  * `pandas`
  * `scikit-learn`
  * `nltk`

You can install these using pip:

```bash
pip install pandas scikit-learn nltk
```

You will also need to download NLTK data, specifically the `stopwords` and `punkt` datasets. You can do this by running a separate Python script with the following lines:

```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
```

#### How to Use

1.  **Prepare your data:** Make sure you have an Excel file named `Comments.xlsx` in the same directory as the notebook. The script assumes the text data is in a column named `comment_text`.
2.  **Install dependencies:** Install all the required libraries and NLTK data as mentioned above.
3.  **Run the notebook:** Open `text_mining.ipynb` in a Jupyter Notebook environment and run all the cells sequentially. The output will display the most important and most frequent words found in your data.
