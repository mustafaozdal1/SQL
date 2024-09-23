## PROJE 8



### ÇÖZÜM

```
CREATE TABLE employee (
    id SERIAL PRIMARY KEY,
    name VARCHAR(50),
    birthday DATE,
    email VARCHAR(100)
);


COPY employee(name, birthday, email)
FROM 'D:/MOCK_DATA.csv'
DELIMITER ','
CSV HEADER;


UPDATE employee
SET email = 'newemail1@gmail.com'
WHERE id = 1;

UPDATE employee
SET birthday = '1990-01-01'
WHERE name = 'John';

UPDATE employee
SET name = 'Jack'
WHERE birthday = '1985-05-20';

UPDATE employee
SET id = 55
WHERE email = 'johndoe@gmail.com';

UPDATE employee
SET email = 'updatedemail@gmail.com', name = 'Ashley'
WHERE id = 2;



silme işlemi

DELETE FROM employee
WHERE id = 3;

DELETE FROM employee
WHERE name = 'Jane';

DELETE FROM employee
WHERE birthday = '1995-07-15';

DELETE FROM employee
WHERE email = 'doe@gmail.com';

DELETE FROM employee
WHERE id = 10;

```