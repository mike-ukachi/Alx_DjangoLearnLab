# 🟢 CREATE Operation

## 🎯 Project Instruction
> "Create a Book instance with the title '1984', author 'George Orwell', and publication year 1949."

## 💻 Command Used in Django Shell

```python
from bookshelf.models import Book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
```
