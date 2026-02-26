CREATE DATABASE PraktilineÜlesanne;
use PraktilineÜlesanne;

--Category tabeli liisamine
CREATE TABLE Category(
idCategory int,
Category_Name varchar(30)
);

--product tabeli liisamine
CREATE TABLE Product(
idProduct int,
Name varchar(30),
idCategory int,
Price decimal(7,2)
);

--Sale tabeli liisamine
CREATE TABLE Sale(
idSale int,
idProduct int,
idCustomer int,
Count_pr int,
Date_of_sale date
);

--UNIQUE liisamine
ALTER TABLE Category
ADD CONSTRAINT Category_Name_UNIQUE UNIQUE(Category_Name);

ALTER TABLE Product
ADD CONSTRAINT Name_UNIQUE UNIQUE(Name);

ALTER TABLE Sale
ADD CONSTRAINT idSale_UNIQUE UNIQUE(idSale);

ALTER TABLE Sale
ADD CONSTRAINT idCustomer_UNIQUE UNIQUE(idCustomer);

ALTER TABLE Sale
ADD CONSTRAINT Count_pr_UNIQUE UNIQUE(Count_pr);

--NOTNULL liisamine
ALTER TABLE Category
ALTER COLUMN idCategory int NOT NULL;

ALTER TABLE Product
ALTER COLUMN idProduct int NOT NULL;

--PK liisamine
ALTER TABLE Category
ADD CONSTRAINT pk_idCategory PRIMARY KEY(idCategory);

ALTER TABLE Product
ADD CONSTRAINT pk_idProduct PRIMARY KEY(idProduct);

--FK liisamine
ALTER TABLE Product
ADD CONSTRAINT fk_idCategory FOREIGN KEY(idCategory)
REFERENCES Category(idCategory);

ALTER TABLE Sale
ADD CONSTRAINT fk_idProduct FOREIGN KEY(idProduct)
REFERENCES Product(idProduct);

--Customer tabeli liisamine
CREATE TABLE Customer(
idCustomer int NOT NULL identity(1,1),
Name varchar(30),
contact varchar(15)
);

--PK idCustomer liisamine
ALTER TABLE Customer
ADD CONSTRAINT pk_idCustomer PRIMARY KEY(idCustomer);

--FK idCustomer liisamine
ALTER TABLE Sale
ADD CONSTRAINT fk_idCustomer FOREIGN KEY(idCustomer)
REFERENCES Customer(idCustomer);
