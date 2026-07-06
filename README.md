# SOAR-X

SOAR-X is an authorized-scope security operations platform for academic and lab environments. It brings together vulnerability assessment, scan orchestration, detection logic, forensic export, and reporting in a single Flask-based application.

## Overview

This project is designed for safe, controlled security testing in environments you own or are explicitly authorized to assess. It includes a web dashboard, REST-style APIs, and a demo application for lab-oriented simulation.

## Features

- Multi-target and CIDR-aware scanning workflows with nmap integration
- Scope control and authorization-aware reporting
- Vulnerability heuristics with OWASP-oriented metadata
- SIEM-style detection for suspicious activity patterns
- Forensic export in JSON and CSV formats
- Incident and evidence management workflows
- Interactive dashboard with charting and reporting views

## Screenshots

Placeholder for screenshots:

- Dashboard overview
- Scan results and findings
- Incident and forensic report views

## Installation

### Prerequisites

- Python 3.10+
- Optional: nmap installed on the host for full scanning support

### Local setup

```powershell
cd path\to\SOAR-X
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python app.py
```

Open http://127.0.0.1:5000/login to begin.

## Requirements

The project dependencies are listed in requirements.txt and include:

- Flask
- python-nmap
- requests
- reportlab
- python-dotenv

## How to Run

### Local development

```powershell
python app.py
```

### Docker Compose

```bash
docker compose build
docker compose up
```

Optional demo profile:

```bash
docker compose --profile mock up
```

### Seed sample data

```powershell
python scripts\seed_sample_data.py
```

## Project Structure

```text
app.py                  # Entry point for the Flask app
requirements.txt       # Python dependencies
Dockerfile              # Container image definition
docker-compose.yml      # Local lab deployment
soarx/                  # Application package
  config.py             # Settings and environment defaults
  db.py                 # Database initialization and helpers
  routes/               # Web, API, and demo blueprints
  services/             # Scan, risk, and incident-related logic
  scanners/             # Scanner orchestration components
  detection/            # Detection rules and analysis
  forensics/            # Timeline and evidence utilities
  reporting/            # Report generation
  templates/            # HTML templates
  static/               # CSS and JavaScript assets
  utils/                # Scope and network helpers
scripts/                # Seed and utility scripts
data/                   # Runtime and sample data
```

## Technologies Used

- Python
- Flask
- SQLite
- Jinja2 templates
- Chart.js
- ReportLab
- python-nmap

## Future Improvements

- Add automated tests and CI pipelines
- Improve container hardening and deployment settings
- Add authentication and session policy refinements
- Expand analytics and alert correlation features

## License

This project is licensed under the MIT License. See the LICENSE file for details.
