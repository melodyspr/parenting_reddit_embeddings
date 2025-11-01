Parenting Reddit Embeddings

This repository contains the code used to train word embeddings on Reddit discussions about parenting.
It reproduces the analyses published in:
Sepahpour-Fard, M., Quayle, M., Schuld, M., & Yasseri, T. (2023)
Using word embeddings to analyse audience effects and individual differences in parenting Subreddits.
EPJ Data Science, 12(1), 38.
https://epjds.epj.org/articles/epjdata/abs/2023/01/13688_2023_Article_412/13688_2023_Article_412.html

📘 Overview
The notebook full_code_parenting_reddit_embeddings.ipynb preprocesses Reddit comments collected from several parenting-related subreddits and trains author-aware word embeddings to analyze audience effects and individual differences in parenting discourse.

🧩 Key steps
Data loading
Imports comments from multiple subreddits:
r/Daddit (fathers)
r/Mommit (mothers)
r/Parenting threads focused on fathers and mothers
Cleaning and filtering
Removes deleted and AutoModerator comments
Removes authors active in both a mothers’ and a fathers’ subreddit
Normalizes frequent multiword terms (e.g., “post partum” → “postpartum”)
Text preprocessing
Tokenizes text
Generates bigrams and trigrams
Removes stopwords
Applies lemmatization
Inserts “agent” tokens to distinguish user-specific tokens
Embedding training
Trains Word2Vec models using Gensim on the preprocessed text
Monitors loss and convergence during training
Produces cleaned text files and trained embedding models for downstream linguistic and semantic analysis

⚙️ Dependencies
The notebook requires the following Python libraries:
pandas
numpy
gensim
matplotlib
seaborn
scikit-learn
nltk
tqdm
adjustText

📄 Citation
If you use this code or reproduce the analyses, please cite:
@article{sepahpour2023using,
  title={Using word embeddings to analyse audience effects and individual differences in parenting Subreddits},
  author={Sepahpour-Fard, Melody and Quayle, Michael and Schuld, Maria and Yasseri, Taha},
  journal={EPJ Data Science},
  volume={12},
  number={1},
  pages={38},
  year={2023},
  publisher={Springer Berlin Heidelberg}
}
