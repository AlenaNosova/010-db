### **Запрос для вставки данных минимум о двух книгах в коллекцию books**
```javascript
db.books.insertMany([
  {
    title: "Book I: The Ring Sets Out",
    description: "Description for Book I",
    authors: "J. R. R. Tolkien"
  },
  {
    title: "Book II: The Ring Goes South",
    description: "Description for Book I",
    authors: "J. R. R. Tolkien"
  }
]);
```
### **Запрос для поиска полей документов коллекции books по полю title**
```javascript
db.books.find({ title: "Book I: The Ring Sets Out" });
```
### **Запрос для редактирования полей: description и authors коллекции books по _id записи**
```javascript
db.books.updateOne(
  { _id: 1 },
  { $set: { description: "New description for Book I", authors: "John Ronald Reuel Tolkien" } }
);
```
