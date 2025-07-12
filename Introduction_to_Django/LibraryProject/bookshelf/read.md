# 🔵 READ Operation

## 🎯 Project Instruction
> "Retrieve the Book instance with the title '1984'."

## 💻 Command Used in Django Shell

```python
from bookshelf.models import Book
book = Book.objects.get(title="1984")
print(book.title, book.author, book.publication_year)
```