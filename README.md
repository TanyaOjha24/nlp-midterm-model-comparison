# Character-Level Language Model Comparison

A comparative study of three language modeling architectures: **Bigram, LSTM, and Transformer**, for character-level next-character prediction using the Tiny Shakespeare dataset.

## Project Overview

This project explores how different NLP architectures learn sequential patterns and generate text. Three models are implemented and evaluated using the same dataset and vocabulary.

The objective is to compare their predictive performance, computational efficiency, and generated text quality.

## Models Implemented

| Model | Architecture | Key Characteristics |
|---|---|---|
| Bigram | Statistical language model | Predicts using the previous character |
| LSTM | Recurrent neural network | Uses hidden and cell states to capture sequential dependencies |
| Transformer | Decoder-only architecture | Uses causal self-attention and positional embeddings |

## Dataset

**Tiny Shakespeare** is a character-level text corpus containing approximately 1.1 million characters.

- Vocabulary size: 65 characters
- Training split: 80%
- Validation split: 20%
- Context length: 128 characters

The dataset is downloaded automatically when the notebook is executed.

## Experimental Results

| Model | Training Loss | Validation Loss | Execution Time |
|---|---:|---:|---:|
| Bigram | 2.4515 | 2.4996 | 0.1043 sec |
| LSTM | 1.2586 | 1.5671 | 65.78 sec |
| Transformer | 1.5916 | 1.8096 | 45.55 sec |

*Note: Bigram execution time represents transition matrix construction, whereas LSTM and Transformer times represent neural network training.*

### Key Findings

- **Bigram:** Fastest to construct but produced the least coherent text.
- **LSTM:** Achieved the lowest validation loss and generated the most coherent text.
- **Transformer:** Used fewer parameters and trained faster than the LSTM, but achieved a higher validation loss in this experiment.

## Repository Structure

```text
nlp-midterm-model-comparison/
├── README.md
├── NLP_Midterm_Model_Comparison.ipynb
├── data/
│   └── README.md
└── results/
    ├── comparison_table.csv
    └── generated_samples.txt
```

## Technologies Used

- Python
- PyTorch
- NumPy
- Pandas
- Matplotlib
- Google Colab
- CUDA and NVIDIA T4 GPU

## Getting Started

1. Clone the repository:

```bash
git clone https://github.com/TanyaOjha24/nlp-midterm-model-comparison.git
cd nlp-midterm-model-comparison
```

2. Install dependencies:

```bash
pip install torch numpy pandas matplotlib
```

3. Open `NLP_Midterm_Model_Comparison.ipynb` in Google Colab or Jupyter Notebook.

4. Run the notebook cells sequentially. The dataset downloads automatically.

A CUDA-compatible GPU is recommended for neural model training.

## Conclusion

The experiment demonstrates how model architecture influences character-level language modeling. While Transformers offer parallel processing and contextual modeling, the LSTM achieved the best predictive performance under the selected experimental settings.

## AI Use Disclosure

AI assistance was used for conceptual explanations, implementation guidance, debugging, and documentation refinement. Model execution, experimental outputs, and result interpretation were reviewed as part of the project workflow.

## Author

**Tanya Ojha**  
MS in Analytics  
Northeastern University
