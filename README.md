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
