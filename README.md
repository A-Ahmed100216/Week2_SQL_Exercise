## ERD
![ERD](https://github.com/A-Ahmed100216/Week2_SQL_Exercise/blob/main/SQL_images/ERD%20Update.png)

## Code
``` sql
Create DATABASE Booksaurus_Aminah
USE Booksaurus_Aminah
CREATE TABLE user_details (
    UserID INT NOT NULL IDENTITY(1,1) PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(MAX) NOT NULL,
    phone_number VARCHAR(15) NOT NULL
);

CREATE TABLE eBook_details (
    AuthorID INT NOT NULL REFERENCES user_details(UserID),
    eBookID INT NOT NULL Identity(1,1) PRIMARY KEY,
    Title VARCHAR(200) NOT NULL,
    Place VARCHAR(100) NOT NULL,
    Release_Date DATE NOT NULL,
);

CREATE TABLE booking_details (
    BookingID INT NOT NULL IDENTITY(1,1) PRIMARY KEY,
    Title INT NOT NULL REFERENCES eBook_details(eBookID),
    Borrower INT NOT NULL REFERENCES user_details(UserID),
    Borrow_Date DATE NOT NULL,
    Cost DECIMAL (4,2) NOT NULL
);

INSERT INTO ebook_details(AuthorID,Title, Place, Release_Date)
VALUES (2, 'Throne of Glass', 'United States','2020-10-10')

INSERT INTO user_details(full_name, email, phone_number)
VALUES ('Jane Doe', 'J.Doe@email.com','0123456789')

INSERT INTO user_details(full_name, email, phone_number)
VALUES ('S J Maas', 'SJ.Maas@email.com','0137292893')

INSERT INTO booking_details(Title, Borrower, Borrow_Date, Cost)
VALUES (2, 2,'2020-10-10',3.39)



SELECT * FROM user_details
SELECT * FROM eBook_details
SELECT * FROM booking_details
```

![user_details](https://github.com/A-Ahmed100216/Week2_SQL_Exercise/blob/main/SQL_images/updated_tables.png)

