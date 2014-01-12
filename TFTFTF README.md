ti
==

technologie internetowe


drop DATABASE pojedynek_na_dzikim_zach
USE sklep

CREATE DATABASE pojedynek_na_dzikim_zach
USE pojedynek_na_dzikim_zach
GO

CREATE TABLE przestepca (
id_przestepca INT IDENTITY(1,1) PRIMARY KEY,
imie VARCHAR(15) NOT NULL CHECK(LEN(imie)>2),
nazwisko VARCHAR(20)NOT NULL CHECK(LEN(nazwisko)>2),
pseudonim VARCHAR(20)UNIQUE,
glowne_przestepstwo VARCHAR(25),
stan_prawny VARCHAR(20),
miejsce_pobytu VARCHAR(30),
wartosc_nagrody MONEY CHECK(wartosc_nagrody>0),
);
GO

INSERT INTO przestepca
VALUES ('JOHN', 'DALTON', 'BRODATY', 'KRADZIEZE', 'POSZUKIWANY', 'SANTA FE', '1000');
INSERT INTO przestepca
VALUES ('FRANK', 'SMITH', 'SZALONY FRANK', 'ZABUJSTWA', 'PODZUKIWANY', 'SWEETWATER', '5000');
INSERT INTO przestepca
VALUES ('TUCO', 'RAMIREZ', 'BRZYDKI', 'GWAŁT', 'ZBIEG', 'FORT SUMNER', '7000');
INSERT INTO przestepca
VALUES ('PABLO', 'GOMEZ', 'EL INDIO', 'NAPADY NA BANK', 'POSZUKIWANY', 'EL PASO', '10000');
INSERT INTO przestepca
VALUES ('JUAN', 'LIMA', 'DZIKI', 'KRADZIEŻE BYDŁA', 'POSZUKIWANY', 'AQUA CALIENTE', '2000');
INSERT INTO przestepca
VALUES ('PIKE', 'BISHOP', NULL, 'NAPADY NA BANK', 'ZBIEG', 'SAN RAFAEL', '1500');
INSERT INTO przestepca
VALUES ('WILLIAM', 'BONNEY', 'BILLY KID', 'ZABUJSTWA', 'POSZUKIWANY', 'FORT SUMMER', '5000');
