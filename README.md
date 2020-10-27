## ERD
![ERD](https://github.com/A-Ahmed100216/Week2_SQL_Exercise/blob/main/SQL_images/ERD%20Update.png)

## Code
``` sql
Create DATABASE Booksaurus_Aminah
USE Booksaurus_Aminah
CREATE TABLE user_details (
    UserID INT NOT NULL PRIMARY KEY,
    username VARCHAR(100) NOT NULL,
    email VARCHAR(MAX) NOT NULL,
    phone_number VARCHAR(15) NOT NULL
)

CREATE TABLE eBook_details (
    eBookID INT NOT NULL PRIMARY KEY,
    Title VARCHAR(200) NOT NULL,
    Place VARCHAR(100) NOT NULL,
    Release_Date DATE NOT NULL,
    username VARCHAR(100) NOT NULL
)

CREATE TABLE booking_details (
    BookingID INT NOT NULL PRIMARY KEY,
    Title VARCHAR(200) NOT NULL,
    Borrower_Name VARCHAR(100) NOT NULL,
    Borrow_Date DATE NOT NULL,
    Cost DECIMAL (4,2) NOT NULL
)

INSERT INTO ebook_details(
    eBookID, Title, Place, Release_Date, username
)
VALUES (
    1,'Throne of Glass', 'United States','2020-10-10', 'S J Maas'
)

INSERT INTO user_details(
    UserID, username, email, phone_number
)
VALUES (
    1, 'Jane Doe', 'J.Doe@email.com','0123456789'
)

INSERT INTO user_details(
    UserID, username, email, phone_number
)
VALUES (
    2, 'S J Maas', 'SJ.Maas@email.com','0137292893'
)


INSERT INTO booking_details(
    BookingID, Title, Borrower_Name, Borrow_Date, Cost
)
VALUES (
    1, 'Throne of Glass', 'S J Maas','2020-10-10',3.39
)


SELECT * FROM user_details
SELECT * FROM eBook_details
SELECT * FROM booking_details

```

![user_details](https://github.com/A-Ahmed100216/Week2_SQL_Exercise/blob/main/SQL_images/updated_tables.png)

