# Mongodbfundamentals
# MongoDB Fundamentals Assignment

**Instructions**

- Complete all exercises using MongoDB shell or Compass
- Submit your queries and explanations
- Take screenshots of your results where requested

**Part 1: Basic CRUD Operations**

***Exercise 1.1: Database and Collection Creation***

-Create a database called bookstore and a collection called books. Insert the following 5 books:

```javascript
// Insert these books:
1. Title: "The Hobbit", Author: "J.R.R. Tolkien", Price: 15.99, Genre: "Fantasy", Pages: 310, InStock: true
2. Title: "1984", Author: "George Orwell", Price: 12.50, Genre: "Dystopian", Pages: 328, InStock: true
3. Title: "Pride and Prejudice", Author: "Jane Austen", Price: 9.99, Genre: "Romance", Pages: 432, InStock: false
4. Title: "The Catcher in the Rye", Author: "J.D. Salinger", Price: 14.25, Genre: "Fiction", Pages: 277, InStock: true
5. Title: "Dune", Author: "Frank Herbert", Price: 18.99, Genre: "Sci-Fi", Pages: 896, InStock: true
```

**Deliverable:** Provide the insert commands used and a screenshot showing all 5 documents.

**Exercise 1.2: Read Operations**

***Write queries to find:***

1. All fantasy books
2. Books that cost less than $15
3. Books that are in stock and have more than 300 pages
4. All books sorted by price in descending order

**Deliverable:*** Provide each query and the results.

***Exercise 1.3: Update Operations***

**Perform the following updates:**

1. Increase the price of all fantasy books by $2
2. Add a new field Rating: 4.5 to "The Hobbit"
3. Update "Dune" to be out of stock (InStock: false)

**Deliverable:** Provide the update commands and verify with find queries.

**Exercise 1.4: Delete Operations**

1. Delete all books that are out of stock
2. Delete the book "The Catcher in the Rye"

**Deliverable:** Provide the delete commands and show the remaining books.

**Part 2: Query Operators**

**Exercise 2.1: Comparison Operators**

- Using the same books collection (reinsert the original data), write queries using:

1. $gt - Find books with more than 400 pages
2. $in - Find books in "Fantasy" or "Sci-Fi" genres
3. $ne - Find books not written by "George Orwell"

**Deliverable:** Provide each query and explain what each operator does.

**Exercise 2.2: Logical Operators**

Write queries using:

1. $and - Find books by "J.R.R. Tolkien" that cost less than $20
2. $or - Find books that cost less than $10 OR have more than 500 pages
3. $nor - Find books that are not fantasy and not out of stock

**Deliverable:** Provide queries and results.

**Part 3: Array and Embedded Documents**

***Exercise 3.1: Working with Arrays***

- Create a new collection called customers with the following structure:

```javascript
{
  name: "John Doe",
  email: "john@email.com",
  orders: [
    { bookId: ObjectId("book_id_here"), quantity: 2, date: ISODate("2024-01-15") },
    { bookId: ObjectId("book_id_here"), quantity: 1, date: ISODate("2024-01-20") }
  ],
  addresses: [
    { type: "home", street: "123 Main St", city: "Boston", zip: "02101" },
    { type: "work", street: "456 Market St", city: "Boston", zip: "02110" }
  ]
}
```

- Add at least 3 customers with different order histories.

**Deliverable:**

1. Find customers who have ordered more than 1 quantity of any book
2. Find customers with a home address in Boston
