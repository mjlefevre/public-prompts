# Prompt: summarize-logs.py

Use this prompt with any LLM (Claude, ChatGPT, Gemini, etc.) to generate a working PEP 723 script.

---

## The Prompt

```
Write me a Python script that analyzes log files and produces a summary report.

Requirements:
- Accept one or more log file paths as command-line arguments
- Also accept input from stdin (for piping: `cat *.log | python summarize-logs.py`)
- Detect common log formats automatically (Apache, nginx, syslog, JSON lines, generic timestamped)
- Produce a summary including:
  - Total line count
  - Date range covered
  - Breakdown by log level (ERROR, WARN, INFO, DEBUG) if detectable
  - Top 10 most frequent error messages (with counts)
  - Requests per hour histogram (if applicable)
  - Any anomalies (sudden spikes in errors, gaps in timestamps)
- Output as formatted text by default, with a `--json` flag for machine-readable output
- Handle large files efficiently (streaming, don't load entire file into memory)

Make this a PEP 723 script with inline dependencies. Use `rich` for formatted output and `python-dateutil` for flexible date parsing.
```

---

## Expected Output

The LLM should produce a complete `.py` file starting with:

```python
# /// script
# requires-python = ">=3.11"
# dependencies = [
#     "rich",
#     "python-dateutil",
# ]
# ///
```

## Usage

Save the output to `summarize-logs.py` and run:

```bash
uv run summarize-logs.py /var/log/nginx/access.log
uv run summarize-logs.py app.log error.log --json
cat /var/log/syslog | uv run summarize-logs.py
```
