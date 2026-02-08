# Prompt: convert-csv-to-json.py

Use this prompt with any LLM (Claude, ChatGPT, Gemini, etc.) to generate a working PEP 723 script.

---

## The Prompt

```
Write me a Python script that converts CSV files to JSON with flexible options.

Requirements:
- Accept a CSV file path as input, or read from stdin
- Output JSON to stdout by default, or to a file with `-o` / `--output`
- Support multiple output formats:
  - `--format records` (default): Array of objects, each row becomes an object with column headers as keys
  - `--format columns`: Object with column names as keys, arrays of values
  - `--format nested`: Allow specifying a grouping key with `--group-by` to create nested structure
- Handle data type inference:
  - Detect integers, floats, booleans, dates, and nulls automatically
  - Allow disabling with `--no-infer` to keep everything as strings
- Support common CSV variations:
  - Auto-detect delimiter (comma, tab, semicolon, pipe)
  - Allow explicit delimiter with `-d` / `--delimiter`
  - Handle quoted fields and escaped characters properly
  - Skip comment lines (starting with #) with `--skip-comments`
- Pretty-print JSON by default, use `--compact` for minified output
- Show a preview of the first 5 rows with `--preview` (doesn't write output)

Make this a PEP 723 script with inline dependencies. Use only the standard library - no external dependencies needed for this one, but include `rich` for the preview feature formatting.
```

---

## Expected Output

The LLM should produce a complete `.py` file starting with:

```python
# /// script
# requires-python = ">=3.11"
# dependencies = [
#     "rich",
# ]
# ///
```

## Usage

Save the output to `convert-csv-to-json.py` and run:

```bash
uv run convert-csv-to-json.py data.csv > data.json
uv run convert-csv-to-json.py data.csv -o data.json --compact
uv run convert-csv-to-json.py sales.csv --format nested --group-by region
cat export.csv | uv run convert-csv-to-json.py --format columns
uv run convert-csv-to-json.py data.tsv -d '\t' --preview
```
