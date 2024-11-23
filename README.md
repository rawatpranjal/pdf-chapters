# PDF Split and Summarize

This script splits a single PDF file into multiple chapters based on page ranges defined in a `chapters.txt` file and generates LaTeX summaries for each chapter using OpenAI's GPT.

## File Structure

```
project_folder/
├── input/                  # Folder containing the input PDF
│   └── example.pdf         # The PDF to split
├── output/                 # Folder where chapter PDFs will be saved
├── chapters.txt            # Text file with chapter names and page ranges
├── key.txt                 # File containing the OpenAI API key
├── main.py                 # The Python script for splitting
└── summarize.py            # The Python script for summarizing chapters
```

## How to Use

### Step 1: Install Dependencies
   ```bash
   pip install PyPDF2 openai tqdm
   ```

### Step 2: Split PDF into Chapters
1. Place the PDF to split in the `input/` folder.
2. Create a `chapters.txt` file in this format:
   ```
   chapter_name start_page end_page
   ```
3. Run the script to split the PDF:
   ```bash
   python3 main.py
   ```

   The chapter PDFs will be saved in the `output/` folder as:
   ```
   01_chapter_name.pdf
   02_chapter_name.pdf
   ```

### Step 3: Summarize Chapters and Save to LaTeX
1. Place your OpenAI API key in `key.txt`.
2. Run the summarization script:
   ```bash
   python3 summarize.py
   ```
3. A LaTeX file (`summary.tex`) will be created in the project folder. It will include summaries of all chapters.