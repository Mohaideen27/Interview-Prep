# 2. HTML Interview Questions – Concise Answers

## HTML Fundamentals

1\. What is HTML?

HTML stands for HyperText Markup Language. It is used to create the structure of web pages using elements and tags.

2\. What is HTML5?

HTML5 is the latest major version of HTML. It introduced semantic elements, audio, video, canvas, and improved form features.

3\. Difference between HTML and HTML5?

- HTML is the earlier version.
- HTML5 supports semantic tags like `header`, `footer`, and `article`.
- HTML5 supports audio and video without external plugins.
- HTML5 provides improved form input types.

4\. What are HTML tags and elements?

- Tag: A markup keyword inside angle brackets, like `<p>`.
- Element: The complete structure, including opening tag, content, and closing tag.

5\. Difference between block-level and inline elements?

- Block elements start on a new line and take available width. Example: `div`, `p`, `h1`.
- Inline elements take only the required width. Example: `span`, `a`, `strong`.

6\. What are semantic HTML elements?

Semantic elements clearly describe their meaning to browsers and developers.

Examples: `header`, `nav`, `main`, `section`, `article`, `footer`.

7\. Difference between div and span?

- `div` is a block-level container.
- `span` is an inline container.
- Both are used to group HTML elements.

8\. What is the purpose of DOCTYPE?

`<!DOCTYPE html>` tells the browser to render the document using HTML5 standards mode.

9\. What are attributes in HTML?

Attributes provide additional information about HTML elements.

Example:

```
<img src="photo.jpg" alt="Profile photo">
```

Here, `src` and `alt` are attributes.

10\. Difference between id and class?

- `id` uniquely identifies an element on a page.
- `class` can be applied to multiple elements.
- Both are used for CSS styling and JavaScript selection.

11\. What are forms in HTML?

Forms are used to collect user input and submit data to a server using the `<form>` element.

12\. What are different input types?

Common input types:

- `text`
- `password`
- `email`
- `number`
- `radio`
- `checkbox`
- `date`
- `file`
- `submit`
- `button`

13\. Difference between GET and POST methods?

- GET retrieves data and sends parameters in the URL.
- POST submits data in the request body.
- GET is generally used for reading data.
- POST is commonly used for creating or submitting data.

14\. What is the purpose of label tag?

The `<label>` tag provides a description for form inputs and improves accessibility.

15\. Difference between required, readonly, and disabled?

- `required`: User must enter a value before form submission.
- `readonly`: Value cannot be edited but is submitted with the form.
- `disabled`: Input cannot be interacted with and is not submitted.

16\. What is the purpose of local storage?

Local storage stores key-value data in the browser that remains available even after closing and reopening the browser.

17\. Difference between localStorage, sessionStorage, and cookies?

- `localStorage`: Data persists until manually cleared.
- `sessionStorage`: Data lasts for the browser tab's session.
- `cookies`: Small data stored in the browser and can be sent automatically with HTTP requests.

18\. What is the purpose of meta viewport tag?

It makes web pages responsive by controlling the viewport width and scaling on different devices.

Example:

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

19\. How do you embed images, audio, and video?

Using HTML tags:

```
<img src="image.jpg" alt="Image">

<audio controls src="audio.mp3"></audio>

<video controls src="video.mp4"></video>
```

20\. What is accessibility in HTML?

Accessibility means designing websites so everyone, including people with disabilities, can use them.

We use semantic tags, labels, alt text, keyboard navigation, and ARIA attributes.

# 3. CSS Interview Questions – Concise Answers

## CSS Fundamentals

1\. What is CSS?

CSS stands for Cascading Style Sheets. It is used to style HTML elements, including colors, fonts, spacing, and layouts.

2\. What are the different ways to apply CSS?

Three ways:

- Inline CSS: Using the `style` attribute.
- Internal CSS: Using the `<style>` tag.
- External CSS: Using a separate `.css` file.

3\. What is the CSS box model?

The CSS box model describes how every HTML element is structured.

It consists of:

1. Content
2. Padding
3. Border
4. Margin

4\. Explain margin, padding, and border.

- Margin: Space outside the border.
- Padding: Space between content and border.
- Border: Line surrounding the padding and content.

5\. Difference between margin and padding?

- Margin creates space outside an element.
- Padding creates space inside an element, between content and border.

6\. Difference between display: block, inline, and inline-block?

- `block`: Starts on a new line and takes available width.
- `inline`: Takes required width; width and height generally cannot be set.
- `inline-block`: Stays inline but allows width and height.

7\. What is Flexbox?

Flexbox is a one-dimensional CSS layout system used to arrange elements in a row or column.

8\. What is CSS Grid?

CSS Grid is a two-dimensional layout system used to arrange elements in rows and columns.

9\. Difference between Flexbox and Grid?

- Flexbox handles one-dimensional layouts (row or column).
- Grid handles two-dimensional layouts (rows and columns).

10\. Difference between relative, absolute, fixed, and sticky positioning?

- `relative`: Positions an element relative to its normal position.
- `absolute`: Positions an element relative to its nearest positioned ancestor.
- `fixed`: Positions an element relative to the viewport.
- `sticky`: Behaves relatively until a scroll threshold is reached, then sticks.

11\. What are pseudo-classes?

Pseudo-classes define special states of elements.

Examples: `:hover`, `:focus`, `:first-child`.

12\. What are pseudo-elements?

Pseudo-elements style specific parts of an element.

Examples: `::before`, `::after`, `::first-line`.

13\. What is CSS specificity?

Specificity determines which CSS rule is applied when multiple rules target the same element.

General priority:

Inline styles > ID > Class/attribute/pseudo-class > Element/pseudo-element.

14\. Difference between em, rem, %, and px?

- `px`: Fixed CSS pixel unit.
- `em`: Relative to the element's font size (for font-size, relative to the parent).
- `rem`: Relative to the root element's font size.
- `%`: Relative to the relevant parent or containing context.

15\. What are media queries?

Media queries apply CSS styles based on screen size or device characteristics.

Example:

```
@media (max-width: 768px) {
  .container {
    width: 100%;
  }
}
```

16\. How do you make a website responsive?

- Use media queries.
- Use Flexbox and Grid.
- Use relative units like `%`, `rem`, and `vw`.
- Add the viewport meta tag.
- Use responsive images.

17\. Difference between visibility: hidden and display: none?

- `visibility: hidden`: Hides the element but keeps its layout space.
- `display: none`: Hides the element and removes its layout space.

18\. Difference between z-index and position?

- `position` controls how an element is positioned.
- `z-index` controls its stacking order when stacking contexts allow it.
- `z-index` is commonly used with positioned elements and certain other stacking-context elements.

19\. What are CSS transitions and animations?

- Transition: Smoothly changes a property from one state to another.
- Animation: Creates multiple style changes using `@keyframes`.

Example:

```
button {
  transition: background 0.3s;
}

button:hover {
  background: blue;
}
```

## Tailwind CSS

20\. What is Tailwind CSS?

Tailwind CSS is a utility-first CSS framework that allows developers to style elements using predefined utility classes directly in HTML or JSX.

21\. What are the advantages of Tailwind CSS?

- Faster development.
- Responsive design support.
- Consistent styling.
- Less custom CSS.
- Easy customization.

22\. Difference between normal CSS and Tailwind CSS?

- Normal CSS uses custom selectors and stylesheets.
- Tailwind uses predefined utility classes.
- Tailwind makes styling directly in HTML or JSX easier.
- Normal CSS provides more traditional separation of styles.

23\. How do you handle responsive layouts using Tailwind CSS?

Tailwind provides responsive prefixes like:

- `sm:` – Small screens.
- `md:` – Medium screens.
- `lg:` – Large screens.
- `xl:` – Extra-large screens.

Example:

```
<div className="w-full md:w-1/2 lg:w-1/3">
  Responsive Content
</div>
```  



# SQL & SQLite Interview Questions – Concise Answers

Simple, interview-ready answers with SQL examples for practical questions.

## SQL Fundamentals

1\. What is SQL?

SQL stands for Structured Query Language. It is used to create, manage, retrieve, and manipulate data in relational databases.

2\. What is a database?

A database is an organized collection of data that can be stored, accessed, managed, and updated easily.

3\. What is SQLite?

SQLite is a lightweight, serverless relational database that stores data in a single file. It is commonly used in small applications and mobile apps.

4\. Difference between SQLite and MySQL?

- SQLite is serverless and file-based.
- MySQL uses a client-server architecture.
- SQLite is suitable for small applications.
- MySQL is suitable for larger applications with multiple concurrent users.

5\. What is a primary key?

A primary key uniquely identifies each record in a table. It cannot contain NULL or duplicate values.

6\. What is a foreign key?

A foreign key is a column that references the primary key of another table. It maintains relationships between tables.

7\. What is a unique key?

A unique key ensures that all values in a column or combination of columns are unique. NULL handling depends on the database.

8\. What is a composite key?

A composite key is a key made up of two or more columns used together to uniquely identify a record.

9\. What is normalization?

Normalization is the process of organizing database tables to reduce data duplication and improve data consistency.

10\. What are the different normal forms?

- 1NF: Each column contains atomic values.
- 2NF: Must be in 1NF and have no partial dependency on a candidate key.
- 3NF: Must be in 2NF and have no transitive dependency of non-key attributes on candidate keys.
- BCNF: Every determinant must be a candidate key.

11\. What is denormalization?

Denormalization intentionally introduces some data redundancy to improve read performance and reduce complex joins.

12\. What are SQL constraints?

SQL constraints are rules applied to table columns to maintain data accuracy and integrity.

Examples:

- PRIMARY KEY
- FOREIGN KEY
- UNIQUE
- NOT NULL
- CHECK
- DEFAULT

13\. Difference between DELETE, DROP, and TRUNCATE?

- `DELETE`: Removes selected rows from a table.
- `TRUNCATE`: Removes all rows while keeping the table structure (not supported by SQLite).
- `DROP`: Removes the entire table, including its structure.

14\. Difference between WHERE and HAVING?

- `WHERE` filters individual rows before grouping.
- `HAVING` filters grouped results after `GROUP BY`.

15\. What is GROUP BY?

`GROUP BY` groups rows that have the same values in specified columns, usually with aggregate functions.

16\. What is ORDER BY?

`ORDER BY` sorts query results in ascending (`ASC`) or descending (`DESC`) order.

17\. What are aggregate functions?

Aggregate functions perform calculations on multiple rows and return a single result.

Examples:

- `COUNT()`
- `SUM()`
- `AVG()`
- `MIN()`
- `MAX()`

## SQL Intermediate Concepts

18\. What is a JOIN?

A JOIN combines records from two or more tables based on a related column.

19\. Explain INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL JOIN.

- INNER JOIN: Returns matching records from both tables.
- LEFT JOIN: Returns all records from the left table and matching records from the right.
- RIGHT JOIN: Returns all records from the right table and matching records from the left.
- FULL JOIN: Returns all records from both tables, including unmatched records.

20\. What is a subquery?

A subquery is a query written inside another SQL query. It is used to retrieve data that the main query depends on.

21\. What is an index?

An index improves data retrieval speed by allowing the database to find records faster. However, it requires storage and can slow down write operations.

22\. What is a database transaction?

A transaction is a group of database operations treated as one logical unit. Either all operations succeed or the transaction is rolled back.

23\. What are ACID properties?

ACID ensures reliable database transactions.

- Atomicity: All operations succeed or none.
- Consistency: Database remains valid.
- Isolation: Concurrent transactions do not interfere improperly.
- Durability: Committed changes are permanent.

24\. Difference between SQL and NoSQL?

- SQL databases are relational and use structured tables.
- NoSQL databases support flexible data models such as documents and key-value pairs.
- SQL commonly uses predefined schemas.
- NoSQL often supports flexible schemas.

25\. What is Django ORM?

Django ORM stands for Object Relational Mapping. It allows developers to interact with databases using Python classes and methods instead of writing SQL queries manually.

## SQL Practical Interview Questions

For these examples, assume we have a table named `employees` with columns:

`id`, `name`, `salary`, `department`.

26\. How do you perform CRUD operations using SQL?

CRUD means Create, Read, Update, and Delete.

```
-- CREATE
INSERT INTO employees (name, salary, department)
VALUES ('John', 30000, 'IT');

-- READ
SELECT * FROM employees;

-- UPDATE
UPDATE employees
SET salary = 40000
WHERE id = 1;

-- DELETE
DELETE FROM employees
WHERE id = 1;
```

27\. How do you retrieve duplicate records?

Using `GROUP BY` and `HAVING`.

```
SELECT name, COUNT(*)
FROM employees
GROUP BY name
HAVING COUNT(*) > 1;
```

28\. How do you find the second-highest salary?

Using a subquery:

```
SELECT MAX(salary)
FROM employees
WHERE salary < (
    SELECT MAX(salary)
    FROM employees
);
```

This returns the second-highest distinct salary.

29\. How do you count records in a table?

Using `COUNT()`.

```
SELECT COUNT(*) FROM employees;
```

30\. How do you update multiple records?

Using `UPDATE` with a condition.

```
UPDATE employees
SET salary = salary + 5000
WHERE department = 'IT';
```

This increases the salary of all employees in the IT department by 5,000.

## Most Important SQL Queries to Practice

These are commonly asked in practical coding rounds.

1\. Find the highest salary

```
SELECT MAX(salary) FROM employees;
```

2\. Find the lowest salary

```
SELECT MIN(salary) FROM employees;
```

3\. Find employees earning more than 30,000

```
SELECT * FROM employees
WHERE salary > 30000;
```

4\. Count employees department-wise

```
SELECT department, COUNT(*)
FROM employees
GROUP BY department;
```

5\. Sort employees by highest salary

```
SELECT * FROM employees
ORDER BY salary DESC;
```

6\. Find the top 3 highest salaries

```
SELECT DISTINCT salary
FROM employees
ORDER BY salary DESC
LIMIT 3;
```

7\. Find employees whose names start with A

```
SELECT * FROM employees
WHERE name LIKE 'A%';
```

8\. Find employees with NULL department

```
SELECT * FROM employees
WHERE department IS NULL;
```

## Final Interview Preparation Priority

High priority

Focus on these topics first:

- Primary Key vs Foreign Key
- DELETE vs DROP vs TRUNCATE
- WHERE vs HAVING
- All types of JOINs
- GROUP BY and ORDER BY
- Normalization
- ACID properties
- Subqueries
- Second-highest salary
- Duplicate records
- SQL CRUD operations
- Django ORM

Interview tip: For SQL, don't just memorize definitions. Practice writing queries yourself. Interviewers commonly give tables and ask you to retrieve, filter, join, group, and update records.


# Python, Django & Django REST Framework – Interview Answers

These answers are short, simple, and suitable for speaking directly in a technical interview.

# 8. Django Interview Questions

### Django Fundamentals

1\. What is Django?

Django is a high-level Python web framework used to build secure, scalable, and maintainable web applications quickly.

2\. Why do we use Django?

- Built-in authentication.
- Database ORM.
- Admin panel.
- Security features.
- URL routing.
- Rapid development.

3\. What is MVT architecture?

MVT stands for Model-View-Template. It separates database logic, application logic, and presentation.

4\. Explain Model, View, and Template.

- Model: Handles database structure and data.
- View: Handles application logic and requests.
- Template: Handles the user interface.

5\. Difference between Django and Flask?

- Django is a full-featured framework with built-in tools.
- Flask is a lightweight framework that provides more flexibility and requires extensions for additional features.

6\. What is a Django project?

A Django project is the complete web application containing settings, URLs, and multiple apps.

7\. What is a Django app?

A Django app is a module responsible for a specific functionality, such as users, products, or payments.

8\. Difference between project and app?

- Project: Complete website or application.
- App: Individual functionality within the project.
- One project can contain multiple apps.

9\. What is settings.py?

`settings.py` contains project configurations such as database settings, installed apps, middleware, and security settings.

10\. What is urls.py?

`urls.py` maps URL patterns to their corresponding views.

11\. What is views.py?

`views.py` contains functions or classes that handle requests and return responses.

12\. What is models.py?

`models.py` defines database tables using Python classes.

13\. What is admin.py?

`admin.py` is used to register models and manage database records through Django's admin panel.

14\. What is manage.py?

`manage.py` is a command-line utility used to manage Django projects.

Example:

```
python manage.py runserver
```

15\. What is Django ORM?

ORM stands for Object Relational Mapping. It allows us to interact with databases using Python instead of writing SQL queries directly.

16\. What are migrations?

Migrations track and apply changes made to Django models in the database.

17\. Difference between makemigrations and migrate?

- `makemigrations`: Creates migration files based on model changes.
- `migrate`: Applies migrations to the database.

18\. What are Django model fields?

Model fields define the type of data stored in database columns.

Examples: `CharField`, `IntegerField`, `EmailField`, `DateField`, `BooleanField`.

19\. What is a QuerySet?

A QuerySet is a collection of database records returned by Django ORM. It supports filtering, sorting, and querying.

20\. Difference between get() and filter()?

- `get()`: Returns a single matching object; raises an exception if none or multiple are found.
- `filter()`: Returns a QuerySet containing matching objects.

21\. Difference between ForeignKey, OneToOneField, and ManyToManyField?

- ForeignKey: Many-to-one relationship.
- OneToOneField: One-to-one relationship.
- ManyToManyField: Many-to-many relationship.

22\. What is Django admin?

Django admin is a built-in interface used to manage application data without creating a separate management interface.

23\. What is middleware?

Middleware is a component that processes requests and responses globally before they reach the view or after the view returns a response.

24\. What is CSRF protection?

CSRF stands for Cross-Site Request Forgery. Django uses CSRF tokens to protect forms and requests from unauthorized cross-site submissions.

25\. What is authentication in Django?

Authentication verifies the identity of a user, usually through a username and password.

26\. What is authorization?

Authorization determines what an authenticated user is allowed to access or perform.

27\. What is session management?

Session management stores user-specific information across multiple requests, commonly using a session ID and server-side session data.

28\. Explain Django request-response lifecycle.

1. User sends a request.
2. Middleware processes the request.
3. URL dispatcher identifies the view.
4. View executes business logic.
5. Model interacts with the database if needed.
6. View returns a response.
7. Middleware processes the response.
8. Response is sent to the user.

29\. How do you connect Django with SQLite?

Configure the `DATABASES` setting in `settings.py`.

Django uses SQLite by default.

30\. How do you implement CRUD operations in Django?

CRUD stands for Create, Read, Update, and Delete.

```
# CreateStudent.objects.create(name="John")# ReadStudent.objects.all()# UpdateStudent.objects.filter(id=1).update(name="Sam")# DeleteStudent.objects.filter(id=1).delete()
```

# 9. Django REST Framework (DRF) Interview Questions

Very important – Prepare thoroughly

1\. What is Django REST Framework?

Django REST Framework is a powerful toolkit built on Django for creating REST APIs.

2\. Why do we use DRF?

- Easy API development.
- Serialization.
- Authentication and permissions.
- Built-in validation.
- Pagination.
- Browsable API.

3\. What is a REST API?

REST API is an architectural style that allows applications to communicate using HTTP methods and exchange data, commonly in JSON format.

4\. What are REST principles?

- Client-server architecture.
- Stateless communication.
- Uniform interface.
- Cacheable responses.
- Layered system.

5\. Difference between REST and SOAP?

- REST is an architectural style.
- SOAP is a messaging protocol.
- REST commonly uses JSON.
- SOAP commonly uses XML and has strict messaging standards.

6\. What is a serializer?

A serializer converts complex data, such as Django model objects, into JSON-compatible data and validates incoming data.

7\. Difference between Serializer and ModelSerializer?

- Serializer: Requires manually defining fields and validation.
- ModelSerializer: Automatically generates fields based on a Django model.

8\. What is serialization?

Serialization converts complex Python objects into JSON-compatible data for API responses.

9\. What is deserialization?

Deserialization converts incoming data into validated Python data that can be used to create or update objects.

10\. What is APIView?

APIView is a DRF class used to create API endpoints by defining methods such as `get()`, `post()`, `put()`, and `delete()`.

11\. What is GenericAPIView?

GenericAPIView provides common API functionality, such as queryset handling, serializer handling, and filtering support.

12\. What are ViewSets?

ViewSets combine multiple related API operations into a single class, such as listing, creating, updating, and deleting records.

13\. What are routers in DRF?

Routers automatically generate URL patterns for ViewSets.

14\. What are API endpoints?

API endpoints are specific URLs through which clients access API resources.

Example: `/api/users/`

15\. What are HTTP methods?

HTTP methods define the action performed on a resource. Common methods are GET, POST, PUT, PATCH, and DELETE.

16\. Explain GET, POST, PUT, PATCH, and DELETE.

- GET: Retrieve data.
- POST: Create new data.
- PUT: Replace existing data.
- PATCH: Partially update data.
- DELETE: Delete data.

17\. Difference between PUT and PATCH?

- PUT updates or replaces the complete resource.
- PATCH updates only specific fields.

18\. What are HTTP status codes?

HTTP status codes indicate the result of an API request.

19\. Explain 200, 201, 400, 401, 403, 404, and 500.

| Status | Meaning               |
| ------ | --------------------- |
| 200    | OK                    |
| 201    | Created               |
| 400    | Bad Request           |
| 401    | Unauthorized          |
| 403    | Forbidden             |
| 404    | Not Found             |
| 500    | Internal Server Error |

20\. What is token authentication?

Token authentication verifies users through a unique token sent with API requests, usually in the Authorization header.

21\. What is JWT authentication?

JWT stands for JSON Web Token. It is a token-based authentication method where a signed token is used to verify user identity.

22\. What is permission handling in DRF?

Permissions control which users can access specific API endpoints or perform specific actions.

Examples: `AllowAny`, `IsAuthenticated`, `IsAdminUser`.

23\. What is pagination?

Pagination divides large API responses into smaller pages to improve performance and usability.

24\. What is filtering?

Filtering allows users to retrieve specific records based on conditions.

Example: `/api/products/?category=mobile`

25\. What is API validation?

API validation checks incoming data to ensure it meets required rules before saving it to the database.

26\. What is CORS?

CORS stands for Cross-Origin Resource Sharing. It controls whether a frontend from another origin can access backend resources.

27\. How do you handle exceptions in DRF?

DRF provides API exceptions and exception handling mechanisms to return meaningful error responses.

Example:

```
from rest_framework.exceptions import ValidationErrorraise ValidationError("Invalid data")
```

28\. How do you test APIs?

We can test APIs using Postman, DRF's APIClient, or automated testing frameworks.

29\. What is Postman?

Postman is an API testing tool used to send HTTP requests and inspect API responses.

30\. How do you secure a REST API?

- Use authentication.
- Apply permissions.
- Use HTTPS.
- Validate input data.
- Configure CORS properly.
- Protect against CSRF where applicable.
- Use throttling and rate limiting.
- Never expose sensitive information.

## Important topics to revise before your interview

Python – High priority

- List vs Tuple
- Mutable vs Immutable
- `*args` and `**kwargs`
- OOP concepts
- Decorators and Generators
- Exception Handling

Django – High priority

- MVT Architecture
- Django ORM
- Models and Relationships
- Migrations
- Middleware
- CRUD Operations

DRF – Very high priority

- Serializer vs ModelSerializer
- APIView vs ViewSet
- GET, POST, PUT, PATCH, DELETE
- JWT Authentication
- Permissions
- Status Codes
- API Validation
- Pagination and Filtering
