<h1>MovieHub API</h1>

> This is a web application that allows users to interact with a movie database. Users can perform various actions such as signing up, logging in, searching for movies, rating movies, adding movies to their watchlist, leaving comments on movies, and more. To seed the database with top-rated TV shows, I use data from [The Movie Database (TMDb)](https://www.themoviedb.org/).

## Users:
Individuals who are interested in movies and want to manage their movie-watching experience. They can be movie enthusiasts, casual viewers, or anyone looking to keep track of the movies they watch and interact with movie content.

## Key Functions for Users:
The application helps users manage their movie-watching experience by providing functionalities such as searching for movies, viewing detailed information, rating movies, creating a watchlist, and leaving comments. It simplifies the process of keeping track of movies, offers personalized recommendations based on ratings, and enhances user engagement through comments and watchlist features.

## Key Features:
- User Authentication: Ensures secure access and personalization for each user.
- Movie Management: Allows users to search for movies, view details, and rate them, central to the app’s functionality.
- Watchlist: Helps users track movies they want to watch and manage their viewing priorities.
- Comments: Provides a platform for users to share their thoughts on movies, enhancing community interaction.
- Rating System: Calculates and displays average ratings, providing users with insights into movie popularity and quality.
- Database Interactions: Utilizes SQLAlchemy to manage and interact with the database, ensuring efficient data handling and persistence.

## Personal Contributions:

**S** - The application I developed is a movie management and review platform designed to allow users to interact with a database of movies. Users can sign up, log in, and perform various actions such as rating movies, adding them to a watchlist, and leaving comments. By combining user authentication, movie management, and interactive features like comments and ratings, the application aims to enhance the movie-watching experience.

**T** - The application is structured around a RESTful API built using Flask, with a focus on user interaction and movie management. The design process involved:

- Database Design: I used SQLAlchemy to manage the database schema, defining models for User, Movie, Comment, and the join table user_movie to handle user-movie relationships. This schema supports user authentication, movie management, and comment functionality.

- Blueprints and Routes: I organized the application into blueprints to manage different functionalities:
    - Users Blueprint: Handles user authentication, including signup, login, and logout.
    - Movies Blueprint: Manages movie data, including retrieval, searching, and rating.
    - Comments Blueprint: Allows users to add, edit, and delete comments on movies.
   -  Watchlist Blueprint: Manages the user's watchlist and the status of movies.

**A** - Several RESTful APIs were created: 
- [User Authentication](https://github.com/Hackathon-Python/python_project/blob/main/apis/users.py): Implemented user sign-up and login functionality with hashed passwords using Flask-Login for session management. Routes for user authentication handle input validation, user creation, and login checks.
- [Movie Management](https://github.com/Hackathon-Python/python_project/blob/main/apis/movies.py): Developed routes to retrieve all movies, get details of a single movie, search movies, and allow users to rate movies. The rating system calculates the average rating and updates the movie's local rating.
- [Comments](https://github.com/Hackathon-Python/python_project/blob/main/apis/comments.py): Added functionality for users to leave, edit, and delete comments on movies. Ensured comments are associated with users and movies correctly, and handled exceptions during database operations.
- [Watchlist Management](https://github.com/Hackathon-Python/python_project/blob/main/apis/watchlist.py): Implemented routes to add, remove, and update movies in the user’s watchlist. Included functionality to mark movies as watched and fetch movies based on their watch status.

**R** - The final application provides a platform for movie enthusiasts. Overall, the application offers interactive movie management experience, leveraging Flask and SQLAlchemy to provide functionality and user engagement. The modular design and well-defined API routes ensure scalability and maintainability for future enhancements.

[Check out the MovieHub on GitHub](https://github.com/Hackathon-Python/python_project)

## Technologies
- Language: `Python`
- Database: `SQLite`
- Database Managemant: `SQLAlchemy`
- Server: `Flask`

## Competencies

### JF XX.XX

- List the full text of the job function first
- Describe a situation where you demonstrated this job function.
- Summarize the actions you took to accomplish the goal.
- Emphasize the results of this action for your team or your learning.
- Connect the competentcy to this project

### JF XX.XX

- List the full text of the job function first
- Describe a situation where you demonstrated this job function.
- Summarize the actions you took to accomplish the goal.
- Emphasize the results of this action for your team or your learning.
- Connect the competentcy to this project
