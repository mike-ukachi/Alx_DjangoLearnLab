---

### 📄 `delete.md`

```md
# 🔴 DELETE Operation

## 🎯 Project Instruction
> "Delete the Book instance with the title 'Nineteen Eighty-Four'."

## 💻 Command Used in Django Shell

```python
from bookshelf.models import Book
book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()
```
