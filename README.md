# InfoBuddy

InfoBuddy is a simple chatbot application consisting of a frontend built using HTML, CSS and Vanilla JavaScript and a backend powered by Spring Boot. This application allows users to interact with the chatbot, with the backend processing the user queries and providing responses.

## Features
- **Interactive Frontend**: A clean and simple chatbot interface built using HTML.
- **Spring Boot Backend**: Handles user queries and integrates with the Gemini AI API for intelligent responses.
- **Real-Time AI Integration**: Uses the Gemini AI model for advanced conversational capabilities.

## Prerequisites
Before running the project, ensure you have the following installed:
- Java 17 or above
- Maven
- Spring Boot 2.x
- A Gemini API key (details below)
- A browser to test the frontend (`chatbot.html`)

## Project Setup

### Step 1: Clone the Repository
Clone the project from GitHub:
```bash
git clone https://github.com/SubediBinod/Gemini-Chatbot.git
```
### Step 2: Create a Gemini API Key
- Visit the Gemini API Documentation to sign up for an account.
- Once logged in, navigate to the API Keys section and create a new API key.
- Copy your API key. You will need it for the backend configuration.

### Step 3: Configure the Backend
- Open the AIService class in the backend project.
- Update the following constants with your API details
  private static final String GEMINI_MODEL = "gemini-1.5-flash";
 private static final String API_KEY = "your-gemini-api-key"; // Paste your Gemini API Key here

-Open WebConfig and update the following constraints
@Override
            public void addCorsMappings(CorsRegistry registry) {
                registry.addMapping("/api/**")
                        .allowedOrigins("http://localhost:8084") // Paste your portnumber here 
                        .allowedMethods("GET", "POST", "PUT", "DELETE", "OPTIONS")
                        .allowedHeaders("*")
                        .allowCredentials(true);
            }

-Save the changes

### Step 4: Build and Run the Backend
- The backend will start running on http://localhost:8080

### Step 5: Set Up the Frontend
-Run the Frontend 

### Step 6: Test the Chatbot
- Interact with the chatbot through the frontend.
- Verify that the backend communicates with the Gemini API to generate responses.

  ##Screenshot
  ![chatbot](https://github.com/user-attachments/assets/e46ea3a4-73d1-498f-b549-902e84eeb5d8)

  ## Contribution
### We welcome contributions to improve the Gemini Chatbot! To contribute:

- Fork the repository.
- Create a new branch (git checkout -b feature-branch).
- Commit your changes (git commit -m 'Add some feature').
- Push to the branch (git push origin feature-branch).
- Open a pull request.



