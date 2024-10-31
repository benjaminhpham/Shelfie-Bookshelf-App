# Entity Relationship Diagram

Reference the Creating an Entity Relationship Diagram final project guide in the course portal for more information about how to complete this deliverable.

## Create the List of Tables

[👉🏾👉🏾👉🏾 List each table in your diagram]
Users, Favorite Books, Categories, Users_Books, Categories_Books

## Add the Entity Relationship Diagram

[👉🏾👉🏾👉🏾 Include an image or images of the diagram below. You may also wish to use the following markdown syntax to outline each table, as per your preference.]
![Untitled](https://github.com/user-attachments/assets/63166f05-b837-4d5b-b48d-160d890d51e9)

### 1. Users

Contains information on individual users of the library.

| Column Name | Type      | Description                  |
|-------------|-----------|------------------------------|
| id          | integer   | primary key, unique ID for each user |
| username    | text      | user's unique username |
| email       | text      | user's email address |
| password    | password  | user's password      |

### 2. Favorite_Books (Inventory)

Holds information on books available in the library inventory, including user favorites.

| Column Name    | Type      | Description                             |
|----------------|-----------|-----------------------------------------|
| id             | integer   | primary key, unique ID for each book    |
| title          | text      | title of the book                      |
| author         | text      | author of the book                     |
| publication_year | integer | year the book was published            |
| ...            | ...       | ...                                    |

### 3. Users_Books (Join Table)

A join table connecting users and their favorite books, establishing a many-to-many relationship.

| Column Name | Type      | Description                      |
|-------------|-----------|----------------------------------|
| user_id     | integer   | foreign key referencing Users    |
| book_id     | integer   | foreign key referencing Favorite_Books |

### 4. Categories

Lists different categories of books, such as Fiction, Non-Fiction, Sci-Fi, etc.

| Column Name | Type      | Description                |
|-------------|-----------|----------------------------|
| id          | integer   | primary key for each category |
| category_name | text    | name of the book category    |

### 5. Categories_Books (Join Table)

A join table associating books with various categories, enabling many-to-many relationships.

| Column Name | Type      | Description                              |
|-------------|-----------|------------------------------------------|
| book_id     | integer   | foreign key referencing Favorite_Books   |
| category_id | integer   | foreign key referencing Categories       |
