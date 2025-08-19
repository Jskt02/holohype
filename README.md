# Django E-commerce with Cython-optimized Recommendations

This project is a complete, runnable Django e-commerce web application featuring a content-based recommendation system with a performance-critical function optimized using Cython.

## Project Features

- **E-commerce Core**: Product listing, product detail pages, and a session-based shopping cart (add, remove, view, mock checkout).
- **Content-Based Recommendations**:
    - "You may also like" on product detail pages, based on cosine similarity of product tags.
    - "Recommended for You" on the product list page for logged-in users, based on their interaction history (likes/purchases).
- **Cython Optimization**: The cosine similarity calculation is implemented in both pure Python and Cython. The application gracefully falls back to the Python version if the Cython module is not compiled.
- **Demo Data**: Includes a small, realistic dataset (products, users, interactions) and a Django management command to easily populate the database.

## Technology Stack

- **Backend**: Django 5, Python 3.10+
- **Data/AI**: Pandas, NumPy, Cython
- **Database**: SQLite (default)
- **Frontend**: Plain HTML, CSS, and a minimal amount of vanilla JavaScript for AJAX calls.

## Setup and Installation

Follow these steps to get the project running locally.

### 1. Clone the Repository and Set Up a Virtual Environment

```bash
git clone <repository_url>
cd ecommerce_project
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`