Bookshelf API

1. The API can store a list of books.
   Method : POST,
   URL : /books

   The server responds failed when:

- The client does not attach the property name to the request body (status code 400)
- The client attaches a read Page property value that is greater than the pageCount property value (status code 400)
- The server failed to load the book for a general reason (generic error), (status code 500)

2. The API can display entire books.
   Method : GET,
   URL: /books

   If no books have been entered, the server can respond with an array of empty books

3. The API can display book details.
   Method : GET,
   URL: /books/{bookId}

   If the book with the id attached by the client is not found, the server should return a 404 response

4. API can modify book data.
   Method : PUT,
   URL : /books/{bookId}

   The server responds failed when:

- The client does not attach a name property to the request body (status code 400)
- The client attaches a read Page property value that is greater than the pageCount property value (status code 400)
- The id attached by the client is not found by the server (status code 404)

5. The API can delete books.
   Method : DELETE,
   URL: /books/{bookId}
