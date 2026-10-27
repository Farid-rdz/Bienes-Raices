# Bienes Raíces

Proyecto académico con PHP y MySQL para consultar y administrar propiedades. Incluye autenticación y operaciones de creación, consulta, actualización y eliminación.

## Estructura

- `admin/`: panel y operaciones sobre propiedades.
- `includes/`: conexión, funciones y plantillas.
- `src/`: SCSS, JavaScript e imágenes fuente.
- `build/`: recursos compilados listos para usar.
- `imagenes/`: fotografías subidas.
- `Bienes-Raices-db/`: SQL y modelo de Workbench.

## Ejecutar localmente

1. Descarga el repositorio e inicia MySQL.
2. En una base nueva ejecuta `Bienes-Raices-db/BienesRaicesSchema.sql` una sola vez.
3. El SQL original no incluye la tabla de acceso. Ejecuta:

```sql
USE bienes_raices_crud;
CREATE TABLE IF NOT EXISTS usuarios (
 id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
 email VARCHAR(255) NOT NULL UNIQUE,
 password VARCHAR(255) NOT NULL
);
```

4. Ajusta las credenciales locales en `includes/config/database.php`.
5. Desde la raíz del proyecto ejecuta `php -S localhost:8000` (o utiliza la ruta de PHP de XAMPP).
6. En una instalación nueva abre `/usuario.php` una sola vez. La cuenta de demostración es `correo@correo.com` / `123456`. Retira ese archivo de la carpeta pública después de crear la cuenta.
7. Abre `http://localhost:8000/login.php` para administrar propiedades.

Los archivos de `build/` están incluidos. Para trabajar con las fuentes, instala Node y ejecuta `npm ci` y `npm run dev`. `node_modules` no se versiona.

