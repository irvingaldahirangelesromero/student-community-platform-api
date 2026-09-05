# Student Community Platform API

API backend para la plataforma de la comunidad estudiantil, construida sobre Cloudflare Workers utilizando TypeScript, el estándar OpenAPI (con Chanfana) y Hono.

## Requisitos Previos

- Node.js instalado (versión LTS recomendada).
- Gestor de paquetes `pnpm`.

## Instalación y Configuración Base

1. Iniciar sesión en Cloudflare desde la terminal:

   ```bash
   pnpm dlx wrangler login
   ```

2. Instalar las dependencias del proyecto (incluyendo las definiciones de tipos para TypeScript):

   ```bash
   pnpm install
   ```

## Estructura del Proyecto

- `src/index.ts`: Punto de entrada principal y enrutador de la API.
- `src/endpoints/`: Archivos individuales para cada endpoint de la API.
- `wrangler.jsonc`: Archivo de configuración para Cloudflare Workers.

## Desarrollo Local

1. Iniciar el servidor de desarrollo local:

   ```bash
   pnpm run dev
   ```

2. Abrir [`http://localhost:8787/`](http://localhost:8787/) en el navegador para ver la interfaz de Swagger y probar los endpoints.

## Flujo de Trabajo (Git Flow)

Este proyecto implementa Git Flow para el control de versiones:

- La rama `main` contiene el estado base y de producción.
- La rama `develop` se utiliza para integrar el progreso general de desarrollo.
- Cada nueva funcionalidad o implementación debe desarrollarse en su propia rama de tipo `feature` (creada a partir de `develop`) y posteriormente integrarse mediante un Pull Request.