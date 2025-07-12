
---

### 📄 `retrieve.md`

```md
# 🔵 RETRIEVE Operation

## 🎯 Project Instruction
> "Retrieve and display all attributes of the book you just created."

## 💻 Command Used in Django Shell

```python
retrieved = Book.objects.get(title="1984")
print(retrieved.title)
print(retrieved.author)
print(retrieved.publication_year)
