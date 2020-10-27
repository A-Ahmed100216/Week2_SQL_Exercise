## ERD
![ERD](https://github.com/A-Ahmed100216/Week2_SQL_Exercise/blob/main/SQL_images/ERD%20Update.png)

## Code
``` sql
CREATE DATABASE assessment_aminah;
USE assessment_aminah;
CREATE TABLE user_details (
    username VARCHAR(20),
    email VARCHAR(MAX),
    phone_number VARCHAR(11)
)

CREATE TABLE ebook_details (
    Title VARCHAR(30),
    Location VARCHAR(20),
    Release_Date DATE,
    Created_by VARCHAR(20)
)
CREATE TABLE booking_details (
    Book_Title VARCHAR(30),
    Borrower_Name VARCHAR(20),
    Borrow_Date DATE,
    Cost_in_pounds DECIMAL(2,2)
)

INSERT INTO ebook_details(
    Title, Location, Release_Date, Created_by
)
VALUES (
    'Throne of Glass', 'United States','2020-10-10', 'S J Maas'
)
INSERT INTO ebook_details(
    Title, Location, Release_Date, Created_by
)
VALUES (
    'Harry Potter', 'United Kingdom','1997-06-26', 'J K Rowling'
)

INSERT INTO user_details(
    username, email, phone_number
)
VALUES (
    'Jane Doe', 'J.Doe@email.com','0123456789'
)

INSERT INTO user_details(
    username, email, phone_number
)
VALUES (
    'John Doe', 'John.Doe@email.com','0987654320'
)

INSERT INTO user_details(
    username, email, phone_number
)
VALUES (
    'S J Maas', 'SJ.Maas@email.com','03938209320'
)


SELECT * FROM ebook_details
SELECT * FROM user_details
```

![user_details](https://github.com/A-Ahmed100216/Eng74_Week2/blob/main/Images/u$
![ebook_details](https://github.com/A-Ahmed100216/Eng74_Week2/blob/main/Images/$


