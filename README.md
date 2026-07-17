# Resume Parser Project

This project parses resume files and compares them against a job description using the Groq API. It supports PDF and DOCX resume uploads and returns a structured analysis including candidate match score and reasoning.

## Features

- Reads resumes from PDF and DOCX files
- Extracts structured resume information using an LLM
- Compares the parsed resume against a job description
- Produces a match score and summary details
- Uses Pydantic models for structured JSON responses

## Project Structure

```text
week-1/day5/
├── resume_parser.py
├── main.py
├── pyproject.toml
├── README.md
└── resumes/
```

## Prerequisites

- Python 3.10+
- A Groq API key
- Internet access to call the Groq API

## Setup

1. Clone the repository
2. Navigate to the project folder
3. Create and activate a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
```

On Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

4. Install dependencies

If you are using uv:

```bash
uv sync
```

Or install manually:

```bash
pip install groq python-dotenv pydantic pypdf python-docx
```

5. Create a `.env` file in the project root

```env
GROQ_API_KEY=your_groq_api_key_here
```

6. Place your resume files in the `resumes/` folder

Supported formats:
- `.pdf`
- `.docx`

## Run the Project

```bash
python resume_parser.py
```

The script will:
- read all resumes from the `resumes/` folder
- parse each resume
- compare it with the sample job description
- print the top and bottom matching candidates

## Notes

- The script currently uses a sample job description embedded in the code.
- You may want to replace it with your own job description later.
- Make sure your API key is kept private and not committed to GitHub.

## Example Environment Variable

```env
GROQ_API_KEY=your_api_key_here
```

## License

This project is for educational and personal use.
