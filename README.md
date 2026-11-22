# GitHub Quota Monitor

Windows desktop application for monitoring GitHub Actions Storage, Actions Cache, repository availability, API rate limits, billing information and usage history.

## Features
- GitHub repository monitoring
- Actions Storage and Actions Cache overview
- GitHub API rate-limit monitoring
- Actions artifacts listing
- Billing usage summary when available from the API
- Analytics, CSV/XLSX exports and scheduled reports
- Windows notifications and system tray support
- Russian and English interface
- Lightweight polling and chart rendering

## Requirements
- Windows 10/11
- Python 3.12 recommended
- A GitHub Personal Access Token with the read permissions required for the repositories and Actions data you monitor

## Quick start
1. Download or clone this repository.
2. Run `run.bat`.
3. Enter your GitHub token in **Settings**.
4. Add repositories using `owner/repository`, one per line.
5. Save settings and run a check.

## Run from source
```powershell
py -3.12 -m venv .venv
.venv\\Scripts\\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
python main.py
```

## Build a Windows executable
```powershell
pip install -r build-requirements.txt
build_exe.bat
```
The build script creates a PyInstaller distribution in the `dist` directory.

## Local data and security
Configuration, monitoring history, analytics and logs are stored locally under `%LOCALAPPDATA%\\GitHubQuotaMonitor`. The GitHub token is kept in the local application configuration. Do not commit tokens, `.env` files, personal configuration, logs or local databases.

Use a token with read-only access wherever possible. The application does not need repository write permissions for monitoring.

## Language
Choose **Русский** or **English** in Settings. The selected language is saved locally.

## Documentation
See the README and the instructions in the application settings. Detailed guides will be expanded in the `docs/` directory in subsequent documentation updates.

## Current version
**v5.64**

See the application changelog in the releases section when a packaged release is published.

## Disclaimer
This is an independent utility and is not affiliated with or endorsed by GitHub. GitHub API fields, billing availability and plan information may vary by account and API permissions. Usage estimates shown by the application are not an official invoice.
