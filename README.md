# Email Backup Script

This script allows you to back up emails from any IMAP server to your local machine. It provides an interactive command-line interface to select which folders to export, and saves each email as an `.eml` file in a structured directory.

## Features
- Connects to any IMAP server (server and port can be provided as an argument or interactively)
- Prompts for username and password securely
- Lists all available folders and lets you select which to export
- Creates a subfolder for each exported folder
- Saves each email as an individual `.eml` file
- Compatible with Python 3.7+

## Requirements
- Python 3.7 or higher
- `imapclient`

Install dependencies with:

```
pip install -r requirements.txt
```


## Download

You can download the pre-built Windows executable here:

**[Download email-backup.exe](dist/email-backup.exe)**

## Usage

### 1. Activate your virtual environment (if using one)

```
.venv\Scripts\Activate  # On Windows
source .venv/bin/activate  # On Linux/macOS
```

### 2. Run the script

You can provide the IMAP server (and optional port) as an argument:

```
python backup.py xmail.mwn.de:993
```

Or run without arguments and enter the server and port interactively:

```
python backup.py
```

You will be prompted for your username and password. Then, all folders will be listed and you can select which ones to export by entering their numbers (comma-separated).

### 3. Output

- Exported emails are saved in the `mail_export` directory.
- Each selected folder will have its own subdirectory.
- Each email is saved as `<uid>.eml`.

## Security Note
- Your password is not stored.
- Do not share your credentials or the exported `.eml` files unless you trust the recipient.

## License
MIT License
