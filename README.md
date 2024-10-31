## Movie Recommender Bot with OpenAI, spaCy, Whisper, and TMDb

    This project is a movie recommendation bot powered by LangChain and OpenAI’s language model. Users can receive tailored movie suggestions based on genre, release year, ratings, and runtime using The Movie Database (TMDb) API. The bot is hosted on a Gradio interface for a seamless interactive experience.

## Question To Be Answered
At the start of the project we defined the following question as one we wanted to answer for this project:

Given movie review datasets that includes names, length, rating, etc., can we create a chatbot that processes user requests for movie recommendations based on user requirements such as certain years (can be a range), length (can be a range), rating (can be a range), genre, etc.?

"Suggest an action movie made between 2018-2019 that has a rating of 8.0 or greater."


### Features

* Simple, direct interface to ChatGPT via OpenAI API.
  
* Conversational Interaction: Users can chat naturally, specifying preferences like genre, release years, and rating levels.

* Detailed Movie Information: Provides additional movie details, including release date, rating, and runtime.

* Dynamic Querying: Determines user needs from text input to fetch relevant movie recommendations from TMDb.

### Requirements

* Python 3.8+
* Dependencies:
* langchain
* openai
* requests
* gradio

Install dependencies with:

    pip install langchain openai requests gradio

## Setup

    API Keys:

        Obtain your OpenAI API Key from OpenAI.
        Obtain your TMDb API Key from The Movie Database.

Configure API Keys: Replace the placeholder keys in the code with your own OpenAI and TMDb keys:

    openai_api_key = "your_openai_api_key"
    tmdb_api_key = "your_tmdb_api_key"

## Files
The core solution for this project can be found in the `chatbot_solution.ipynb` file. The other files were used by individual team members during the project and then code from them were combined in the final solution file. This is a Jupyter Notebook and requires an environment set up for running Jupyter Notebooks in order to test and run the solution.

## Usage

### Running the Bot

1)   Start the Gradio interface:

            chatgpt_interface.launch()

2) Example Queries:

* "Suggest some recent action movies."

* "Can you find highly rated dramas from 2020 to 2023?"

* "Recommend top-rated sci-fi movies under 120 minutes."

3) Explanation of Main Functions:

* query_tmdb: Interacts with the TMDb API to retrieve movie recommendations based on user preferences.

* chatgpt_direct_movie_recommender: Processes user input, detects relevant keywords (e.g., genre, year, rating), and queries TMDb if necessary.

## Technical Overview

* LangChain and Prompting:

    * A custom PromptTemplate is used to guide the conversation.

    * ConversationBufferMemory stores chat history, allowing for continuity in responses.
    
* API Querying:

    * query_tmdb fetches movie data from TMDb, filtering by genre, year, and rating based on user input.
    
    * The bot limits responses to the top 10 results for optimal performance.





## Question To Be Answered
Given movie review datasets that includes names, length, rating, etc., can we create a chatbot that processes user requests for movie recommendations based on user requirements such as certain years (can be a range), length (can be a range), rating (can be a range), genre, etc.?

"Suggest an action movie made between 2018-2019 that has a rating of 8.0 or greater."

