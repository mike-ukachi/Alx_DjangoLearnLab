🟢 CREATE Operation
🔧 Instruction
Create a Book instance with the title “1984”, author “George Orwell”, and publication year 1949.

💻 Django Shell Commands
python
from bookshelf.models import Book

book = Book(title="1984", author="George Orwell", publication_year=1949)
book.save()
✅ Expected Output
python
print(book)
# Output: <Book: 1984>
🔵 RETRIEVE Operation
🔧 Instruction
Retrieve and display all attributes of the book you just created.

💻 Django Shell Commands
python
retrieved = Book.objects.get(title="1984")

print(retrieved.title)
print(retrieved.author)
print(retrieved.publication_year)
✅ Expected Output
python
1984
George Orwell
1949
⚠️ Common Error
python
Book.DoesNotExist: Book matching query does not exist.
Solution: Confirm the book was saved and the title matches exactly. Use Book.objects.all() to inspect available records.

🟡 UPDATE Operation
🔧 Instruction
Update the title of “1984” to “Nineteen Eighty-Four” and save the changes.

💻 Django Shell Commands
python
retrieved.title = "Nineteen Eighty-Four"
retrieved.save()

print(retrieved.title)
✅ Expected Output
python
Nineteen Eighty-Four
🔴 DELETE Operation
🔧 Instruction
Delete the book you created and confirm the deletion by retrieving all books again.

💻 Django Shell Commands
python
retrieved.delete()

Book.objects.all()