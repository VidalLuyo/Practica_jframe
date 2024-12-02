# Practica_jframe

drop database R_VidalLuyo;
create database R_VidalLuyo;
use R_VidalLuyo;

CREATE TABLE CLIENTE (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    DNI CHAR(8) NOT NULL,
    NOMBRES VARCHAR(100) NOT NULL,
    APELLIDOS VARCHAR(100) NOT NULL,
    DIRECCION VARCHAR(255),
    CELULAR VARCHAR(15),
    SEXO CHAR(1) NOT NULL CHECK (SEXO IN ('M', 'F'))
);

INSERT INTO CLIENTE (DNI, NOMBRES, APELLIDOS, DIRECCION, CELULAR, SEXO) VALUES
('12345678', 'Juan', 'Pérez', 'Av. Principal 123', '987654321', 'M'),
('87654321', 'María', 'Lopez', 'Calle Secundaria 456', '987654322', 'F'),
('45678912', 'Carlos', 'Ramírez', 'Jr. Lima 789', '987654323', 'M'),
('65432198', 'Ana', 'García', 'Av. Perú 101', '987654324', 'F'),
('78912345', 'Luis', 'Fernández', 'Calle Central 202', '987654325', 'M');


SELECT * FROM CLIENTE WHERE SEXO = 'M';
