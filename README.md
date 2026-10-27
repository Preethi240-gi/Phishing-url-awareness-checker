# EWB Phishing URL Awareness Checker

## Project overview
This beginner Python command-line project checks the visible text of a URL for six selected warning signs. It is intended for defensive cybersecurity learning.

**Important:** This program does not open URLs, visit websites, scan for malware, query reputation services, or prove that a URL is safe. "No listed warning signs found" does not mean "safe".

## Features
- Checks for an `@` symbol.
- Flags URLs longer than 100 characters.
- Flags hostnames that look like IPv4 addresses.
- Flags hostnames with five or more dot-separated segments.
- Checks for the `xn--` punycode marker.
- Flags the HTTP scheme.
- Repeats checks until the user types `q`, `quit`, or `exit`.
- Displays a `REVIEW CAREFULLY` summary when warning signs are found.
- Handles malformed URL parsing without crashing.

## Requirements
- Python 3.10 or later.
- No additional Python packages are required.

## How to run
1. Open a terminal in this project folder.
2. Check Python: `python --version` (Windows may also use `py --version`; Mac/Linux may use `python3 --version`).
3. Run the program:
   - Windows: `python phishing_checker.py`
   - Mac/Linux: `python3 phishing_checker.py`
4. Enter one of the sample URLs listed in `tests/test_samples.md`.
5. Type `q` to exit.

## Testing
Five workbook sample URLs and their expected observations are documented in [`tests/test_samples.md`](tests/test_samples.md). The actual output should be checked on your own computer before submission.

## Screenshots
The `screenshots` folder contains **sample reference captures** showing the program output. The workbook asks for evidence captured on your computer, so rerun the program locally and replace these reference images with your own screenshots before submitting.

## Improvements included
The starter code has been extended using improvement options described in the workbook:
1. **Loop with quit:** test multiple URL strings without restarting the program.
2. **Review carefully summary:** reports the number of warning signs found.
3. **Malformed input handling:** catches `ValueError` raised by URL parsing and displays a clear message.

## Limitations
- These are simple heuristics, not a phishing verdict.
- Legitimate URLs can trigger warnings, and malicious URLs can avoid these checks.
- The IPv4-style pattern checks the format only; it does not validate each octet's range.
- The program does not use machine learning, live threat intelligence, or internet requests.

## Ethical use
Use only the safe sample strings in the workbook or other benign test strings. Do not open suspicious links, collect credentials, send phishing messages, or probe websites as part of this project.

## Author
Student name: Tinglikar PreethiSudha
Course / group: CyberSecurity
