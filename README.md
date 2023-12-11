# prueba-tecnica-jr 

# Descripción
En Grupo Firma, estamos buscando un desarrollador que nos ayude a implementar un sistema de login para comenzar a construir nuestro software de renta de automóviles. Te hemos contratado para realizar nuestro login utilizando una API de pruebas. Contamos con un endpoint para el login, que es el siguiente: https://dummyjson.com/auth/login

## Características Principales del Software (OBLIGATORIAS)
A continuación, se detallan las cosas que deben implementarse en el software:

- Login simple con Angular: Utilizar el endpoint mencionado.
- Diseño responsivo: Utilizar Tailwind o Bootstrap.
- Navegación entre vistas con Angular Router.
- Protección de vistas con un guard de ruta.
- Utilización de servicios de Angular.
- Utilización de Git y Github para manejo de versiones y ramas.
- Documentación básica para la instalación.

- Nota: Todo esto se refiere a la funcionalidad principal del software: realizar el login e ingresar a una vista protegida que no se puede acceder de ninguna forma sin estar logueado.

## Características Deseables (NO OBLIGATORIAS)
Se sugiere implementar las siguientes características adicionales:

- Validación de formulario.
- Interceptor  (Angular)
- Integrar animaciones en algunos elementos.
- Arquitectura del proyecto en capas.
- Página de error para rutas no encontradas (page error 404).
- Buenas prácticas de programación (Código limpio, buen nombramiento de variables, principios SOLID, etc.).
- Commit Convencionales (Conventional Commits).
- Pruebas unitarias (E2E, Jasmine, Karma).
- Implementación de issues en GitHub para un control realista de solución de problemas y requerimientos.
- Subirlo a un servicio cloud gratuito (GitHub Pages, Render, Vercel, etc.).
- Manejo de errores (Alertas, Try Catch, etc.).
- Diagrama de flujo de usuario (Caso de uso, Diagrama de flujo que muestre lo que el usuario puede o no puede hacer).

## MockUp 

![MockUp](https://github.com/grupo-firma-developer/prueba-tecnica-jr/blob/main/mockup.png?raw=true)

## Tecnologías Utilizadas

- Node
- Angular 16
- Tailwind CSS o Bootstrap
- Git
- Github

## Ejemplo de uso api 

Credenciales para el login:

```json
{
  "username": "kminchelle",
  "password": "0lelplR",
}
```

```javascript

fetch('https://dummyjson.com/auth/login', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    
    username: 'kminchelle',
    password: '0lelplR',
    // expiresInMins: 60, // optional
  })
})
.then(res => res.json())
.then(console.log);

```

Respuesta credenciales correctas:

```json
{
  "id": 15,
  "username": "kminchelle",
  "email": "kminchelle@qq.com",
  "firstName": "Jeanne",
  "lastName": "Halvorson",
  "gender": "female",
  "image": "https://robohash.org/autquiaut.png?size=50x50&set=set1",
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MTUsInVzZXJuYW1lIjoia21pbmNoZWxsZSIsImVtYWlsIjoia21pbmNoZWxsZUBxcS5jb20iLCJmaXJzdE5hbWUiOiJKZWFubmUiLCJsYXN0TmFtZSI6IkhhbHZvcnNvbiIsImdlbmRlciI6ImZlbWFsZSIsImltYWdlIjoiaHR0cHM6Ly9yb2JvaGFzaC5vcmcvYXV0cXVpYXV0LnBuZz9zaXplPTUweDUwJnNldD1zZXQxIiwiaWF0IjoxNjM1NzczOTYyLCJleHAiOjE2MzU3Nzc1NjJ9.n9PQX8w8ocKo0dMCw3g8bKhjB8Wo7f7IONFBDqfxKhs"
}
```
Respuesta credenciales incorrectas:

```json
{message: 'Invalid credentials'}
```



## Estructura del Proyecto

- La La arquitectura sugerida para este proyecto puede ser cualquier cosa, pero se proporciona un ejemplo basado en capas:


```
-proyecto/
  ├── src/
  |    ├── app/
  |    |    ├── core/
  |    |    |    ├── models/             // Define modelos de datos
  |    |    |    |    ├── user.model.ts
  |    |    |    ├── services/           // Lógica de negocio y servicios de aplicación
  |    |    |    |    ├── auth.service.ts
  |    |    |    ├── guards/             // Guards para la autenticación y autorización
  |    |    |    |    ├── auth.guard.ts
  |    |    ├── modules/
  |    |    |    ├── login/
  |    |    |    |    ├── components/
  |    |    |    |    |    ├── login.component.ts
  |    |    |    |    |    ├── login.component.html
  |    |    |    |    |    ├── login.component.css (o .scss para estilos)
  |    |    |    |    ├── login.module.ts
  |    |    |    ├── protected-page/
  |    |    |    |    ├── components/
  |    |    |    |    |    ├── protected-page.component.ts
  |    |    |    |    |    ├── protected-page.component.html
  |    |    |    |    |    ├── protected-page.component.css (o .scss para estilos)
  |    |    |    |    ├── protected-page.module.ts
  |    ├── shared/
  |    |    ├── components/               // Componentes compartidos
  |    |    |    ├── header/
  |    |    |    |    ├── header.component.ts
  |    |    |    |    ├── header.component.html
  |    |    |    |    ├── header.component.css (o .scss para estilos)
  |    |    ├── directives/               // Directivas compartidas
  |    |    ├── pipes/                    // Pipes compartidos
  |    ├── assets/
  ├── ...
  ├── README.md

```

## Actividades a realizar paso a paso
- Crear proyecto con angular
- Crear repositorio de github
- Subir proyecto base a la rama dev
- Crear rama dev-[tu nombre aqui] por lo que quedaria algo asi " dev-ramiro " por ejemplo 
- Integrar dependencias nesecarias
- Crear estructura del proyecto
- Implementar características principales del software
- Hacer merge con rama master o main del proyecto (Por lo que solo debemos tener un merge)
- Opcional (En caso de tener issues indicar el issues que hace referencia con el numero del issue)

## Envio de la prueba tecnica 
- Debes crear un repositorio publico llamado prueba-tecnica-jr-gf y subir tu proyecto
- Compartir el repositorio con nosotros mediante email u algun medio de contacto






