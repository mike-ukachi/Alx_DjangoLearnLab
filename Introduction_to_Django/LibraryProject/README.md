# LibraryProject

LibraryProject is a simple Django web application for managing a bookshelf. It demonstrates basic CRUD (Create, Retrieve, Update, Delete) operations on a `Book` model.

## Features

- Add new books with title, author, and published year
- View all books in the library
- Update book details
- Delete books from the library
- Admin interface for managing books

## Project Structure

- `bookshelf/` - Django app containing the `Book` model, admin configuration, and migrations
- `LibraryProject/` - Django project settings, URLs, and configuration files
- `db.sqlite3` - SQLite database file

## Getting Started

1. **Install dependencies**  
   Make sure you have Python and Django installed.

2. **Apply migrations**

3. **Create a superuser (optional, for admin access)**

4. **Run the development server**

5. **Access the app**  
- Admin: [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

## Book Model

The `Book` model is defined in [`bookshelf.models.Book`](bookshelf/models.py):

- `title`: CharField, max length 200
- `author`: CharField, max length 100
- `published_year`: IntegerField

## Usage

You can use the Django shell to perform CRUD operations:

```python
from bookshelf.models import Book

# Create
book = Book(title="1984", author="George Orwell", published_year=1949)
book.save()

# Retrieve
retrieved = Book.objects.get(title="1984")
print(retrieved.title, retrieved.author, retrieved.published_year)

# Update
retrieved.title = "Nineteen Eighty-Four"
retrieved.save()

# Delete
retrieved.delete()
```