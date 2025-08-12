News Aggregator API
-------------------

The News Aggregator API is a Spring Boot-based application that allows users to register, log in, and fetch personalized news articles based on their preferences. It uses JWT (JSON Web Tokens) for authentication and integrates with external news APIs to fetch news articles.

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

Technologies Used:
1)Spring Boot: Backend framework.

2)Spring Security: Authentication and authorization.

3)JWT (JSON Web Tokens): Token-based authentication.

4)H2 Database: In-memory database for storing user information and preferences.

5)WebClient: For making asynchronous HTTP requests to external APIs.

6)Maven: Dependency management.

7)Postman: API testing.

Setup Instructions
Prerequisites
Java 22.

Maven (for dependency management).

Postman (for testing the API).


