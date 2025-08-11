[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vgbm4cZ0)


Upload document → review_documents(files) is called with the uploaded file objects.

Read content → For each file, _read_docx_text() (or similar) extracts the text for AI preview.

AI folder selection → AI reads a short preview and picks the most relevant folders from your local directory tree.

Load reference docs → _load_docs_from_folders() reads all files inside those selected folders.

Chunk & embed → Those reference docs are chunked and embedded fresh every run (dynamic RAG).

Pass to LLM → Only the retrieved top chunks plus the uploaded doc are sent to the analysis chain.

AI analysis output → Parsed JSON of issues found.

Review doc creation → _add_comments_to_docx() creates a commented version of the uploaded doc.

ZIP packaging → All reviewed docs are zipped into reviewed_documents.zip for download.

So basically:
Upload → Preview → Folder pick → Load refs → Embed → Retrieve → Analyze → Annotate → Zip.

<img width="1333" height="628" alt="image" src="https://github.com/user-attachments/assets/7f54d1cc-fa8c-4e0f-bdec-6cdea7976740" />



