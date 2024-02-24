
# Introduccion SQL


Creacion de tabla
```
CREATE TABLE empleados (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100),
    edad INT,
    salario DECIMAL(10, 2)
);
```


Agregar informacion
```
INSERT INTO empleados (nombre, edad, salario) VALUES ('Juan', 30, 50000.00);
INSERT INTO empleados (nombre, edad, salario) VALUES ('María', 25, 60000.00);
INSERT INTO empleados (nombre, edad, salario) VALUES ('Pedro', 35, 55000.00);
```


Mas informacion en conjunto
```
INSERT INTO empleados (nombre, edad, salario) VALUES
('Juan Pérez', 30, 55000.00),
('María García', 25, 60000.00),
('Pedro Rodríguez', 35, 62000.00),
('Luisa Martínez', 28, 58000.00),
('Ana Sánchez', 32, 57000.00),
('Carlos Gómez', 27, 53000.00),
('Laura Hernández', 31, 59000.00),
('Daniel López', 29, 54000.00),
('Sofía Díaz', 33, 61000.00),
('Javier Fernández', 26, 52000.00),
('Lucía Vázquez', 34, 60000.00),
('Elena Ruiz', 30, 55000.00),
('Diego Moreno', 25, 59000.00),
('Sara Castro', 35, 62000.00),
('Mario Navarro', 28, 58000.00),
('Silvia Jiménez', 32, 57000.00),
('Alejandro Flores', 27, 53000.00),
('Natalia Rojas', 31, 59000.00),
('Roberto Medina', 29, 54000.00),
('Paula Serrano', 33, 61000.00),
('Manuel Ortiz', 26, 52000.00),
('Carmen Guerrero', 34, 60000.00),
('Antonio Molina', 30, 55000.00),
('Eva Delgado', 25, 59000.00),
('Miguel Torres', 35, 62000.00),
('Isabel Ramos', 28, 58000.00),
('Rafael Reyes', 32, 57000.00),
('Cristina Cruz', 27, 53000.00),
('Pablo Blanco', 31, 59000.00),
('Adriana Muñoz', 29, 54000.00);
```

Consultar informacion
```
SELECT * FROM empleados;
```

Consultar informacion selectiva
```
SELECT nombre, salario FROM empleados;
```

Actualizar datos en la tabla
```
UPDATE empleados SET salario = 52000.00 WHERE nombre = 'Juan';
```

Eliminar un registro de la tabla
```
DELETE FROM empleados WHERE nombre = 'Pedro';
```

Seleccionar datos con filtrado básico:
```
SELECT * FROM empleados WHERE edad > 25;
```

Seleccionar datos con un ordenamiento
```
SELECT * FROM empleados ORDER BY salario DESC;
```

Seleccionar la suma de los salarios de empleados con mas de 35 años, usando un alias
```
SELECT SUM(salario) AS suma_salarios
FROM empleados
WHERE edad > 25;
```

