# Information Retrieval Project - Enhanced with BM25

This project implements and compares three information retrieval models on the 20 Newsgroups dataset:
- **Vector Space Model (VSM)** with TF-IDF
- **BM25** (Best Matching 25) - Probabilistic ranking
- **Boolean Retrieval** with soft matching

## ⚡ Quick Start

```bash
# 1. Clone the repository
git clone <your-repo-url>
cd <repo-name>

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download NLTK data (in Python)
python -c "import nltk; nltk.download('wordnet'); nltk.download('omw-1.4')"

# 4. Start Jupyter and run the notebook
jupyter notebook "IR PROJECT.ipynb"
```

Then in Jupyter: `Cell` → `Run All`

## 📋 Features

### Retrieval Models
- ✅ Vector Space Model with TF-IDF and cosine similarity
- ✅ BM25 implementation with configurable parameters (k1, b)
- ✅ Boolean retrieval with AND/OR/NOT operators and soft matching fallback

### Evaluation & Analysis
- ✅ Comprehensive evaluation framework
  - Precision@k (k=5, 10, 20)
  - Recall@k (k=5, 10, 20)
  - Average Precision (AP)
  - Mean Average Precision (MAP)
- ✅ Per-category performance analysis
- ✅ Failure analysis (queries with AP < 0.2)
- ✅ Query length impact analysis

### Visualizations
- ✅ Precision@k comparison plots
- ✅ Recall@k comparison plots
- ✅ MAP comparison bar charts
- ✅ Per-category performance visualizations

### Export & Reporting
- ✅ Detailed CSV exports of all metrics
- ✅ Aggregated results summaries
- ✅ Automated markdown report generation
- ✅ High-resolution plots (300 DPI)

## 🚀 Getting Started

### Prerequisites

**Python Version**: Python 3.7 or higher

**Required Packages**:
```bash
pip install numpy pandas scikit-learn nltk matplotlib wordcloud jupyter
```

**Or install all at once**:
```bash
pip install -r requirements.txt
```

**Download NLTK Data** (required for text preprocessing):
```python
import nltk
nltk.download('wordnet')
nltk.download('omw-1.4')
```

### Installation Steps

1. **Clone the repository**:
   ```bash
   git clone <your-repo-url>
   cd <repo-name>
   ```

2. **Install dependencies**:
   ```bash
   pip install numpy pandas scikit-learn nltk matplotlib wordcloud jupyter
   ```

3. **Download NLTK data** (run in Python):
   ```python
   import nltk
   nltk.download('wordnet')
   nltk.download('omw-1.4')
   ```

### Running the Notebook

1. **Start Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

2. **Open the notebook**:
   - Navigate to `IR PROJECT.ipynb` in the Jupyter interface
   - Click to open

3. **Run all cells**:
   - Option 1: Click `Cell` → `Run All` in the menu
   - Option 2: Run cells sequentially using `Shift + Enter`
   
   **Important**: Run cells in order from top to bottom!
   - Cells 1-43: Setup, preprocessing, and basic retrieval
   - Cells 44-70: BM25 implementation and enhanced analysis

4. **View results**:
   - Check visualizations in `ir_outputs/plots/`
   - Review CSV files in `ir_outputs/`
   - Read the summary report: `ir_outputs/evaluation_report.md`

### Expected Runtime

- **Full notebook execution**: ~5-10 minutes
- **BM25 evaluation** (Cell 52): ~2-3 minutes
- **Visualization generation**: ~10-15 seconds

## 📊 Dataset

**20 Newsgroups Dataset** - 5 selected categories:
- `alt.atheism`
- `comp.graphics`
- `rec.sport.baseball`
- `sci.med`
- `talk.politics.misc`

Total documents: 4,531

## 📁 Project Structure

```
.
├── IR PROJECT.ipynb              # Main Jupyter notebook
├── README.md                     # This file
├── .gitignore                    # Git ignore rules
├── Infor Retrieval Final project report.pdf
├── Information retrieval project.pdf
└── ir_outputs/                  # Generated results (created when run)
    ├── evaluation_detailed.csv
    ├── evaluation_summary.csv
    ├── category_performance.csv
    ├── map_scores.csv
    ├── evaluation_report.md
    └── plots/
        ├── precision_comparison.png
        ├── recall_comparison.png
        └── map_comparison.png
```

## 🔍 Key Components

### BM25 Implementation
```python
def bm25_score(query_terms, doc_id, k1=1.5, b=0.75):
    # Computes BM25 score with:
    # - Term frequency saturation (k1)
    # - Document length normalization (b)
    # - IDF with smoothing
```

### Evaluation Framework
```python
def evaluate_all_models(queries, relevant_docs, k_values=[5, 10, 20]):
    # Evaluates VSM, BM25, and Boolean retrieval
    # Returns DataFrame with all metrics
```

## 📈 Results

The notebook generates comprehensive results including:
- **Performance Metrics**: Precision, Recall, AP, MAP for all models
- **Visualizations**: Comparison plots showing model performance
- **Analysis**: Per-category breakdown, failure analysis, query length impact
- **Reports**: Automated markdown summary with key findings

## 📚 Documentation

All documentation is included in the Jupyter notebook with detailed markdown cells explaining each section.



## 📝 Important Notes

- ⚠️ **Run cells sequentially**: The notebook must be run from top to bottom
- ⚠️ **Prerequisites required**: Cells 1-43 must be executed before cells 44-70
- ⏱️ **Evaluation time**: The comprehensive evaluation (Cell 52) takes ~2-3 minutes
- 💾 **Output location**: All results are saved to `ir_outputs/` directory
- 📊 **Dataset download**: The 20 Newsgroups dataset (~14 MB) downloads automatically on first run

## 🐛 Troubleshooting

### Common Issues

**Issue**: `ModuleNotFoundError: No module named 'sklearn'`
```bash
# Solution: Install scikit-learn
pip install scikit-learn
```

**Issue**: `LookupError: Resource wordnet not found`
```python
# Solution: Download NLTK data
import nltk
nltk.download('wordnet')
nltk.download('omw-1.4')
```

**Issue**: `NameError: name 'evaluation_queries' is not defined`
```
Solution: Run all cells from the beginning (cells 1-43 first)
```

**Issue**: Plots not displaying
```bash
# Solution: Ensure matplotlib is installed
pip install matplotlib
# If using Jupyter, add this to a cell:
%matplotlib inline
```

### Performance Tips

- Close other applications to free up memory
- The dataset requires ~500 MB RAM
- Evaluation of 50 queries processes ~4,500 documents each
- First run takes longer due to dataset download

## 🎓 Academic Context

This project was developed as part of an Information Retrieval course, demonstrating:
- Classical IR models (VSM, Boolean)
- Modern probabilistic ranking (BM25)
- Comprehensive evaluation methodologies
- Performance analysis and visualization

## 📄 License

This project is for educational purposes.

## 🤝 Contributing

This is an academic project. For questions or suggestions, please open an issue.

---

**Last Updated**: December 2, 2024
