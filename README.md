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
