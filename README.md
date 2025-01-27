# Document-Search 
A web application that allows users to upload, search, view, and manage documents efficiently. Built with React for the frontend and FastAPI for the backend, the application uses MongoDB Atlas as the database and supports text-based search functionality.

Features 
                                                                                                                                                                                                                          . Upload documents in PDF or DOCX format.
. Extracts and stores text content from uploaded documents.
. Search functionality using MongoDB's full-text search.
. View document details such as filename, upload date, and content.
. Delete uploaded documents from the database.
. Error handling for unsupported file types or failed operations. 

Tech Stack
Frontend
. React: Interactive UI for document upload and search.
. Zustand: State management for managing search results, selected documents, and app state.
. Backend
. FastAPI: Handles document upload, search, and management.
. MongoDB Atlas: Stores documents and performs text-based search queries.
Other Tools
PyPDF2: Extracts text from PDF files.
python-docx: Extracts text from DOCX files.
Databutton Secrets: Securely manages environment variables like MongoDB credentials.
Getting Started
Prerequisites
Python 3.9+ installed.
Node.js and npm installed for the frontend.
MongoDB Atlas cluster set up and URI available.
Installation
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/yourusername/document-search-app.git
cd document-search-app
2. Backend Setup
Navigate to the backend directory:

bash
Copy
Edit
cd backend
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Add your MongoDB URI to the environment:

Create a .env file:
bash
Copy
Edit
touch .env
Add the MongoDB URI:
makefile
Copy
Edit
MONGODB_URI=your_mongodb_atlas_uri
Run the backend server:

bash
Copy
Edit
uvicorn main:app --reload
3. Frontend Setup
Navigate to the frontend directory:
bash
Copy
Edit
cd frontend
Install dependencies:
bash
Copy
Edit
npm install
Start the development server:
bash
Copy
Edit
npm start
API Endpoints
Upload Document
POST /upload
Uploads a PDF or DOCX file.
Request:
json
Copy
Edit
{
  "file": "document.pdf"
}
Response:
json
Copy
Edit
{
  "message": "Document uploaded successfully",
  "id": "123456",
  "filename": "document.pdf"
}
Search Documents
POST /search
Searches for documents based on a query string.
Request:
json
Copy
Edit
{
  "query": "search text"
}
Response:
json
Copy
Edit
{
  "results": [
    {
      "id": "123456",
      "filename": "document.pdf",
      "content": "Preview of the document content...",
      "upload_date": "2025-01-01T12:00:00Z"
    }
  ]
}
View All Documents
GET /documents
Retrieves all uploaded documents.
Delete Document
DELETE /documents/{document_id}
Deletes a document by its ID.
How to Use
Start both the backend and frontend servers.
Open the frontend in your browser (default: http://localhost:3000).
Upload a document.
Use the search bar to find documents by keywords.
Click on a search result to view document details.
Use the delete option to remove unwanted documents.
File Structure
Frontend
css
Copy
Edit
frontend/
├── src/
│   ├── components/
│   │   ├── SearchInterface.tsx
│   │   ├── SearchResults.tsx
│   ├── utils/
│   │   └── store.ts
│   └── App.tsx
└── package.json
Backend
bash
Copy
Edit
backend/
├── main.py
├── routers/
│   └── documents.py
├── requirements.txt
└── .env
Feel free to open issues or submit pull requests for improvements or bug fixes.

