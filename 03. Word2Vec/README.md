# 🌐 Google News Pretrained Word2Vec Model

This project uses the pretrained Google News Word2Vec model, commonly distributed as:

`GoogleNews-vectors-negative300.bin`

The model contains approximately 3 million word and phrase vectors, each with 300 dimensions, learned from Google News text.

## 📥 Download the Model

**Dataset source:** [Google News Vectors — Kaggle](https://www.kaggle.com/datasets/adarshsng/googlenewsvectors)

1. Open the Kaggle dataset page.
2. Download the dataset files.
3. If the downloaded file is compressed, extract it.
4. Ensure that the final binary file is named `GoogleNews-vectors-negative300.bin`.
5. Place it in this folder:

```text
03. Word2Vec/
├── README.md
├── friends-Word2Vec.ipynb
├── game-of-thrones.ipynb
├── on pre trained dataset.ipynb
└── GoogleNews-vectors-negative300.bin
```

The model is very large, so it is intentionally not stored in this GitHub repository. Download it separately only when required by a notebook.

**Important:** Kaggle may package or name the downloaded files differently. Check the downloaded archive and make sure the expected binary model is available before running the relevant notebook.

## ⚙️ Loading the Pretrained Model

Install Gensim if necessary:

```bash
pip install gensim
```

Load the model using:

```python
from gensim.models import KeyedVectors

model = KeyedVectors.load_word2vec_format(
    "GoogleNews-vectors-negative300.bin",
    binary=True
)
```

This loads the pretrained vectors into memory. Because the model is large, loading it may require substantial RAM and time.
