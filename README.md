## 📌 What can you do in this cinema?

### 🎥 Watch your favorite films and TV shows
- Catalog of films and TV shows
- Convenient categories, genres, and collections
- High-quality video and adaptive streaming support

### 🔍 Easily find interesting content
- Smart search by title, genre, actors
- Filter by rating and year of release

### ❤️ Create your own cinema
- Add films to "Favorites"
- Create your own playlists and collections

### ⭐ Rate and discuss
- Like films and leave comments
- Find out the average rating from users

### 👥 Watch with friends
- Add friends and share collections
- Chat in private messages
- Create "Watch Parties" to watch films together

### 📩 Receive useful notifications
- New films and popular releases
- Likes to your comments

### 📊 Track your activity
- Viewing history

---

## Features
### 1. Users and authentication
- Registration and login (JWT/OAuth2)
- Password recovery

### 2. Movie and TV series catalog
- Categories, genres, tags
- Filtering, sorting, searching
- Favorites and Collections

### 3. Viewing content
- Adaptive streaming support (HLS, DASH)
- Viewing history

### 4. Review and rating system
- Likes and comments
- Average content rating

### 5. Social
- Friendships
- Messages
- Watch together parties

### 6. Notifications
- Email/Push via Celery
- Notifications about new releases

### 7. Caching and performance
- Popular page caching (Redis)
- Background task processing (Celery) 

### 8. Logging
- Logging of all requests and responses
- Writing errors to the `logs/app.log` file (10 MB rotation)
- Logging of Celery background tasks
- Exception handlers with logging of errors

---

## Technology stack
### **FastAPI**
- Authentication and authorization (JWT/OAuth2)
- Routes for API:
  - Users (registration, login, profile, friendships)
  - Content (films, genres, collections)
  - Ratings, comments
  - Playlists
  - Favorites
  - Messages
  - etc.

### **SQLAlchemy**
- ORM models for all entities:
  - Users
  - Friendship
  - films
  - Playlists
  - Favorites
  - Messages
  - Watch parties
  - etc.
- Repositories and services for separating logic from API
- Alchemical connections (Foreign Keys, Many-to-Many, One-to-Many)
- Migrations from Alembic
- Optimized queries

### **Redis**
- Caching popular queries (movie catalog, ratings)
- Cache for frequently used data
- TTL (Time to Live) for cache
- Storing user sessions

### **Celery**
- Sending email/push notifications (email confirmation, new releases)
- Cleaning outdated data (tokens, cache)
- Scheduled tasks (e.g. updating collections)

### **PostgreSQL**
- Storing all information (films, users, playlists, favorites, etc.)
- Indexes to speed up search

---
