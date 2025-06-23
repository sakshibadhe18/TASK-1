## Library Management System ##
Overview:
This project is a simple Library Management System built in MySQL.
It contains the basic operations to manage Members, Books, and Issued books.

Features:
Keep track of members and their contact information.

Store information about available books.

Record book issue and return dates.

 ## Tables ##
 ## Member ##
 | Column     | Type         | Description             |
| ---------- | ------------ | ----------------------- |
| member\_id | INT (PK)     | Unique ID of the member |
| name       | VARCHAR(100) | Name of the member      |
| phone      | VARCHAR(15)  | Contact number          |
| address    | VARCHAR(200) | Address                 |

## Books ##
| Column          | Type         | Description                 |
| --------------- | ------------ | --------------------------- |
| book\_id        | INT (PK)     | Unique ID of the book       |
| title           | VARCHAR(200) | Book title                  |
| author          | VARCHAR(100) | Author's name               |
| published\_year | INT          | Year the book was published |

## Issue ##
| Column       | Type     | Description                     |
| ------------ | -------- | ------------------------------- |
| issue\_id    | INT (PK) | Unique issue transaction ID     |
| member\_id   | INT (FK) | References `Member(member_id)`  |
| book\_id     | INT (FK) | References `Books(book_id)`     |
| issue\_date  | DATE     | Date when the book was issued   |
| return\_date | DATE     | Date when the book was returned |
