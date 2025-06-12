CinePredict
CinePredict: Flask web app with AI-powered movie recommendations via chatbot. Uses SentenceTransformers for semantic matching, spaCy for keyword extraction, and Tailwind CSS for a responsive UI. Discover films by story or genre/rating.
Table of Contents

Features
Installation
Usage
Project Structure
Technologies Used
Contributing
License
Acknowledgments

Features

AI-Driven Recommendations: Uses SentenceTransformers (all-mpnet-base-v2) for semantic similarity and spaCy (en_core_web_sm) for keyword extraction.
Story-Based Matching: Input a plot description to find similar movies.
Genre & Rating Filters: Filter by genre (e.g., Action) and minimum rating (e.g., 7.0).
Responsive UI: Styled with Tailwind CSS, supporting dark mode.
Interactive Chatbot: User-friendly interface for movie discovery.
Data Pipeline: Scripts to fetch movie data from TMDB and generate embeddings.

Installation
Prerequisites

Python 3.8+
pip
Git
TMDB API key (get one at TMDB)
Node.js (optional, for Tailwind CSS build if not using CDN)

Setup

Clone the Repository
git clone https://github.com/AHSAN-MEHMOOD/Movie-Recommendation-Chatbot_AI.git
cd Movie-Recommendation-Chatbot_AI


Create and Activate Virtual Environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate


Install Dependencies
pip install -r requirements.txt
python -m spacy download en_core_web_sm


Fetch Movie Data

Add your TMDB API key to fetch_movie_data.py:
TMDB_API_KEY = "your_tmdb_api_key_here"


Run:
python fetch_movie_data.py




Generate Embeddings

Run:
python generate_embeddings.py




Run the App
python app.py


Visit http://localhost:5000.



Usage

Open the Web App

Navigate to http://localhost:5000 to see featured movies.


Use the Chatbot

Click "CinePredict AI" (bottom-right) to open the chatbot.
Type story and describe a plot (e.g., "A hacker in a simulated reality").
Type genre to filter by genre (e.g., "Action") and rating (e.g., "7.0").
Follow prompts to refine your query.


View Recommendations

Movies appear in a styled list, each on a separate line (e.g., "- The Matrix (Rating: 8.7)").



Project Structure
Movie-Recommendation-Chatbot_AI/
├── static/
│   blog.html  # HTML template with Tailwind CSS and jQuery
├── app.py                   # Flask backend with AI recommendation logic
├── fetch_movie_data.py      # Script to fetch movie data from TMDB
├── generate_embeddings.py   # Script to generate embeddings
├── movies_cleaned.csv       # Movie dataset (generated)
├── embeddings.npy           # Precomputed embeddings (generated)
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation

Technologies Used

Backend:
Flask: Web framework
SentenceTransformers (all-mpnet-base-v2): Semantic similarity
spaCy (en_core_web_sm): Keyword extraction
pandas & numpy: Data handling
scikit-learn: Cosine similarity
requests: TMDB API calls


Frontend:
Tailwind CSS: Responsive styling via CDN
jQuery: AJAX and DOM manipulation
HTML/CSS/JavaScript: UI and interactivity


Environment:
Python 3.8+
Browser-compatible



Contributing

Fork the repository.

Create a branch:
git checkout -b feature/your-feature


Commit changes:
git commit -m "Add your feature"


Push:
git push origin feature/your-feature


Open a pull request.


Adhere to PEP 8 for Python code and include tests/documentation.
License
MIT License. See LICENSE for details.
Acknowledgments

Flask
SentenceTransformers
spaCy
TMDB API
Tailwind CSS

