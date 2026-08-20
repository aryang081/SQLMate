# SQLMate 🤖

SQLMate is an AI-powered SQL database assistant that allows users to interact
with a SQLite company database using natural-language questions.

Instead of writing SQL queries manually, users can ask questions such as:

- Who has the highest salary?
- What departments are in the company?
- Show me the employee details.
- What is the budget of the Engineering department?

The application uses an LLM to understand the question, select the appropriate
database tool, query the SQLite database, and return a natural-language answer.

## Tech Stack

- Python
- LangChain
- LangGraph
- OpenRouter
- SQLite
- Gradio
- Jupyter Notebook

## Architecture

User Question
      ↓
Gradio Chat Interface
      ↓
LangGraph Agent
      ↓
LLM via OpenRouter
      ↓
Database Tools
      ↓
SQLite Database
      ↓
Natural-Language Response

## Features

- Natural-language SQL database interaction
- Automatic tool selection
- Database schema inspection
- SQL query execution
- Multiple database tools
- Conversational context
- Gradio-based chat interface

## Database

The project currently uses a SQLite database:

`company_final_app.db`

The database contains:

- `departments`
- `employees`

## Setup

### 1. Clone the repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd SQLMate

2. Create a virtual environment
python3 -m venv .venv
source .venv/bin/activate
3. Install dependencies
python -m pip install -r requirements.txt
4. Configure the API key
Create a .env file in the project root:
OPENROUTER_API_KEY=your_api_key_here
Do not commit the .env file to GitHub.
5. Run the project
Open basic.ipynb in VS Code or Jupyter Notebook and run the cells
from top to bottom.
The final cell launches the Gradio interface.
Example
User:
Who has the highest salary?
SQLMate:
Alice has the highest salary, with a salary of 95,000.
Project Structure
SQLMate/
├── basic.ipynb
├── company_final_app.db
├── requirements.txt
├── README.md
└── .gitignore
Security
API keys are stored in environment variables and are not committed to the
repository.
Make sure .env is included in .gitignore.
Future Improvements
Convert the notebook into a standalone Python application
Add support for more databases
Improve SQL query validation
Add authentication
Deploy the application