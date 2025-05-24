# Request Header Parser Microservice

This is the boilerplate for the Request Header Parser Microservice project. Instructions for building your project can be found at https://www.freecodecamp.org/learn/apis-and-microservices/apis-and-microservices-projects/request-header-parser-microservice

Este repositorio contiene dos microservicios creados como parte del curso de APIs y Microservicios de FreeCodeCamp:

1. **Request Header Parser Microservice**
2. **URL Shortener Microservice**

## Descripción de funcionalidades

### Request Header Parser

Este microservicio devuelve los datos del encabezado de una solicitud HTTP en formato JSON.

#### `/api/whoami`

Devuelve:

- `ipaddress`: la IP del cliente.
- `language`: el idioma preferido del cliente.
- `software`: el sistema operativo y navegador del cliente.

#### Ejemplo de respuesta

```json
{
  "ipaddress": "::ffff:159.20.14.100",
  "language": "en-US,en;q=0.5",
  "software": "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:50.0) Gecko/20100101 Firefox/50.0"
}
```

### URL Shortener

Permite acortar URLs y redirigir a ellas usando un número corto.

#### `/api/shorturl` 

Puedes hacer un POST y obtener una respuesta en JSON con las propiedades `original_url` y `short_url`. Ejemplo:

```json
{ "original_url": "https://freeCodeCamp.org", "short_url": 1 }
```

---

## Tecnologías

- Node.js
- Express

---

## Cómo ejecutar el proyecto

1. Clona el repositorio:

```bash
git clone https://github.com/TheMasterShoot/project-headerparser-microservice.git
```

2. Instala las dependencias:

```bash
npm install
```

3. Inicia el servidor:

```bash
npm start
```

4. Accede a la aplicación desde tu navegador:

```bash
http://localhost:3000
```

---

## Pruebas

1. Debes proporcionar tu propio proyecto, no la URL de ejemplo.
2. Puedes hacer un `POST` a `/api/shorturl` y obtener una respuesta en JSON con las propiedades `original_url` y `short_url`. Ejemplo:

```json
{ "original_url": "https://freeCodeCamp.org", "short_url": 1 }
```

3. Al visitar `/api/shorturl/<short_url>`, serás redirigido a la URL original.
4. Si envías una URL inválida que no sigue el formato válido como `http://www.example.com`, la respuesta en JSON contendrá:

```json
{ "error": "invalid url" }
```
