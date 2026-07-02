# 🏢 GestFincas 2.0

![PHP Version](https://img.shields.io/badge/PHP-8.0+-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-MVC-success?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-MVP-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

*Plataforma SaaS (B2B/B2C) orientada al sector PropTech para la digitalización, administración y gestión eficiente de comunidades de vecinos.*

## 💡 Propuesta de Valor (PropTech)

**GestFincas 2.0** centraliza y moderniza la administración tradicional de fincas resolviendo los puntos de fricción más comunes en las comunidades residenciales. Nuestro producto ofrece:

- **Gestión Integral de Viviendas:** Control centralizado del censo de propietarios e inquilinos.
- **Control de Accesos Seguro:** Sistema de validación de identidades mediante códigos únicos para residentes y juntas directivas.
- **Comunicación Transparente:** Un canal directo que elimina los cuellos de botella informativos entre los vecinos y la figura del presidente o administrador.

## 🛠️ Stack Tecnológico

La plataforma está construida priorizando el rendimiento, la escalabilidad y los estándares de desarrollo web:

- **Backend:** PHP Nativo (v8.0 o superior).
- **Base de Datos:** MySQL / MariaDB (Relacional).
- **Frontend:** HTML5, CSS3 y Vanilla JavaScript (Enfoque ligero, sin dependencias pesadas).
- **Patrón de Arquitectura:** MVC (Modelo-Vista-Controlador).

## 🏗️ Arquitectura del Sistema

El proyecto sigue una separación estricta de responsabilidades (SoC) basada en el patrón MVC, garantizando un código mantenible y modularizado:

- 📂 `/config/`: Configuraciones críticas del entorno (Enrutador, credenciales de DB) y scripts de persistencia de datos (SQL).
- 📂 `/public/`: Document Root de la aplicación. Contiene el Front Controller (`index.php`) y recursos estáticos (`/assets`). Todo el tráfico web debe apuntar aquí por seguridad.
- 📂 `/src/`: Directorio principal del Core de negocio:
  - `controllers/`: Orquestación lógica, manejo de *requests* HTTP y control de sesiones (ej. `AuthController.php`).
  - `models/`: Abstracción de datos, sanitización y consultas directas a la base de datos (ej. `UsuarioModel.php`).
  - `views/`: Renderizado de interfaces de usuario y componentes visuales reutilizables.

## 🚀 Guía de Inicio Rápido (Quick Start)

### 1. Requisitos Previos
Asegúrate de contar con el siguiente stack en tu entorno local:
- Entorno de servidor local (XAMPP, WAMP, MAMP o Docker).
- PHP 8.0+
- Servidor MySQL / MariaDB activo.
- Git.

### 2. Despliegue Local
Abre tu terminal y ejecuta los siguientes comandos en la carpeta pública de tu servidor (ej. `htdocs` o `www`):

```bash
# Clonar el repositorio
git clone [https://github.com/tu-usuario/GestFincas2.0.git](https://github.com/tu-usuario/GestFincas2.0.git)

# Acceder al directorio del proyecto
cd GestFincas2.0
```
### 3. Configuración de Base de DatosAccede a tu gestor de base de datos (ej. phpMyAdmin o DBeaver).Crea una base de datos vacía llamada exactamente: gestfincas.Importa el volcado inicial ejecutando o importando el archivo config/gestfincas.sql. Esto construirá el esquema y cargará datos semilla (seeders).

### 4. Credenciales Seguras y Variables de EntornoPor políticas de seguridad, las credenciales nunca se suben al repositorio. Para configurar tu conexión local:
```Bash
# Duplica el archivo de ejemplo para crear tu configuración local
cp config/config.php.example config/config.local.php
```
Edita config/config.local.php con los datos de tu entorno:
PHP
<?php
return [
    'host'    => 'localhost', // o 127.0.0.1
    'db'      => 'gestfincas',
    'user'    => 'root',      // Usuario de BD local
    'pass'    => '',          // Contraseña de BD local
    'charset' => 'utf8mb4'
];
?>
Arrancar la aplicación:Navega en tu navegador web a la ruta pública:
http://localhost/GestFincas2.0/public/index.php

## 🔑 Datos de Acceso (Test Environment)

El script SQL inicial despliega usuarios de prueba para validar los flujos del producto inmediatamente tras la instalación:

Rol de Usuario,Nombre de Vivienda,Correo Electrónico (Login),Contraseña
Vecino / Test,Planta 2-1B,mariapelaez@gmail.com,casacasa

(Recomendamos cambiar estas credenciales tras el primer inicio de sesión por motivos de auditoría).

## 🤝 Contribución y Licencia

Este proyecto está distribuido bajo la licencia MIT. Eres libre de utilizarlo, modificarlo y distribuirlo comercialmente.Si deseas contribuir al desarrollo:Haz un Fork del repositorio.Crea una rama para tu feature (git checkout -b feature/NuevaFuncionalidad).Realiza tus commits (git commit -m 'feat: Añade integración con Stripe').Sube los cambios (git push origin feature/NuevaFuncionalidad) y abre un Pull Request.
