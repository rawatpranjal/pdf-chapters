# PDF Chapter Splitter

This script splits a single PDF file into multiple chapters based on page ranges defined in a `chapters.txt` file.

## File Structure

```
project_folder/
├── input/                  # Folder containing the input PDF
│   └── example.pdf         # The PDF to split
├── output/                 # Folder where chapter PDFs will be saved
├── chapters.txt            # Text file with chapter names and page ranges
└── main.py                 # The Python script
```

## How to Use

1. Install the required library:
   ```bash
   pip install PyPDF2
   ```
2. Place the PDF to split in the `input/` folder.
3. Create a `chapters.txt` file in this format:
   ```
   chapter_name start_page end_page
   ```
   Example:
   ```
   introduction_and_motivation 21 43
   running_and_analyzing_experiments 44 56
   ```
4. Run the script:
   ```bash
   python3 main.py
   ```
5. The chapter PDFs will be saved in the `output/` folder as:
   ```
   01_chapter_name.pdf
   02_chapter_name.pdf
   ```
```