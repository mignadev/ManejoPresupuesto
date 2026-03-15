Manejo de Presupuestos

Aplicación web para el registro y control de movimientos financieros, desarrollada con ASP.NET MVC en Visual Studio, que permite a los usuarios gestionar sus cuentas, categorías y transacciones.

Características principales:

  Creación y conexión a base de datos SQL Server.
  CRUD completo de entidades: usuarios, cuentas, categorías y transacciones.
  Formularios con distintos tipos de controles: texto, dropdown, checkbox, fecha, etc.
  Uso de procedimientos almacenados y consultas SQL desde el patrón MVC.
  Implementación del principio de inversión de dependencias para mayor flexibilidad y mantenibilidad.
  Aislamiento de CSS para estilos independientes por módulo.
  Calendario mensual para visualizar transacciones.
  Exportación de transacciones a Excel.
  
Configuración del correo para recuperación de contraseña

  Para que la función de “Olvidaste tu contraseña” funcione, se envía la nueva contraseña al correo configurado.
  El correo y su contraseña se configuran en “Administrar secretos del usuario” de Visual Studio.
  Los secretos se almacenan localmente y no se suben a GitHub por seguridad.
  La configuración se divide en dos partes:
  
      1. appsettings.Development.json (configuración general)
      Define el servidor SMTP que se usará para enviar los correos:
      "CONFIGURACIONES_EMAIL": {
        "HOST": "smtp.gmail.com",
        "PUERTO": 587
      }
      
      2. archivo Secrets de usuario en Visual Studio (datos sensibles)     
      Aquí se almacenan el correo y la contraseña que usará la aplicación para enviar emails. 
      (la contraseña debe ser creada con el modo de Contraseña de Aplicación de Google, o si no no funcionará)
      Debe escribirse así:
        {
          "CONFIGURACIONES_EMAIL": {
            "EMAIL": "tu_correo@gmail.com",
            "PASSWORD": "tu_contraseña_de_aplicacion_de_google"
          }
        }
        
Cómo ejecutar el proyecto

  Abrir Visual Studio y abrir el proyecto.  
  Asegurarse de tener SQL Server instalado y en funcionamiento.
  Ejecutar el script SQL incluido en la carpeta /Database para crear y poblar la base de datos en SQL Server.
  (ejecutar el script en master, ya que el script de sql incluye la creación de la base de datos)
  Configurar los secretos del usuario en Visual Studio:
  Correo electrónico y contraseña (o contraseña de aplicación de Google para evitar conflictos con problemas de seguridad) para la recuperación de contraseña.
  Restaurar paquetes NuGet si es necesario.
Configurar los secretos del usuario en Visual Studio:
Correo electrónico y contraseña para recuperación de contraseña.
Restaurar paquetes NuGet si es necesario.
