# Chatbot

Enhanced Q&A Chatbot with Ollama
This project is a Q&A Chatbot built using Streamlit and the Langchain framework. It leverages open-source language models from Ollama, providing users with an intuitive interface to ask any question and receive responses based on the chosen model and configuration.

Features
Interactive User Interface: Built using Streamlit, allowing users to interact with the chatbot seamlessly.
Open-Source Model Integration: Uses Ollama's open-source language models, giving flexibility in model choice.
Adjustable Response Settings: Customize response temperature and token limits using sidebar sliders.
Prompt Customization: The chatbot’s prompt is defined using a template, making it easy to modify its behavior.
Environment Variable Support: Uses dotenv to manage API keys and other environment variables securely.
Installation
Prerequisites
Ensure you have Python installed (version 3.7 or higher). You'll also need to install the following Python packages:

bash
Copy code
pip install streamlit langchain-core langchain-community python-dotenv
Setting Up Environment Variables
Create a .env file in the root of the project directory to store your API keys securely. Add the following line to .env:

bash
Copy code
LANGCHAIN_API_KEY=your_actual_langchain_api_key_here
Run the Chatbot
To run the chatbot, use the following command:

bash
Copy code
streamlit run app.py
Usage
Open the Streamlit app using the link provided in the terminal after running app.py.
Choose the desired model from the sidebar (e.g., gemma2:2b).
Adjust the Temperature (controls randomness of the response) and Max Tokens (limits response length) using the sliders.
Enter your question in the input field, and the chatbot will generate a response.
Enjoy interactive and informative answers from your chatbot!
How It Works
The chatbot utilizes the following core components:

Prompt Template: A structured prompt that sets the system behavior (e.g., "You are a helpful assistant...") and formats the user input.
Ollama Language Models: The core engine generating responses based on the user’s query.
Langchain Framework: Handles the logic for constructing the chain of operations, parsing output, and customizing responses.
Environment Variables: Stores sensitive API keys securely using dotenv.
Project Structure
bash
Copy code
|-- .env                  # Contains environment variables (API keys)
|-- .streamlit/
    |-- secrets.toml      # For storing Streamlit secrets (optional)
|-- app.py                # Main Streamlit application code
|-- README.md             # Project documentation
|-- requirements.txt      # List of required Python packages
Customization
You can easily modify the chatbot's behavior by adjusting the Prompt Template inside app.py. For example, you can change the system's initial prompt to make the bot more formal, creative, or specialized in a particular field.

Future Improvements
Add support for more open-source language models from different providers.
Implement session management to maintain context over multiple queries.
Integrate with a knowledge base for specific domain-oriented Q&A.
Add a file upload option for document-based Q&A.
Troubleshooting
Missing Secrets Error
If you encounter a FileNotFoundError regarding missing secrets, make sure that the .env file is correctly set up with your API key, or place the secrets in the secrets.toml file inside the .streamlit directory.

Common Issues
Incorrect API Key: Make sure the LANGCHAIN_API_KEY is valid.
Environment Setup: Ensure all required packages are installed. Refer to requirements.txt for dependencies.
