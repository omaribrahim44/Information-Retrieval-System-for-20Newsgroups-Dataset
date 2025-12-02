# Information Retrieval System for 20 Newsgroups Dataset

A comprehensive information retrieval system implementing and comparing three retrieval models on the 20 Newsgroups dataset:
- **Vector Space Model (VSM)** with TF-IDF
- **BM25** (Best Matching 25) - Probabilistic ranking
- **Boolean Retrieval** with soft matching

## ⚡ Quick Start

```bash
# Clone the repository
git clone https://github.com/omaribrahim44/Information-Retrieval-System-for-20Newsgroups-Dataset.git
cd Information-Retrieval-System-for-20Newsgroups-Dataset

# Install dependencies
pip install -r requirements.txt

# Download NLTK data
python -c "import nltk; nltk.download('wordnet'); nltk.download('omw-1.4')"

# Launch Jupyter Notebook
jupyter notebook
```

Then open `IR PROJECT.ipynb` and run all cells (`Cell` → `Run All`)

## 📋 Features

### Retrieval Models
- Vector Space Model with TF-IDF and cosine similarity
- BM25 implementation with configurable parameters (k1=1.5, b=0.75)
- Boolean retrieval with AND/OR/NOT operators and soft matching fallback

### Evaluation Metrics
- Precision@k (k=5, 10, 20)
- Recall@k (k=5, 10, 20)
- Average Precision (AP)
- Mean Average Precision (MAP)

### Analysis
- Per-category performance analysis
- Failure analysis (queries with AP < 0.2)
- Query length impact analysis

### Visualizations
- Precision@k comparison plots
- Recall@k comparison plots
- MAP comparison bar charts

### Export
- Detailed CSV exports of all metrics
- Aggregated results summaries
- Automated markdown report generation
- High-resolution plots (300 DPI)

## 🚀 Installation

### Prerequisites
- Python 3.7 or higher
- pip package installer

### Step 1: Clone the Repository
```bash
git clone https://github.com/omaribrahim44/Information-Retrieval-System-for-20Newsgroups-Dataset.git
cd Information-Retrieval-System-for-20Newsgroups-Dataset
```

### Step 2: Install Required Packages
```bash
pip install -r requirements.txt
```

This installs:
- `numpy` - Numerical computing
- `pandas` - Data manipulation
- `scikit-learn` - Machine learning (TF-IDF, cosine similarity)
- `nltk` - Natural language processing
- `matplotlib` - Visualization
- `wordcloud` - Word cloud generation
- `jupyter` - Notebook environment

### Step 3: Download NLTK Data
```bash
python -c "import nltk; nltk.download('wordnet'); nltk.download('omw-1.4')"
```

## 📖 Usage

### Running the Notebook

1. **Start Jupyter**:
   ```bash
   jupyter notebook
   ```

2. **Open the notebook**: Click on `IR PROJECT.ipynb`

3. **Run all cells**: `Cell` → `Run All` (or `Shift + Enter` for each cell)

### Notebook Structure

- **Cells 1-43**: Data loading, preprocessing, and basic retrieval models
- **Cells 44-70**: BM25 implementation and comprehensive analysis

⚠️ **Important**: Run cells sequentially from top to bottom!

### Viewing Results

After running the notebook, results are saved in `ir_outputs/`:
- `evaluation_detailed.csv` - Per-query metrics
- `evaluation_summary.csv` - Aggregated metrics
- `category_performance.csv` - Per-category analysis
- `evaluation_report.md` - Summary report
- `plots/` - Visualization images

## 📊 Dataset

**20 Newsgroups Dataset** - 5 categories:
- `alt.atheism`
- `comp.graphics`
- `rec.sport.baseball`
- `sci.med`
- `talk.politics.misc`

**Total documents**: 4,531  
**Download**: Automatic on first run (~14 MB)

## 📁 Project Structure

```
.
├── IR PROJECT.ipynb       # Main Jupyter notebook
├── README.md              # This file
├── requirements.txt       # Python dependencies
├── .gitignore             # Git ignore rules
└── ir_outputs/            # Generated results (created when run)
    ├── *.csv              # Evaluation metrics
    ├── *.md               # Reports
    └── plots/             # Visualization plots
```

## ⏱️ Expected Runtime

- **Full notebook**: ~5-10 minutes
- **BM25 evaluation**: ~2-3 minutes
- **Visualizations**: ~10-15 seconds
- **First run**: Longer due to dataset download

## 🐛 Troubleshooting

### Common Issues

**`ModuleNotFoundError: No module named 'sklearn'`**
```bash
pip install scikit-learn
```

**`LookupError: Resource wordnet not found`**
```bash
python -c "import nltk; nltk.download('wordnet'); nltk.download('omw-1.4')"
```

**`NameError: name 'evaluation_queries' is not defined`**
- Solution: Run all cells from the beginning (cells 1-43 must run first)

**Plots not displaying**
```bash
pip install matplotlib
```

### Performance Tips
- Close other applications to free memory
- Requires ~500 MB RAM
- First run downloads dataset automatically

## 🔍 Key Implementation Details

### BM25 Scoring
```python
def bm25_score(query_terms, doc_id, k1=1.5, b=0.75):
    # Term frequency saturation (k1)
    # Document length normalization (b)
    # IDF with smoothing
```

### Evaluation Framework
```python
def evaluate_all_models(queries, relevant_docs, k_values=[5, 10, 20]):
    # Evaluates VSM, BM25, and Boolean retrieval
    # Returns DataFrame with comprehensive metrics
```

## 📈 Results

The notebook generates:
- **Metrics**: Precision, Recall, AP, MAP for all three models
- **Plots**: Performance comparison visualizations
- **Analysis**: Category breakdown, failure analysis, query length impact
- **Reports**: Automated markdown summaries

## 🎓 Academic Context

Developed for an Information Retrieval course, demonstrating:
- Classical IR models (VSM, Boolean)
- Modern probabilistic ranking (BM25)
- Comprehensive evaluation methodologies
- Performance analysis and visualization

## 📄 License

This project is for educational purposes.

## 🤝 Contributing

This is an academic project. For questions or suggestions, please open an issue.

---

**Repository**: https://github.com/omaribrahim44/Information-Retrieval-System-for-20Newsgroups-Dataset  

