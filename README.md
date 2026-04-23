# Parish Management System - API Core

Este repositorio contiene el backend de una solución integral diseñada para la digitalización y gestión administrativa de entidades parroquiales. El sistema permite la coordinación de eventos litúrgicos, administración de ministerios y gestión automatizada de peticiones de feligreses.

## Arquitectura y Diseño

El proyecto está construido bajo los principios de **Clean Architecture**, asegurando un desacoplamiento total entre la lógica de negocio y los detalles de implementación (Frameworks, DB).

- **Domain:** Contiene las reglas de negocio puras, entidades y definiciones de interfaces (repositorios).
- **Data:** Implementación de persistencia utilizando **Prisma ORM** y acceso a datos.
- **Presentation:** Capa de entrada que maneja la lógica de los controladores, middlewares de validación y rutas de Express.
- **Domain-Driven Design (DDD):** Uso de DTOs para la transferencia de datos y manejo de errores personalizados para una API consistente.

## Stack Tecnológico

- **Runtime:** Node.js
- **Lenguaje:** TypeScript
- **Framework:** Express.js
- **ORM:** Prisma
- **Base de Datos:** PostgreSQL / MySQL
- **Testing:** Jest & Supertest (Unitarios e Integración)

## Funcionalidades Principales

- **Gestión de Calendario Litúrgico:** Sistema de eventos con validaciones de fechas y tipos de celebraciones.
- **Validación de Restricciones:** Lógica programada para restringir peticiones de intenciones en fechas de alta solemnidad.
- **Control de Acceso:** Gestión de roles para personal administrativo, clero y coordinadores de ministerios.
- **Gestión de Comunidades:** Soporte multi-sede para la administración de capillas y comunidades afiliadas.

## Calidad de Software

El proyecto incluye una suite de pruebas para garantizar la integridad de la lógica de negocio:

- **Pruebas unitarias** para las entidades del dominio.
- **Pruebas de integración** para los endpoints principales.
- **Reportes de cobertura** generados (disponibles en la carpeta `/coverage`).

## Instalación y Configuración

1. **Clonar el repositorio:**

   ```
   git clone [url-del-repo]

   ```

2. **Instalar dependencias:**

   ```
   npm install

   ```

3. **Variables de entorno:**

Configurar las variables de entorno en un archivo .env (puedes usar .env.template como referencia).

4. **Ejecutar migraciones de Prisma:**

   ```
   npx prisma migrate dev

   ```

5. **Iniciar en modo desarrollo:**

   ```
   npm run dev

   ```
