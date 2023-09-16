- Descargar la imagen de MariaDB

    ```bash
    docker pull mariadb
    ```

- Crear un contenedor MariaDB

    ```bash
    docker run --detach --name some-mariadb --env MARIADB_USER=example-user --env MARIADB_PASSWORD=my_cool_secret --env MARIADB_ROOT_PASSWORD=my-secret-pw  mariadb:latest
    ```
- Conéctese a MariaDB

    ```bash
    docker exec -it some-mariadb bash
    ```
- Acceder a la base de datos
    ```bash
    mariadb -u example-user -p
    mariadb -u root -p
    ```
    [Cuando te lo pida introduce la contraseña "my_cool_secret" o "my-secret-pw" si entras como root y pulsa Enter]


- Administrar el contenedor [Sustituir "mi_base_de_datos" por el nombre del contenedor "459f8874d9a2"]

    [Detener el contenedor]
    ```bash
    docker stop mi_base_de_datos
    ```
    [Iniciar nuevamente el contenedor]
    ```bash
    docker start mi_base_de_datos
    ```
    [Eliminar el contenedor]
    ```bash
    docker rm mi_base_de_datos

    ```

- Dentro de mariaDB

    * Crear BD
    ```bash
    CREATE DATABASE my_database;
    ```
    * Entrar a la BD
    ```bash
    USE my_database;
    ```
    * Salir
    ```bash
    EXIT;
    ```
    * Crear tabla
    ```bash
    CREATE TABLE trabajadores (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(50),
    apellido VARCHAR(50),
    sueldo DECIMAL(10, 2),
    fecha_ingreso DATE,
    departamento VARCHAR(50)
    );
    ```
    * Insertar datos
    ```bash
    INSERT INTO trabajadores (nombre, apellido, sueldo, fecha_ingreso, departamento)
    VALUES
    ('Juan', 'Perez', 50000.00, '2022-01-15', 'Ventas'),
    ('Maria', 'Lopez', 45000.00, '2021-12-10', 'Recursos Humanos'),
    ('Pedro', 'Garcia', 55000.00, '2022-02-28', 'Producción'),
    ('Laura', 'Martinez', 48000.00, '2022-03-12', 'Finanzas'),
    ('Carlos', 'Hernandez', 52000.00, '2022-04-05', 'Ventas');
    ```

-
    ```bash
    
    ```