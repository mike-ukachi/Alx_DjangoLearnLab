---

### 📄 `update.md`

```md
# 🟡 UPDATE Operation

## 🎯 Project Instruction
> "Update the title of the Book instance with the title '1984' to 'Nineteen Eighty-Four'."

## 💻 Command Used in Django Shell

```python
from bookshelf.models import Book
book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()
```
