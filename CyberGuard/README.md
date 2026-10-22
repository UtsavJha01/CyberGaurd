# CyberGuard — Python Cybersecurity Toolkit

CyberGuard is a beginner-friendly, defensive cybersecurity dashboard built with Python and Streamlit.

## Features
- **Password Analyzer:** Local heuristic checks for length, character variety, common passwords, and repeated characters. Passwords are not saved.
- **File Integrity Monitor:** Uses SHA-256 hashes to create a local baseline and detect changes.
- **Security Log Analyzer:** Parses authentication logs and flags IP addresses with repeated failed-login events.
- **Authorized TCP Port Check:** Checks a user-selected list of up to 20 TCP ports on a device you own or are authorized to test.

## Tech stack
Python 3.10+, Streamlit, Pandas, SQLite-ready local project structure, SHA-256.

## Run locally

### Windows (PowerShell)
```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
streamlit run app.py
```

### macOS / Linux
```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
streamlit run app.py
```

Then open `http://localhost:8501` if it does not open automatically.

## Project structure
```text
CyberGuard_GitHub_Submission/
├── app.py
├── requirements.txt
├── README.md
├── PROJECT_REPORT.md
├── GITHUB_SETUP.md
├── LICENSE
├── .gitignore
├── utils/
│   ├── __init__.py
│   ├── passwords.py
│   ├── integrity.py
│   └── logs.py
├── sample_data/
│   └── auth.log
└── data/
    └── .gitkeep
```

## Safety and limitations
Use this project only on files, logs, and devices you own or have explicit permission to assess. The port checker is a basic TCP connection check, not a vulnerability scanner. Log matching and password scoring are educational heuristics and can produce false positives or miss events. This project does not block attacks, remove malware, or replace professional security tools.

## Suggested future improvements
- Unit tests with `pytest`
- CSV/PDF export for analysis reports
- Real-time file monitoring
- Configurable Windows Event Log support
- Authentication and access control before hosting publicly

## License
MIT. See `LICENSE`.
