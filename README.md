# AI Career Recommendation System

An intelligent web application that uses AI to recommend careers based on user interests. The system learns about your interests and provides personalized career recommendations with detailed explanations.

## Features

- **User Authentication**: Secure signup and login system
- **Interest Collection**: Interactive interface to select your interests
- **AI-Powered Recommendations**: Machine learning model that analyzes your interests and matches them with suitable careers
- **Detailed Career Descriptions**: Comprehensive information about each recommended career
- **Explanation System**: Understand why each career was recommended based on your interests
- **Clean Modern UI**: Beautiful, responsive design

## Technology Stack

### Frontend
- HTML5
- CSS3 (with modern styling and animations)
- JavaScript (vanilla JS for API interactions)

### Backend
- Python 3.x
- Flask (web framework)
- SQLite (database)
- JWT (authentication)
- Custom ML model for career matching

## Installation

1. **Clone or download the project**

2. **Install Python dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**:
   ```bash
   python app.py
   ```

4. **Open your browser** and navigate to:
   ```
   http://localhost:5000
   ```

## Project Structure

```
Project/
├── app.py                 # Flask backend application
├── model.py               # Career recommendation ML model
├── requirements.txt       # Python dependencies
├── README.md             # This file
├── index.html            # Main HTML file (all pages)
├── static/
│   ├── css/
│   │   └── styles.css    # Stylesheet
│   └── js/
│       └── app.js        # Frontend JavaScript
└── career_recommendations.db  # SQLite database (created automatically)
```

## How It Works

1. **Introduction Page**: Users are introduced to the system
2. **Signup/Login**: Users create an account or login
3. **Interest Collection**: Users select their interests from a comprehensive list
4. **AI Analysis**: The ML model analyzes user interests and matches them with careers
5. **Recommendations**: Users receive top 5 career recommendations with:
   - Match score percentage
   - Detailed career description
   - Explanation of why the career matches their interests

## API Endpoints

- `POST /api/signup` - Create a new user account
- `POST /api/login` - Login and get JWT token
- `GET /api/interests` - Get list of available interests
- `GET /api/user/interests` - Get user's saved interests
- `POST /api/user/interests` - Save user's interests
- `GET /api/recommendations` - Get career recommendations (requires authentication)

## Database Schema

- **users**: Stores user account information
- **user_interests**: Stores user-selected interests
- **careers**: Stores career information and required interests

## Customization

You can customize the careers database by modifying the `init_default_careers()` function in `app.py` to add more careers or update existing ones.

## Security Notes

- Change the `SECRET_KEY` in production
- Use environment variables for sensitive data
- Consider using a more robust database (PostgreSQL) for production
- Implement rate limiting for API endpoints

## License

This project is open source and available for educational purposes.

