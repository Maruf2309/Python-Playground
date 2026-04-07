# Python-Playground
Programming is Fun!

# 🐍 Python Data Playground

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://python.org)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Imports: isort](https://img.shields.io/badge/%20imports-isort-%231674b1?style=flat&labelColor=ef8336)](https://pycqa.github.io/isort/)
[![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=flat&logo=Jupyter)](https://jupyter.org/try)

> **A production-grade Python toolkit for data enthusiasts** — from data cleaning to visualization and automation.

---

## 📚 Table of Contents

### 🎯 Getting Started
- [Overview](#-overview)
- [Features](#-features)
- [Quick Start](#-quick-start)
- [Installation](#installation)

### 📖 Learning Path: Basic → Advanced

#### 🟢 **BEGINNER LEVEL** *(Weeks 1-3)*

##### Python Fundamentals for Data
- [Variables & Data Types](#variables--data-types) → `basics/01_variables.ipynb`
- [Lists & List Comprehensions](#lists--list-comprehensions) → `basics/02_lists.ipynb`
- [Dictionaries & JSON Data](#dictionaries--json-data) → `basics/03_dictionaries.ipynb`
- [Tuples & Immutable Data](#tuples--immutable-data) → `basics/04_tuples.ipynb`
- [Sets & Unique Values](#sets--unique-values) → `basics/05_sets.ipynb`
- [Control Flow (if/else/loops)](#control-flow) → `basics/06_control_flow.ipynb`
- [Functions & Lambda Expressions](#functions--lambda) → `basics/07_functions.ipynb`
- [Error Handling & Exceptions](#error-handling) → `basics/08_error_handling.ipynb`
- [Basic Coding](#error-handling) → `basics/09_basic_coding.ipynb`
- [Quick Coding](#error-handling) → `basics/10_quick_coding.ipynb`

##### Data Structures & Algorithms
- [Working with Strings](#string-manipulation) → `basics/09_strings.ipynb`
- [File I/O (CSV, JSON, TXT)](#file-io) → `basics/10_file_io.ipynb`
- [List/Dict Comprehensions](#comprehensions) → `basics/11_comprehensions.ipynb`
- [Basic Algorithms (Sort, Search)](#basic-algorithms) → `basics/12_algorithms.ipynb`

#### 🟡 **INTERMEDIATE LEVEL** *(Weeks 4-7)*

##### Data Manipulation & Analysis
- [NumPy Fundamentals](#numpy-fundamentals) → `data_handling/numpy_basics.ipynb`
- [Pandas Series & DataFrame](#pandas-series--dataframe) → `data_handling/pandas_intro.ipynb`
- [Data Cleaning & Preprocessing](#data-cleaning) → `data_handling/cleaner.py`
- [Missing Value Handling](#missing-values) → `data_handling/imputation.ipynb`
- [Outlier Detection & Removal](#outlier-detection) → `data_handling/outliers.ipynb`
- [Data Transformation & Feature Engineering](#feature-engineering) → `data_handling/transformer.py`
- [Merging, Joining & Concatenating](#merging-data) → `data_handling/merging.ipynb`
- [GroupBy & Aggregations](#groupby-operations) → `data_handling/groupby.ipynb`
- [Pivot Tables & Cross Tabs](#pivot-tables) → `data_handling/pivot.ipynb`
- [Time Series Data Handling](#time-series) → `data_handling/time_series.ipynb`

##### Data Visualization
- [Matplotlib Basics](#matplotlib-basics) → `visualization/matplotlib_intro.ipynb`
- [Seaborn Statistical Plots](#seaborn-plots) → `visualization/seaborn_templates.py`
- [Customizing Visualizations](#customizing-plots) → `visualization/styling.py`
- [Subplots & Figure Layouts](#subplots) → `visualization/subplots.ipynb`
- [Plotly Interactive Dashboards](#interactive-plots) → `visualization/interactive.py`
- [Advanced Visualizations (Heatmaps, Pairplots)](#advanced-viz) → `visualization/advanced.ipynb`

##### Automation & Scripting
- [Working with APIs](#api-integration) → `automation/api_fetcher.py`
- [Web Scraping with BeautifulSoup](#web-scraping) → `automation/web_scraper.py`
- [Automated Email Reports](#email-automation) → `automation/email_reporter.py`
- [File & Folder Automation](#file-automation) → `automation/file_organizer.py`
- [Scheduling Tasks](#task-scheduling) → `automation/scheduler.py`
- [Logging & Monitoring](#logging) → `utils/logger.py`

#### 🔴 **ADVANCED LEVEL** *(Weeks 8-12)*

##### Performance Optimization
- [Efficient Pandas Operations](#pandas-performance) → `advanced/performance_optimization.ipynb`
- [Vectorization vs Loops](#vectorization) → `advanced/vectorization.ipynb`
- [Memory Optimization](#memory-optimization) → `advanced/memory_profiling.ipynb`
- [Parallel Processing with Dask](#parallel-processing) → `advanced/dask_parallel.ipynb`
- [Caching & Memoization](#caching) → `advanced/caching_decorators.py`
- [Profiling Code Performance](#profiling) → `advanced/profiling.ipynb`

##### Advanced Data Techniques
- [Working with Large Datasets (Chunking)](#large-datasets) → `advanced/chunking_processing.ipynb`
- [Database Integration (SQL)](#database-integration) → `advanced/sql_alchemy.py`
- [Efficient Data Storage (Parquet, HDF5)](#data-storage) → `advanced/efficient_storage.ipynb`
- [Streaming Data Processing](#streaming-data) → `advanced/streaming_processor.py`
- [Custom Pandas Aggregations](#custom-aggregations) → `advanced/custom_aggregations.py`

##### Object-Oriented Programming for Data
- [Classes for Data Pipelines](#classes-for-data) → `advanced/data_pipeline_class.py`
- [Inheritance & Polymorphism](#inheritance) → `advanced/oo_design.ipynb`
- [Decorators & Context Managers](#decorators) → `advanced/decorators_context.py`
- [Generators & Iterators for Memory Efficiency](#generators) → `advanced/generators.ipynb`
- [Design Patterns for Data Engineering](#design-patterns) → `advanced/design_patterns.py`

##### Testing & Best Practices
- [Unit Testing for Data Code](#unit-testing) → `tests/test_cleaner.py`
- [Test-Driven Development (TDD)](#tdd) → `tests/tdd_example.ipynb`
- [Type Hints & Data Validation](#type-hints) → `utils/validator.py`
- [Documentation with Docstrings](#documentation) → `docs/api.md`
- [Git & Version Control Best Practices](#git-best-practices) → `docs/git_guide.md`

##### Real-World Projects
- [Project 1: E-Commerce Sales Analysis](#project-sales) → `projects/sales_analysis/`
- [Project 2: Customer Segmentation](#project-segmentation) → `projects/customer_segmentation/`
- [Project 3: Time Series Forecasting](#project-forecast) → `projects/time_series_forecast/`
- [Project 4: Automated Data Pipeline](#project-pipeline) → `projects/etl_pipeline/`
- [Project 5: Real-Time Dashboard](#project-dashboard) → `projects/realtime_dashboard/`

### 📚 Reference Sections
- [API Reference](#-api-reference)
- [Utility Functions](#-utility-functions)
- [Configuration & Environment](#-configuration)
- [Testing & Quality](#-testing--quality)

### 🤝 Community
- [Contributing](#-contributing)
- [Author](#-author)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

---

## 🎯 Overview

**Python Data Playground** is a curated collection of Python scripts, Jupyter notebooks, and utilities designed for **data professionals and enthusiasts** who want to:

- ✅ Master Python fundamentals through **data-centric examples**
- ✅ Learn **practical data cleaning** techniques
- ✅ Create **beautiful visualizations** with ready-to-use templates
- ✅ Automate **repetitive data tasks**
- ✅ Build **real-world data projects**
- ✅ Progress from **basic to advanced** concepts systematically

---

## ✨ Features

| Category | Capabilities |
|----------|--------------|
| **📊 Data Handling** | CSV/JSON/Excel/Parquet loading, missing value imputation, outlier detection, type inference |
| **📈 Visualization** | Time series, correlation matrices, distributions, categorical comparisons, regression plots |
| **⚙️ Automation** | File organization, API data fetching, email reporting, scheduled tasks |
| **🧹 Data Cleaning** | Automated pipeline, text standardization, duplicate removal, type fixing |
| **📓 Interactive Learning** | Jupyter notebooks with real datasets, step-by-step tutorials |
| **🔧 Utilities** | Logging, data validation, config management, performance profiling |
| **🚀 Advanced Topics** | Parallel processing, memory optimization, streaming data, custom aggregations |

---


---

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- (Optional) virtualenv/conda for environment management

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/python-data-playground.git
cd python-data-playground

# 2. Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate      # Linux/macOS
# venv\Scripts\activate       # Windows

# 3. Install dependencies
pip install --upgrade pip
pip install -r requirements.txt

# 4. Install development dependencies (optional)
pip install -r requirements-dev.txt

# 5. Set up pre-commit hooks (optional)
pre-commit install

# 6. Verify installation
python -c "import pandas; print(f'Pandas {pandas.__version__}')"
```

# 📖 Learning Path: Detailed Curriculum

🟢 BEGINNER LEVEL *(Weeks 1-3)*
```bash
Variables & Data Types
### basics/variables
- Integers, floats, strings, booleans
- Type conversion and casting
- Working with None/null values
- Constants and naming conventions


Lists & List Comprehensions

### basics/lists
- Creating, indexing, slicing lists
- List methods (append, extend, insert, remove)
- Nested lists for matrix data
- List comprehensions for data filtering
Dictionaries & JSON Data

### basics/dictionaries
- Key-value pair operations
- Dictionary methods (get, update, setdefault)
- Nested dictionaries for hierarchical data
- JSON serialization/deserialization
Control Flow

### basics/control_flow
- Conditional statements for data filtering
- For loops for iteration
- While loops for streaming data
- Break, continue, else clauses
🟡 INTERMEDIATE LEVEL *(Weeks 4-7)*
Pandas Series & DataFrame

### data_handling/pandas_intro
- Creating DataFrames from dicts, lists, files
- Indexing with loc, iloc, at, iat
- Boolean indexing for filtering
- Vectorized operations
Data Cleaning Pipeline

### data_handling/cleaner.py
cleaner = DataCleaner(df)
df_clean = (cleaner
    .handle_missing_values(strategy='auto')
    .remove_outliers(method='iqr', threshold=1.5)
    .standardize_text_columns()
    .fix_data_types()
    .df
)
Visualization Mastery

### visualization/seaborn_templates.py
viz = DataVisualizer()
viz.plot_time_series(df, 'date', 'sales')
viz.plot_correlation_matrix(df.select_dtypes(include='number'))
viz.plot_distribution(df, 'revenue', kind='histogram')

🔴 ADVANCED LEVEL *(Weeks 8-12)*
Performance Optimization

### advanced/performance_optimization.ipynb
### Before: Slow loop
result = []
for i in range(len(df)):
    result.append(df['col1'].iloc[i] + df['col2'].iloc[i])

### After: Vectorized (100x faster)
result = df['col1'] + df['col2']

### Memory optimization
df['category'] = df['category'].astype('category')  # Reduces memory by 90%
Parallel Processing
python
### advanced/dask_parallel.ipynb
import dask.dataframe as dd

### Handle datasets larger than RAM
ddf = dd.read_csv('huge_dataset/*.csv')
result = ddf.groupby('category').amount.mean().compute()
OOP for Data Pipelines
python
### advanced/data_pipeline_class.py
class DataPipeline:
    def __init__(self, source, destination):
        self.source = source
        self.destination = destination
        self.steps = []
    
    def add_step(self, func):
        self.steps.append(func)
        return self
    
    def execute(self):
        data = self.load()
        for step in self.steps:
            data = step(data)
        self.save(data)
        return data
💡 Usage Examples by Skill Level
🟢 Beginner Example


### Load and explore a dataset
from utils.helpers import load_data

df = load_data('data/sample_sales.csv')
print(f"Dataset shape: {df.shape}")
print(f"Columns: {df.columns.tolist()}")
print(df.head())
🟡 Intermediate Example
python
### Complete EDA workflow
from data_handling.cleaner import DataCleaner
from visualization.seaborn_templates import DataVisualizer

### Clean data
cleaner = DataCleaner(df)
df_clean = cleaner.clean()

### Visualize insights
viz = DataVisualizer()
viz.plot_distribution(df_clean, 'sales', kind='histogram')
viz.plot_categorical_comparison(df_clean, 'region', 'sales')

### Generate report
print(cleaner.get_cleaning_report())
🔴 Advanced Example
python
### Production-ready data pipeline
from advanced.data_pipeline_class import DataPipeline
from advanced.caching_decorators import cache, retry
from advanced.parallel_processing import parallel_apply

@pipeline = (DataPipeline('s3://bucket/data', 'postgresql://db')
    .add_step(clean_data)
    .add_step(transform_features)
    .add_step(validate_schema)
    .add_step(parallel_apply(expensive_function))
)

result = pipeline.execute()
``` 

# Development Workflow
```bash
# 1. Fork & clone
git clone https://github.com/yourusername/python-data-playground.git
cd python-data-playground

# 2. Create feature branch
git checkout -b feature/amazing-feature

# 3. Install dev dependencies
pip install -r requirements-dev.txt

# 4. Make changes & test
pytest tests/ -v
black .
isort .

# 5. Commit & push
git commit -m "Add amazing feature"
git push origin feature/amazing-feature

# 6. Open Pull Request

```

### 👨‍💻 Author
Maruf Hossain

`Data Enthusiast & Python Developer`

💼 LinkedIn: [yourprofile](https://www.linkedin.com/in/maruf17/)

📧 Email: maruf.hossain.1997@gmail.com

🐙 GitHub: [github.com/yourusername](https://github.com/Maruf2309)