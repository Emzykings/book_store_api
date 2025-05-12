📚 Book Store Library API
A simple but fully functional **Library Management System API** built with **FastAPI**.
This project supports book tracking, borrowing and returning of books, fine calculation for overdue books, and reporting of most borrowed books.

### 🚀 Features
* Add new books to the library
* View all books, available books, and borrowed books
* Borrow books by title or author
* Return books and calculate overdue fines
* Delete books by title
* Get books by title or author
* Track books borrowed the most
* Identify books with prime number suffixes in title


### 🛠️ Tech Stack
* Python 3.8+
* FastAPI
* Pydantic
* Uvicorn (ASGI server)


### 📥 Installation
1️⃣ **Clone the repository**
```bash
git clone https://github.com/your-username/book_store_api.git
cd book_store_api
```

2️⃣ **Create and activate virtual environment**
```bash
python -m venv .venv
source .venv/Scripts/activate   # For Windows bash
```

3️⃣ **Install dependencies**
```bash
pip install fastapi uvicorn
```

4️⃣ **Run the server**
```bash
uvicorn main:app --reload
```

5️⃣ **Access the API docs**

```
http://127.0.0.1:8000/docs
```

(Interactive Swagger UI for testing your API)

### 📋 API Endpoints

| Method | Endpoint                 | Description                          |
| ------ | ------------------------ | ------------------------------------ |
| GET    | `/`                      | Welcome message                      |
| GET    | `/all-books`             | Get list of all books                |
| POST   | `/add-book`              | Add a new book                       |
| POST   | `/get-book-by-name`      | Get books by title                   |
| POST   | `/get-books-by-author`   | Get books by author                  |
| GET    | `/get-prime-suffix`      | Get books with prime number in title |
| POST   | `/delete-by-name`        | Delete book by title                 |
| POST   | `/borrow-book-by-author` | Borrow book by author                |
| POST   | `/borrow-book-by-title`  | Borrow book by title                 |
| POST   | `/return-book-by-author` | Return book by author                |
| POST   | `/return-book-by-title`  | Return book by title                 |
| GET    | `/get-borrowed-books`    | Get list of borrowed books           |
| GET    | `/get-available-books`   | Get list of available books          |
| GET    | `/most-borrowed-book`    | Get book(s) borrowed the most        |


### 💡 Fine Calculation Logic
* Users have **14 days free borrowing**.
* After 14 days, fine = **500 units per day overdue**.


### 📝 Notes
This project is designed for learning FastAPI concepts and is **in-memory only** (data resets when server restarts).
You can easily extend it with:
* Database integration (e.g., PostgreSQL, MongoDB)
* User authentication
* Background tasks
* Caching for performance


### 🏆 Acknowledgements
Inspired by real-world library systems to serve as a group learning project and portfolio starter in learning FASTAPI.
