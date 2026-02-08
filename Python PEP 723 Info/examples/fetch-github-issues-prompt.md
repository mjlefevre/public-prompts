# Prompt: fetch-github-issues.py

Use this prompt with any LLM (Claude, ChatGPT, Gemini, etc.) to generate a working PEP 723 script.

---

## The Prompt

```
Write me a Python script that fetches open GitHub issues from a repository and displays them in a formatted table.

Requirements:
- Accept repository owner and repo name as command-line arguments (e.g., `python fetch-github-issues.py microsoft vscode`)
- Optionally accept a GitHub token via the `GITHUB_TOKEN` environment variable for authenticated requests (higher rate limits)
- Display issues in a nicely formatted table showing: issue number, title (truncated to 50 chars), author, labels, and created date
- Sort by most recently updated
- Limit to the 20 most recent issues by default, but allow overriding with a `--limit` flag
- Handle errors gracefully (invalid repo, rate limiting, network issues)

Make this a PEP 723 script with inline dependencies. Use the `requests` library for HTTP and `rich` for table formatting.
```

---

## Expected Output

The LLM should produce a complete `.py` file starting with:

```python
# /// script
# requires-python = ">=3.11"
# dependencies = [
#     "requests",
#     "rich",
# ]
# ///
```

## Usage

Save the output to `fetch-github-issues.py` and run:

```bash
uv run fetch-github-issues.py microsoft vscode
uv run fetch-github-issues.py --limit 50 anthropics anthropic-sdk-python
```
