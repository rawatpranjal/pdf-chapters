```markdown
# PDF Chapter Splitter

This Python script splits a single PDF file into multiple chapter PDFs based on page ranges defined in a `chapters.txt` file. Each chapter is saved as a separate PDF in the `output` folder with sequential numbering.

## Project Structure

```
project_folder/
├── input/                  # Folder containing the input PDF file
│   └── example.pdf         # Place the PDF file to be split here
├── output/                 # Folder where the chapter PDFs will be saved (cleared before each run)
├── chapters.txt            # Text file defining the chapter names and page ranges
└── main.py                 # The Python script for splitting the PDF
```

## Requirements

- Python 3.x
- `PyPDF2` library

Install the required library with:
```bash
pip install PyPDF2
```

## Usage

1. Place the input PDF in the `input/` folder. Only one PDF should be present in this folder.
2. Create or update the `chapters.txt` file in the project folder. Each line should follow the format:
   ```
   chapter_name start_page end_page
   ```
   Example:
   ```
   introduction_and_motivation 21 43
   running_and_analyzing_experiments 44 56
   ```
3. Run the script:
   ```bash
   python3 main.py
   ```
4. The script will:
   - Clear the `output/` folder.
   - Split the input PDF into chapters based on `chapters.txt`.
   - Save the output PDFs in the `output/` folder as `01_chapter_name.pdf`, `02_chapter_name.pdf`, etc.

## Example

### Input
`chapters.txt`:
```
introduction_and_motivation 21 43
running_and_analyzing_experiments 44 56
```

### Output
```
output/
├── 01_introduction_and_motivation.pdf
├── 02_running_and_analyzing_experiments.pdf
```