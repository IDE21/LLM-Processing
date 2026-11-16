# NLP & Deep Learning Notebooks (SDAIA LLM Bootcamp)

Five notebooks from the SDAIA LLM Bootcamp. They go from a basic neural network to fine-tuning transformers, including Arabic sentiment analysis with AraBERT.

## Notebooks

| Notebook | Task | Stack | Result in notebook |
|---|---|---|---|
| [`Build-a-basic-classifier.ipynb`](Build-a-basic-classifier.ipynb) | Handwritten digit classification (MNIST) | TensorFlow / Keras | Test accuracy **0.985** |
| [`Text-classification.ipynb`](Text-classification.ipynb) | Movie-review sentiment (word embeddings) | TensorFlow, NLTK | Test accuracy **0.866** |
| [`Model-Fine-Tuning.ipynb`](Model-Fine-Tuning.ipynb) | Paraphrase detection on GLUE MRPC | Hugging Face `transformers`, `datasets` | Accuracy 0.665, F1 0.799 |
| [`Hate-Speech-Detection-with-AraBERT-and-HuggingFace.ipynb`](Hate-Speech-Detection-with-AraBERT-and-HuggingFace.ipynb) | Arabic tweet sentiment (AJGT corpus) | `aubmindlab/bert-base-arabertv02`, PyTorch | Fine-tuned 4 epochs, best model chosen by macro-F1 |
| [`Healthcare-analysis.ipynb`](Healthcare-analysis.ipynb) | Stroke prediction on tabular health data, with class balancing | pandas, imbalanced-learn, Keras | Accuracy 0.840, recall 0.906 (SMOTE applied before the split, so optimistic) |

## Data

- `healthcare-dataset-stroke-data.csv`: the stroke dataset used by `Healthcare-analysis.ipynb`.
- The other notebooks download their data (MNIST, GLUE MRPC, the movie-review CSV) or expect the [AJGT corpus](https://github.com/komari6/Arabic-twitter-corpus-AJGT) cloned next to the notebook.

## Run it

```bash
pip install -r requirements.txt
jupyter notebook
```

A GPU (for example Google Colab) is recommended for the two transformer notebooks.

## License

Code: [MIT](LICENSE). Datasets follow their original licenses.
