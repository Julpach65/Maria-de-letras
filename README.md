# María de Letras: Sistema de Gestión de Librería

Bienvenido a **María de Letras**, una solución para el control de inventario, ventas y administración de librerías. Este sistema ha sido diseñado con un enfoque profesional, priorizando la confiabilidad de los datos y la experiencia del usuario, incluso en condiciones de conectividad inestable.

## Características Principales

### Tecnología Offline-First (PWA)
Gracias a la implementación de **Service Workers** e **IndexedDB**, el sistema permite operar el punto de venta sin conexión a Internet.
- **Ventas sin interrupciones**: Registra ventas y genera tickets provisionales aunque no haya red.
- **Sincronización Inteligente**: Los datos se sincronizan automáticamente con el servidor una vez que se restablece la conexión.
- **Catálogo Local**: Búsquedas rápidas de productos garantizadas mediante una copia local del inventario.

###  Seguridad y Control de Acceso
- **Autenticación Robusta**: Gestión de sesiones protegida con encriptación Bcrypt para contraseñas.
- **Roles de Usuario**: Niveles de acceso diferenciados para **Administradores** (control total) y **Operadores** (ventas y consultas).

###  Gestión de Inventario y Ventas
- **Transacciones Atómicas**: Garantizamos que cada venta impacte correctamente el stock mediante transacciones SQL (Commit/Rollback).
- **Módulo de Compras y Devoluciones**: Registro detallado de entradas de mercancía y gestión de reclamaciones.
- **Reportes Profesionales**: Generación de reportes de ventas y estados de inventario listos para imprimir.

###  Interfaz Moderna y Responsiva
Diseño visual premium construido con CSS puro, optimizado para una navegación fluida en dispositivos de escritorio y móviles.

## Guía de Instalación

### Requisitos Previos
- Servidor local XAMPP con PHP 7.4+ y MySQL 5.7+.
- Navegador compatible con PWAs (Chrome, Edge, Firefox).

### Pasos para Configurar
1. **Clonar el Repositorio**:
   ```bash
   git clone https://github.com/julpa-upsin/Maria-de-letras.git
   ```

2. **Configurar la Base de Datos**:
   - Acceder a phpMyAdmin.
   - Crear una base de datos llamada `libreria_db`.
   - Importar el archivo `database/schema.sql` (Estructura).
   - Importar `database/seed.sql` (Datos iniciales).

3. **Ajuste de Conexión**:
   - Edite el archivo `config/db.php` con sus credenciales locales.

4. **Ejecutar**:
   - Inicie Apache y MySQL en su servidor.
   - Acceda desde `http://localhost/Maria-de-letras`.


