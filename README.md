# Parse CNAI project list to a structured dataset

The CNAI provides a list of AI and Machine Learning related projects in the Swiss administration. The list is provided as a PDF. With this repo we try to parse the data and create a structured dataset. 

Steps:
- Download PDF
- Open PDF with Acrobat and save to DOCX
- Convert DOCX to Markdown with pandoc:
    - `pandoc -f docx -t markdown -o _input/CNAI_Projekte_D_8_0.md _input/CNAI_Projekte_D_8_0.docx` 
- Process Markdown document with notebook:
    - Read data
    - Split into projects
    - Send to LLM to extract key information
    - Export to Excel file

## Usage
- Clone repo
- Change into repo, create Conda environment: `conda create -n cnai python=3.9`
- Activate environment: `conda activate cnai`
- Install libraries: `pip install -r requirements.txt`
- Open and run notebook.

To preprocess DOCX files you also need to install [pandoc](https://pandoc.org/installing.html). 