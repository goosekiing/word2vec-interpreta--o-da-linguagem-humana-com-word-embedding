# Word2Vec: Interpretação da Linguagem Humana com Word Embedding

This repository contains a project focused on using Word2Vec for interpreting human language through word embedding. The project uses a dataset with titles and texts of news articles in Brazilian Portuguese from various websites, classified into categories: columns, daily life, sports, illustrated, market, and world. The challenge proposed in the project is to create a news classifier that receives the title of the news article as input and determines its category.

## Project Overview

### Data and Preprocessing
- **Dataset:** Titles and texts of news articles in Brazilian Portuguese, classified into different categories.
- **Source:** Models of Word Embeddings from NILC (Interinstitutional Center for Computational Linguistics) composed of researchers from different Brazilian universities such as USP and UFSCar. Pre-trained models in Brazilian Portuguese are available for download [here](http://nilc.icmc.usp.br/nilc/index.php/repositorio-de-word-embeddings-do-nilc).

### Word Embeddings
- **Models Used:**
  - **CBOW (Continuous Bag of Words) with 100 and 300 dimensions:** Predicts the target word using the context and is generally faster.
  - **SKIP-GRAM with 300 dimensions:** Predicts the context using the target word and performs better with rare words.
- **Vector Representation:** The vectors representing the words in the news titles are summed. This method combines the individual semantic information of each word, capturing the collective meaning of the words in the phrase.

### Model Training
- **Logistic Regression:** A LogisticRegression model is trained with the resulting vectors from the title processing, achieving an accuracy rate of 80% for the CBOW model and 81% for the SKIP-GRAM model.

## Course Details
This project was completed as part of the 'Advanced Machine Learning' course on Alura. For more information about the course, visit [Alura](https://cursos.alura.com.br/formacao-machine-learning-avancada).

## Objectives Achieved
- Learn how to represent words with One-hot encoding, including its advantages and disadvantages.
- Understand what Word2Vec is and its benefits.
- Use pre-trained Word2Vec models.
- Comprehend the impacts of biases in Word2Vec models.
- Combine word vectors to represent and classify texts.

## Technologies Used
- Python (v3.11.4)
- Jupyter Notebook
- Numpy
- Pandas
- Scikit-learn
- Gensim
- NLTK

## Project Structure
The directory structure of the project is as follows:
```
word2vec-interpretação-da-linguagem-humana-com-word-embedding/
│   database-test-project-07.csv        
│   database-train-project-07-part-1.csv
│   database-train-project-07-part-2.csv
│   database-train-project-07-part-3.csv  # Training files split to meet GitHub file size limits
│   project-07.ipynb
│   README.md
```

## Setup Instructions
1. Clone the repository:
   ```sh
   git clone https://github.com/goosekiing/word2vec-interpretação-da-linguagem-humana-com-word-embedding.git
   ```
2. Navigate to the project directory:
   ```sh
   cd word2vec-interpretação-da-linguagem-humana-com-word-embedding
   ```
3. Create a virtual environment and activate it:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```
4. Install the required libraries:
   ```sh
   pip install numpy pandas scikit-learn gensim nltk
   ```
5. Download additional NLTK data (if not already done):
   ```python
   import nltk
   nltk.download('all')  # Uncomment and run this in the notebook if needed
   ```

## Running the Notebook
1. Open Jupyter Notebook:
   ```sh
   jupyter notebook
   ```
2. Run the `project-07.ipynb` notebook to see the news classification model in action.

## Language
The language used in this project is Brazilian Portuguese (pt-br).

## Author
GitHub Username: [goosekiing](https://github.com/goosekiing)
