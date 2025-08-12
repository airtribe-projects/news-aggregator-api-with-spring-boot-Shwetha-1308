News Aggregator API
-------------------

The News Aggregator API is a Spring Boot-based application that allows users to register, log in, and fetch personalized news articles based on their preferences. It uses JWT (JSON Web Tokens) for authentication and integrates with external news APIs to fetch news articles.

---------------------

Features:

1)User Authentication:

Register a new user.

Log in with a username and password to receive a JWT token.

2)News Preferences:

Retrieve the logged-in user's news preferences.

Update the logged-in user's news preferences.

3)News Fetching:

Fetch news articles based on the user's preferences.

4)External API Integration:

Integrates with external news APIs (e.g., NewsAPI, GNews) to fetch news articles.

5)Error Handling:

Proper exception handling for invalid requests, authentication errors, and authorization errors.

6)Input Validation:

Validates user registration and news preference updates using Spring's validation annotations.

---------------------------------------------------------------

Technologies Used:

1)Spring Boot: Backend framework.

2)Spring Security: Authentication and authorization.

3)JWT (JSON Web Tokens): Token-based authentication.

4)H2 Database: In-memory database for storing user information and preferences.

5)WebClient: For making asynchronous HTTP requests to external APIs.

6)Maven: Dependency management.

7)Postman: API testing.

-------------------------------------------------------
API Documentation

Base URL

http://localhost:8080

Endpoints

1. Register a New User
   
URL: /api/register

Method: POST

Request Body:

{
   "username": "testuser",
   "password": "testpassword"
}

Response:

 {
     "message": "User registered successfully"
 }
 
2. Log in a User
   
URL: /api/login

Method: POST

Request Body:

  {
      "username": "testuser",
      "password": "testpassword"
  }
  
Response:
    {
        "token": "eyJhbGciOiJIUzI1NiJ9..."
    }
    
3. Get User Preferences
   
URL: /api/preferences

Method: GET

Headers:

Authorization: Bearer <token>

Response:

["sports", "technology"]

4. Update User Preferences
   
URL: /api/preferences

Method: PUT

Headers:

Authorization: Bearer <token>

Request Body:

 ["sports", "technology", "health"]
 
Response:

  "Preferences updated successfully"
  
5. Fetch News Articles
   
URL: /api/news

Method: GET

Headers:

Authorization: Bearer <token>

Response:

  {
      "status": "ok",
      "articles": [
          {
              "title": "News Title 1",
              "description": "News Description 1",
              "source": "News Source 1"
          },
          {
              "title": "News Title 2",
              "description": "News Description 2",
              "source": "News Source 2"
          }
      ]
  }

-----------------------------------------------------------

Testing the API

1)Register a User:

Use the /api/register endpoint to create a new user.

2)Log in:

Use the /api/login endpoint to log in and get a JWT token.

3)Fetch News:

Use the /api/news endpoint with the JWT token to fetch news articles.

4)Update Preferences:

Use the /api/preferences endpoint to update the user's news preferences.

-----------------------------------------------------------------------------

Output:

Check the screenshots for the output.

-----------------------------------------------------------------------------
Optional Features

Caching: Implement a caching mechanism to reduce the number of calls to external news APIs.
