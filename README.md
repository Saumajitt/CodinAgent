# CodinAgent

A command-line AI coding assistant powered by Google Gemini LLMs. CodinAgent interprets natural language prompts to automate coding tasks, file system operations, and more, directly from your terminal.

## Features
- **AI-Powered Coding Agent:** Uses Google Gemini API to understand and execute user requests.
- **File System Automation:** List, read, and write files securely within the working directory.
- **Function Calling:** Dynamically plans and executes function calls based on user prompts.
- **Environment Variable Management:** Securely loads API keys and configuration from `.env` files.
- **Extensible & Modular:** Easily add new functions and capabilities.

## Tech Stack
- **Python 3.12+**
- **Google Gemini API** (`google.genai`)
- **python-dotenv** (for environment management)
- **Standard Python libraries:** `os`, `sys`

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Saumajitt/CodinAgent.git
cd CodinAgent
```


### 2. Set Up Environment (with uv)
- [Install uv](https://github.com/astral-sh/uv) if you don't have it:
  ```bash
  curl -Ls https://astral.sh/uv/install.sh | sh
  ```
- Install dependencies in a virtual environment (recommended):
  ```bash
  uv venv .venv
  source .venv/bin/activate
  uv pip install -r requirements.txt
  ```
- Or, install dependencies directly (if you don't use a venv):
  ```bash
  uv pip install -r requirements.txt
  ```
- Create a `.env` file in the project root and add your Gemini API key:
  ```env
  GEMINI_API_KEY=your_gemini_api_key_here
  ```


### 3. Usage
Run the agent from the project root using uv:
```bash
uv run main.py "List all files in the calculator directory"
```
- For verbose output:
  ```bash
  uv run main.py "Your prompt here" --verbose
  ```

## Example Prompts
- "List all files in the current directory."
- "Show the size of README.md."
- "Write 'Hello, World!' to hello.txt."

## Project Structure
```
CodinAgent/
├── main.py                # Entry point for the CLI agent
├── functions/             # Modular function implementations
│   ├── get_files_info.py
│   ├── write_file.py
│   └── ...
├── calculator/            # Example submodule
├── .env                   # Environment variables (not committed)
├── requirements.txt       # Python dependencies
├── README.md
└── ...
```

## Security
- All file operations are restricted to the working directory for safety.
- API keys are loaded from environment variables and never hardcoded.

## Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License.

## Author
[Saumajit](https://github.com/Saumajitt)
