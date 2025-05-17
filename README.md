# Matrimonial Recommendation System

This project is a collaborative filtering-based recommendation system built using TensorFlow and Flask. It recommends matrimonial profiles based on user preferences like gender, occupation, age, religion, and marital status.

## Features

- Collaborative Filtering using Embedding Layers
- TensorFlow-based model trained on interaction data
- REST API built with Flask
- JSON-based profile data
- Returns top 10 recommended profiles for a given user input
- CORS enabled for frontend integration

## Project Structure

├── app.py # Flask backend API

├── matrimony_recommender_model.h5 # Trained recommendation model

├── gender_mapping.pkl # Pickle file for gender mapping

├── occupation_mapping.pkl # Pickle file for occupation mapping

├── user_mapping.pkl # Pickle file for user mapping

├── profile_mapping.pkl # Pickle file for profile mapping

├── data1.json # Profile data used in recommendations

├── requirements.txt # Required Python libraries


## API Endpoint

### `POST /recommend`

#### Request Body

```json
{
  "user_id": 1,
  "gender": "Male",
  "occupation": "Engineer",
  "age": 28,
  "religion": "Hindu",
  "maritalStatus": "Single"
}

[
  {
    "profile_id": 3,
    "match_percentage": 89.5,
    "name": "Priya",
    "occupation": "Doctor",
    "maritalStatus": "Single",
    "caste": "Brahmin",
    "interests": ["Reading", "Cooking"],
    ...
  },
  ...
]




