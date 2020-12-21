### Conceptual Exercise

Answer the following questions below:

- What is PostgreSQL?
  
  A: PostgreSQL is one example of a **database management system (DMS)**, which does exactly what the name suggests: helps to manage a database.

- What is the difference between SQL and PostgreSQL?

  A: SQL, which stands for *structured query language*, is a programming language commonly used to query databases and database management systems. PostgreSQL is just one example of a database management system that uses SQL as its base language for database management. 

- In `psql`, how do you connect to a database?

  A: (I'm reading this as 'once you are in the psql console') To connect to a database, use the '\c' command followed by the name of an existing database on your system. 

- What is the difference between `HAVING` and `WHERE`?

    A: `HAVING` clauses are used to filter charactaristics of aggregate datasets, whereas  `WHERE` clauses are used to filter characteristics of row data, instead of aggregate data. 

- What is the difference between an `INNER` and `OUTER` join?

  A: `INNER` joins are, the way i think of them, more strict when it comes to the condition. For the data to be included, it HAS to satisfy the condition in BOTH datasets.
  
  For `Outer` joins, depending on the type (left, right, full), this restriction is much looser. All data from one of the tables is included (left/right), and then the data from the other table that fits the condition is also included.  

- What is the difference between a `LEFT OUTER` and `RIGHT OUTER` join?

  A: The difference can be found right in the names. When writing `JOIN` statements, there is the tablename that comes first, to the left of the word 'join', and the table that comes after, or to the right of the word 'join'. `LEFT OUTER` AND `RIGHT OUTER` joins specify specifically which table displays ALL their data, and which displays only that data which satisfies the join condition. Which ever one is named in the join, that's the table that gives all of its data regardless of the join condition. 

- What is an ORM? What do they do?

  A: An **ORM** is an 'object relational mapper', and its job is to take relations/data and 'map' them into code-accessible objects/classes that can be manipulated using a coding language. 

- What are some differences between making HTTP requests using AJAX 
  and from the server side using a library like `requests`?

  A: AJAX requests have the ability to be faster since the browser itself can directly talk to the endpoint without going through the backend. However, too many browser requests can slow things down and using server side HTTP requests (same-origin policy) can help prevent this. Server side also makes it easier to store/access database data, and can be more secure when using passwords since the password isn't just sitting in the JS file. 

- What is CSRF? What is the purpose of the CSRF token?

  A: 'CSRF' stands for "Cross-Site Request Forgery', which basically means that any form from any site can submit to any other url. This can have nasty side effects if the form is meant to delete users, or access private data of some sort. 
  
  To prevent this, forms can include a CSRF token which is included (but hidden) in the form HTML, and is verified/validated when the form is submitted. Server-side logic can be implented so that if this token is not validated, the form never actually submits its data. 

- What is the purpose of `form.hidden_tag()`?

  A: It adds the form fields who have the type `hidden`, like the csrf token in WTforms. This way it's included on the form submit. 