
# Document Search

A web application that allows users to upload, search, view, and manage documents efficiently. Built with React for the frontend and FastAPI for the backend, the application uses MongoDB Atlas as the database and supports text-based search functionality.




## Features

- Upload documents in PDF or DOCX format.
- Extracts and stores text content from uploaded documents.
- Search functionality using MongoDB's full-text Search
- View document details such as filename, upload date, and    content.
-  Delete uploaded documents from the database.
-  handling for unsupported file types or failed operations.



## Tech Stack

**Frontend:** React: Interactive UI for document upload and search.
Zustand: State management for managing search results, selected documents, and app state.

**Backend:** FastAPI: Handles document upload, search, and management.
MongoDB Atlas: Stores documents and performs text-based search queries.

**Others Tools:** PyPDF2: Extracts text from PDF files.
.python-docx: Extracts text from DOCX files.
Databutton Secrets: Securely manages environment variables like MongoDB credentials.


## Installation

 Clone the Repository

```bash
  https://github.com/sahilkumar7103/Document-Search


```  
 Backend Setup
    
```bash   
cd backend
```  
Install dependencies:
```bash   
pip install -r requirements.txt

```   
Add your MongoDB URI to the environment: 

```bash   
touch .env

``` 


```bash   
MONGODB_URI=mongodb+srv://sahilkumar:NxjZyLG3opt6anEi@cluster0.tsvgs.mongodb.net/test

``` 
Run the backend server:

```bash   
uvicorn main:app --reload

```   
Frontend Setup

```bash   
cd frontend

```  
Start the development server:
```bash   
npm start

```
## Deployment

To deploy this project run

```bash
  https://documentsearch.databutton.app/documentsearch
```


## How To Use

- Start both the backend and frontend servers.
-  Upload a document.
- Use the search bar to find documents by keywords.
- Click on a search result to view document details. 
- Use the delete option to remove unwanted documents.


## Contributing

Contributions are always welcome!

Feel free to submit issues or pull requests to improve the project.


