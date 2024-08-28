`--1.test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.`


```SQL
CREATE TABLE employee (
    id INT,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    email VARCHAR(100),
    birthday DATE
);
```


`--2.Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.`

```SQL
INSERT INTO employee(name,birthday,email) VALUES
```


`--3.Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.`
--1.id sütununa göre güncelleme

```SQL
UPDATE employee
SET first_name = 'Updated Name'
WHERE id = 1;
```

`--2.first_name sütununda güncelleme`
```SQL
UPDATE employee
SET email = 'updated.email@example.com'
WHERE first_name='John Doe';
```

`--3.birthday sütununa göre güncelleme`
```SQL
UPDATE employee
SET first_name = 'New Name'
WHERE birthday = '1997-09-02'
```
`--4. email sütununa göre güncelleme`
```SQL
UPDATE employee 
SET birthday ='1997-01-01'
WHERE email = 'zazaza.@gmail.com'
```
`--5. id sütununa göre güncelleme`
```SQL
UPDATE employee
SET first_name='another name' , email = 'another.email@gmail.com'
WHERE id=2;
```

`--4.Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.`
```SQL
DELETE FROM employee
WHERE id=3;

DELETE FROM employee
WHERE first_name = 'John Doe';

DELETE FROM employee
WHERE birthday='1985-09-09';

DELETE FROM employee
WHERE email='dfgsdjfsdf@gmail.com';

DELETE FROM employee
WHERE first_name='jane Smith' AND birthday = '1999-09-08';
```
