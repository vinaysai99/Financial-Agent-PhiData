# Agentic AI Application with PhiData

This project demonstrates how to build end-to-end agentic AI applications using the PhiData framework. It showcases the creation of independent agents and their combination to execute complex workflows.

## Key Features

- **Open Source Platform**: PhiData is used as an open-source framework to build, ship, and monitor agentic systems.
- **AI Agents**: The project includes the creation of AI agents, including multimodal agents, and agentic workflows.
- **LLM Flexibility**: The project can use any LLM and turn it into an agent. It integrates with open source models like Groq, Hugging Face, and others.
- **Knowledge Integration**: It allows for the addition of domain-specific knowledge.
- **Tool Integration**: PhiData allows integration with various tools, such as DuckDuckGo Search, and yFinance.
- **Cloud and Local Deployment**: The framework is capable of being deployed locally as well as on cloud platforms.

## Project Structure

The project consists of the following main components:

- **`financial_agent.py`**: This file contains the core logic for creating a financial analysis application. It includes:
  - **Web Search Agent**: An agent that searches the web for information using the DuckDuckGo search tool .
  - **Financial Agent**: An agent that retrieves financial data using the yFinance tool.
  - **Multi-Agent Workflow**: Combines the web search and financial agents to provide a comprehensive analysis.
- **`playground.py`**: This file sets up a playground environment using PhiData, allowing for interaction with the agents via a web interface.
- **`requirements.txt`**: This file lists all the necessary Python libraries to run the project.
- **`.env`**: This file holds the API keys for PhiData and Groq .

## Setup and Installation

1. **Create a virtual environment:**
   ```bash
   conda create -p venv python=3.12
   ```
2. **Activate the virtual environment:**
   ```bash
   conda activate venv
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
  
4. **Create a .env file:**

- Add your Phi Data API key : PHIDATA_API_KEY=your_Phidata_api_key
- Add your Groq API key : GROQ_API_KEY=your_groq_api_key

5. **Set the Groq API Key in the terminal:**
   ```bash
   setx GROQ_API_KEY "your_groq_api_key"
   ```
   
## Usage
### Running financial_agent.py
- To run the financial agent directly from the command line, use:
  ```bash
  python financial_agent.py
  ```
- This will output the analysis and recommendations in the terminal.
### Running playground.py
1. To start the playground, run:
  ```bash
  python playground.py
  ```
- This will start a server on http://127.0.0.1:7777 .
2. Open your PhiData dashboard.
3. Navigate to the playground section.
4. Select the Local Host endpoint (usually http://127.0.0.1:7777).
5. Interact with the agents via the web interface.
  
## Dependencies

The required libraries are listed in requirements.txt and include:
- phidata 
- python-dotenv
- yfinance
- packaging
- duckduckgo-search
- fastapi
- uvicorn
- groq
- openai

## Example Queries
- Financial Agent: "Summarize analyst recommendations and share the latest news for NVDA".
- Playground: "What is your special skill?", "I am interested in Tesla", "Summarize analyst recommendations and share the latest news for Tesla", "Compare Tesla and Nvidia and provide analyst recommendation".
  
## Notes
- The project uses Groq's API for language model processing.
- The financial_agent.py script uses both web search and financial data to provide comprehensive responses.
- The playground app provides a user-friendly way to interact with the agents.
- This README provides a comprehensive overview of the project, its structure, and how to set it up and use it based on the provided source material.

