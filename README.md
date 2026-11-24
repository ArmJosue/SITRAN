# SITRAN - Sistema de Control de Rutas y Personal

![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![.NET Framework](https://img.shields.io/badge/.NET%20Framework-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![ASP.NET MVC](https://img.shields.io/badge/ASP.NET%20MVC-0078D4?style=for-the-badge&logo=dotnet&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)

**SITRAN** es una aplicación web empresarial desarrollada en **C# con ASP.NET Framework (MVC)** y **SQL Server**, diseñada para gestionar y controlar las rutas de transporte interno o corporativo en empresas privadas, centralizando el registro y asignación de todo el personal operativo involucrado (conductores, vigilantes, coordinadores y empleados).

## Características principales

* **Gestión integral de personal por roles:** Registro, edición y control de empleados diferenciados por cargo y responsabilidades (conductores, personal de seguridad/vigilantes, supervisores y pasajeros).
* **Administración de rutas y horarios:** Creación y mantenimiento de rutas empresariales, puntos de parada, turnos y frecuencias de salida/llegada.
* **Asignación operativa:** Vinculación de conductores, vigilantes y unidades de transporte a rutas específicas según la programación diaria o semanal.
* **Control y bitácora de viajes:** Seguimiento del estado de los recorridos, registro de novedades en ruta y control de cumplimiento.
* **Seguridad y control de acceso:** Autenticación de usuarios y permisos basados en roles dentro del sistema.

## Tecnologías utilizadas

* **Lenguaje:** C#
* **Framework Web:** ASP.NET Framework (Patrón Modelo-Vista-Controlador / MVC 5)
* **Frontend:** Razor Views (`.cshtml`), HTML5, CSS3, Bootstrap, JavaScript / jQuery
* **Acceso a datos:** Entity Framework / ADO.NET
* **Base de datos:** Microsoft SQL Server (administrada mediante SQL Server Management Studio - SSMS)
* **IDE:** Visual Studio

## Estructura del proyecto

```text
SITRAN/
├── Controllers/       # Controladores MVC (Rutas, Empleados, Asignaciones, Acceso)
├── Models/            # Modelos de datos, ViewModels y contexto de base de datos
├── Views/             # Vistas Razor organizadas por módulo
├── Scripts/           # Archivos JavaScript y librerías del cliente
├── Content/           # Hojas de estilo CSS y recursos estáticos
├── Database/          # Scripts SQL (.sql) para creación de tablas y datos iniciales
└── Web.config         # Configuración de la aplicación y cadena de conexión
```

## Requisitos previos

Para ejecutar este proyecto en un entorno local necesitas:

* **Visual Studio 2019 o 2022** con la carga de trabajo *Desarrollo de ASP.NET y web*.
* **.NET Framework 4.7.2** (o la versión específica configurada en el proyecto).
* **SQL Server** (Express, Developer o Standard) y **SQL Server Management Studio (SSMS)**.

## Instalación y configuración

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/tu-usuario/SITRAN.git](https://github.com/tu-usuario/SITRAN.git)
   ```

2. **Configurar la base de datos en SSMS:**
   * Abre **SQL Server Management Studio (SSMS)** y conéctate a tu instancia local de SQL Server.
   * Crea una nueva base de datos llamada `SITRAN_DB` (o restaura el respaldo `.bak` si se incluye en la carpeta `Database/`).
   * Abre y ejecuta el script SQL ubicado en `Database/script_sitran.sql` para generar las tablas, relaciones y registros iniciales.

3. **Configurar la cadena de conexión:**
   * Abre la solución `SITRAN.sln` en **Visual Studio**.
   * Abre el archivo `Web.config` en la raíz del proyecto web.
   * Ubica la sección