Proyecto 2 - Manejo de Presupuestos

Aplicación de manejo de presupuestos donde los usuarios pueden registrar y controlar sus movimientos financieros.

Características principales:

  Creación y conexión a una base de datos SQL Server.
  CRUD de entidades: usuarios, cuentas, categorías y transacciones.
  Formularios con distintos tipos de controles: texto, dropdown, checkbox, fecha, etc.
  Uso de procedimientos almacenados y queries desde MVC.
  Principio de inversión de dependencias para mantener flexibilidad y mantenibilidad.
  Aislamiento de CSS.
  Calendario mensual para visualizar transacciones.
  Exportación de transacciones a Excel.
  Sistema de usuarios propio con opción de recuperación de contraseña.

Configuración de correo para recuperación de contraseña:

  Para que la función de “Olvidaste tu contraseña” funcione, se utiliza un correo electrónico que recibe la nueva contraseña.
  El correo y su contraseña se configuran en “Administrar secretos del usuario” de Visual Studio.
  Los secretos se almacenan localmente y no se suben a GitHub.

Cómo ejecutar el proyecto:

  Restaurar la base de datos ejecutando el script SQL incluido en la carpeta /Database.
  Configurar los secretos del usuario en Visual Studio (correo y contraseña).
  Abrir el proyecto en Visual Studio y ejecutar la aplicación.
