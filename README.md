# Natural Language Processing (NLP) Journey 🧠

A hands-on exploration of **Natural Language Processing (NLP)** using Python, machine learning, text processing, and word embeddings. This repository documents my learning journey through practical Jupyter notebooks, experiments, assignments, and real-world text datasets.

The goal is to understand how raw human language can be cleaned, transformed into numerical representations, and used to build intelligent applications.

**Repository:** [Natural Language Processing (NLP)](https://github.com/souhardya-cell/Natural-Language-Processing-NLP-)

---

## 📌 Table of Contents

* [Overview](#-overview)
* [Repository Structure](#-repository-structure)
* [Topics Covered](#-topics-covered)

  * [Text Preprocessing](#1-text-preprocessing)
  * [Text Representation](#2-text-representation)
  * [Word2Vec](#3-word2vec)
  * [Text Classification](#4-text-classification)
  * [POS Tagging](#5-part-of-speech-pos-tagging)
* [Tech Stack](#-tech-stack)
* [Datasets and Pretrained Models](#-datasets-and-pretrained-models)
* [Installation and Setup](#-installation-and-setup)
* [Learning Objectives](#-learning-objectives)
* [Future Learning](#-future-learning)
* [Author](#-author)

---

## 🔍 Overview

Natural Language Processing is a field of Artificial Intelligence that enables computers to work with human language. It combines techniques from linguistics, statistics, machine learning, and deep learning to process and analyse textual data.

This repository follows a practical, step-by-step learning path:

**Raw Text → Text Preprocessing → Numerical Representation → Word Embeddings → Machine Learning Applications**

The notebooks explore fundamental NLP techniques, compare different approaches to text representation, and demonstrate how processed text can be used for tasks such as sentiment analysis and grammatical tagging.

Each folder focuses on a particular stage of the NLP workflow, with implementations and experiments designed to build both conceptual understanding and practical programming skills.

## 📁 Repository Structure

```text
Natural-Language-Processing-NLP/
│
├── 01. Text Preprocessing/
│   ├── Tokenization.ipynb
│   ├── Text Normalisation Techniques.ipynb
│   ├── Stemming & Lemmatization.ipynb
│   ├── Assignment/
│   │   └── Assignment.ipynb
│   ├── IMDB Dataset.csv
│   └── slang.txt
│
├── 02. Text Representation/
│   ├── BoW.ipynb
│   ├── Tf-Idf.ipynb
│   ├── n-grams.ipynb
│   └── Assignment/
│       ├── Assignment.ipynb
│       └── IMDB Dataset.csv
│
├── 03. Word2Vec/
│   ├── README.md
│   ├── friends-Word2Vec.ipynb
│   ├── game-of-thrones.ipynb
│   ├── on pre trained dataset.ipynb
│   ├── Friends_Transcript.txt
│   └── data/
│
├── 04. Text Classification/
│   ├── Imdb sentiment analysis.ipynb
│   ├── imdb using avg Word2Vec.ipynb
│   ├── IMDB Dataset.csv
│   └── X_word2vec.npy
│
├── 05. POS Tagging/
│   └── POS.ipynb
│
├── .gitignore
└── README.md
```

*Note: This is a high-level overview of the main folders. The exact contents may evolve as more notebooks and experiments are added.*

---

## 🧠 Topics Covered

### 1. Text Preprocessing

**Folder:** `01. Text Preprocessing/`

Text preprocessing is the process of converting raw text into a cleaner and more consistent format before analysis or modelling.

Topics and experiments include:

* **Tokenization:** Splitting text into sentences, words, or tokens.
* **Text normalization:** Standardizing text to reduce unwanted variations.
* **Stemming:** Reducing words to their stems using rule-based techniques.
* **Lemmatization:** Reducing words to their linguistically meaningful base forms.
* **Slang handling:** Exploring the normalization of informal language using a slang dictionary.
* **Dataset exploration:** Working with IMDb movie reviews and preparing text for subsequent NLP tasks.

**Objective:** Understand how the quality and representation of textual input can affect downstream NLP workflows.

### 2. Text Representation

**Folder:** `02. Text Representation/`

Machine learning algorithms generally require numerical input. Text representation techniques convert documents into numerical features that algorithms can process.

#### Bag of Words (BoW)

Represents a document using word occurrence or frequency information. It provides a straightforward way to convert text into a document-term matrix.

#### TF-IDF

Term Frequency–Inverse Document Frequency assigns weights based on a term's frequency in a document and its distribution across the collection of documents. It can help highlight terms that are relatively informative for a document.

#### N-grams

N-grams represent consecutive sequences of tokens, such as:

* Unigrams: `natural`
* Bigrams: `natural language`
* Trigrams: `natural language processing`

N-grams can preserve some local word-order information that a basic Bag of Words representation does not capture.

**Objective:** Understand different methods of feature extraction and how they represent textual information for machine learning.

### 3. Word2Vec

**Folder:** `03. Word2Vec/`

Word2Vec is a family of techniques for learning dense vector representations of words from their surrounding context.

Unlike simple word-count representations, word embeddings can capture useful semantic and syntactic relationships learned from text.

Experiments in this folder include:

* Training or exploring Word2Vec representations using text corpora.
* Working with Friends transcript data.
* Exploring text from Game of Thrones.
* Loading and using pretrained word embeddings.
* Examining semantic similarity between word vectors.
* Understanding how word embeddings can support downstream NLP tasks.

#### Word2Vec architectures

* **CBOW (Continuous Bag of Words):** Predicts a target word using its surrounding context.
* **Skip-gram:** Predicts surrounding context words from a target word.

#### Google News pretrained embeddings

The Google News Word2Vec model is commonly distributed as `GoogleNews-vectors-negative300.bin`. It contains approximately 3 million word and phrase vectors, each with 300 dimensions.

The model is large and is not stored directly in this repository.

**Dataset:** [Google News Vectors — Kaggle](https://www.kaggle.com/datasets/adarshsng/googlenewsvectors)

For download instructions, folder contents, and loading examples, see the dedicated [Word2Vec README](03.%20Word2Vec/README.md).

**Objective:** Explore distributed word representations and understand how pretrained embeddings can be used to represent words numerically.

### 4. Text Classification

**Folder:** `04. Text Classification/`

Text classification assigns predefined categories or labels to textual input. One common application is sentiment analysis, where text is classified according to the sentiment it expresses.

This folder focuses on IMDb movie reviews and experiments with text-based features.

Topics include:

* Preparing text data for classification.
* Exploring IMDb movie-review sentiment analysis.
* Using numerical text representations as model inputs.
* Representing documents using average Word2Vec vectors.
* Working with NumPy feature arrays.
* Comparing sparse text features with dense word-embedding representations.

#### Average Word2Vec

One approach to document representation is to combine the vectors of the words in a document, for example by averaging them.

This creates a fixed-length document vector from variable-length text. However, simple averaging does not preserve word order and can lose important contextual information.

**Objective:** Understand how text representations can be used as input features for supervised machine learning tasks.

### 5. Part-of-Speech (POS) Tagging

**Folder:** `05. POS Tagging/`

Part-of-Speech tagging assigns grammatical categories to words based on their usage and context.

Common tags include:

* Noun
* Verb
* Adjective
* Adverb
* Pronoun
* Preposition
* Conjunction

For example:

| Word    | Example POS tag |
| ------- | --------------- |
| The     | Determiner      |
| student | Noun            |
| learns  | Verb            |
| quickly | Adverb          |

The precise tag depends on the tagging scheme and the context of the word.

**Objective:** Explore grammatical analysis and understand how linguistic information can be extracted from text.

---

## 🛠️ Tech Stack

The repository uses Python and its data science ecosystem for experimentation.

| Tool or library  | Purpose                                      |
| ---------------- | -------------------------------------------- |
| Python           | Core programming language                    |
| Jupyter Notebook | Interactive coding and experimentation       |
| Pandas           | Data manipulation and analysis               |
| NumPy            | Numerical operations and array processing    |
| Scikit-learn     | Machine learning and text feature extraction |
| NLTK             | Natural language processing utilities        |
| Gensim           | Word2Vec and pretrained word embeddings      |
| Matplotlib       | Data visualization                           |

Individual notebooks may require additional libraries or language resources depending on the techniques being explored.

---

## 📦 Datasets and Pretrained Models

The repository uses text datasets and pretrained resources for experimentation.

| Dataset or resource            | Application                               |
| ------------------------------ | ----------------------------------------- |
| IMDb Movie Reviews             | Text preprocessing and sentiment analysis |
| Friends transcript             | Word2Vec experiments                      |
| Game of Thrones text           | Word embedding experiments                |
| Google News pretrained vectors | Semantic word representations             |

### Google News Word2Vec model

* **Dataset source:** [Google News Vectors on Kaggle](https://www.kaggle.com/datasets/adarshsng/googlenewsvectors)
* **Common filename:** `GoogleNews-vectors-negative300.bin`
* **Vector dimensions:** 300
* **Vocabulary:** Approximately 3 million words and phrases

Download the model separately if required by a notebook. Extract the archive if necessary and place the binary file in `03. Word2Vec/`.

Large datasets, model binaries, and generated feature files may be excluded from version control to keep the repository manageable. Check the relevant notebook and folder README for any additional setup requirements.

---

## 🚀 Installation and Setup

### Prerequisites

Install the following before running the notebooks:

* Python
* Anaconda or Miniconda (recommended for environment management)
* Jupyter Notebook or JupyterLab
* Git (if cloning the repository)

### Step 1: Clone the repository

Open a terminal or Anaconda Prompt and run:

```bash
git clone https://github.com/souhardya-cell/Natural-Language-Processing-NLP-.git
cd Natural-Language-Processing-NLP-
```

### Step 2: Create a Conda environment

```bash
conda create -n nlp-learning python=3.11
conda activate nlp-learning
```

### Step 3: Install common dependencies

```bash
pip install jupyter pandas numpy scikit-learn nltk gensim matplotlib
```

Some notebooks may need extra packages or downloaded language resources. Install those as indicated in the relevant notebook.

### Step 4: Launch Jupyter

```bash
jupyter notebook
```

Open the folder for the topic you want to explore and run its notebook cells in order.

### Step 5: Download required resources

Some datasets, pretrained models, or generated files are not included in the repository.

For example, if you want to run the pretrained Google News Word2Vec experiment:

1. Open the [Kaggle dataset page](https://www.kaggle.com/datasets/adarshsng/googlenewsvectors).
2. Download the required model files.
3. Extract the archive if needed.
4. Place the model in `03. Word2Vec/`.
5. Check that the notebook's model path matches the downloaded filename.

---

## 🎯 Learning Objectives

Through this repository, I aim to:

* Build a strong foundation in NLP concepts and workflows.
* Understand text cleaning, normalization, stemming, and lemmatization.
* Compare traditional text representation methods such as BoW and TF-IDF.
* Explore n-grams and their role in representing local word context.
* Understand distributed word representations and Word2Vec architectures.
* Experiment with pretrained word embeddings and semantic similarity.
* Apply text representations to sentiment analysis and classification tasks.
* Explore grammatical analysis through POS tagging.
* Strengthen practical Python, data handling, and machine learning skills.

---

## 🔭 Future Learning

As I continue learning NLP, this repository may expand to include:

* Advanced text classification techniques.
* Named Entity Recognition (NER).
* Sequence modelling and recurrent neural networks.
* Attention mechanisms and Transformer architectures.
* Contextual embeddings and modern language models.
* Further experiments in information retrieval and semantic search.

These are future learning directions rather than claims about techniques already implemented in the current notebooks.

---

## 👨‍💻 Author

**Souhardya Chowdhury**

B.Sc. Data Science student interested in Machine Learning, Natural Language Processing, Data Science, and software development.

* [GitHub Profile](https://github.com/souhardya-cell)
* [NLP Repository](https://github.com/souhardya-cell/Natural-Language-Processing-NLP-)

---

## 📌 Repository Status

This is a continuously evolving learning repository. Notebooks, datasets, experiments, and documentation may be updated as I progress through NLP concepts and applications.

**Learn. Implement. Experiment. Improve.**
