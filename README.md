# Huellitas felices

Backend para sistema de gestión para negocios de petshop y veterinaría desarrollado con Node.js y Express.

## Descripción

Alquilarte Backend es un sistema de gestión para negocios de petshop y veterinaría, desarrollado con Node.js y Express, siguiendo un patrón de arquitectura MVC (Modelo-Vista-Controlador). El proyecto forma parte de un trabajo práctico para la materia de Desarrollo Web Backend.

## Información Técnica

- **Plataforma:** Node.js  
- **Framework:** Express.js  
- **Almacenamiento de datos:** Archivos JSON  
- **Motor de plantillas:** Pug  
- **Versión actual:** 1.0.0  
- **Puerto del servidor:** 5050  

## Estructura del Proyecto

```
```
backendHuellitas/
├── src/                     # Código fuente
│   ├── app.js               # Punto de entrada de la aplicación
│   ├── controllers/         # Controladores
│   ├── database/            # Archivos JSON de almacenamiento
│   ├── middlewares/         # Middlewares personalizados
│   ├── models/              # Definición de modelos
│   ├── repositories/        # Acceso a datos
│   ├── routes/              # Definición de rutas
│   │   ├── api/             # Rutas para API REST
│   │   └── views/           # Rutas para las vistas
│   ├── services/            # Servicios (lógica de negocio)
│   └── views/               # Plantillas Pug
├── .env                     # Variables de entorno
├── .gitignore               # Archivos ignorados por Git
├── package.json             # Configuración y dependencias del proyecto
└── package-lock.json        # Versiones específicas de las dependencias
```
```

## Endpoints API

### Usuarios

| Método | Ruta                | Descripción             | Parámetros de consulta | Cuerpo de solicitud         | Códigos de respuesta |
|--------|---------------------|-------------------------|------------------------|-----------------------------|----------------------|
| GET    | /api/usuarios       | Listar todos los usuarios | email (opcional)      | N/A                         | 200, 404             |
| GET    | /api/usuarios/:id   | Obtener usuario por ID  | N/A                   | N/A                         | 200, 404             |
| POST   | /api/usuarios       | Crear nuevo usuario     | N/A                   | {nombre, rol, email}        | 201, 400             |
| DELETE | /api/usuarios/:id   | Eliminar usuario        | N/A                   | N/A                         | 200, 404, 400        |

### Propiedades

| Ruta                      | Descripción                  | Método |
|---------------------------|------------------------------|--------|
| /propiedades              | Lista de propiedades         | GET    |
| /propiedades/nueva        | Formulario de nueva propiedad| GET    |
| /propiedades/:id          | Detalle de propiedad         | GET    |
| /propiedades/:id/editar   | Formulario de edición        | GET    |

### Rutas de Vistas

| Ruta                | Descripción                    | Método |
|---------------------|-------------------------------|--------|
| /usuarios           | Lista de usuarios             | GET    |
| /usuarios/nuevo     | Formulario de nuevo usuario   | GET    |
| /usuarios/:id       | Detalle de usuario            | GET    |
| /usuarios/:id/editar| Formulario de edición         | GET    |
| /auth/login         | Formulario de inicio de sesión| GET    |
| /auth/register      | Formulario de registro        | GET    |

## Requisitos de Instalación y Ejecución

### Requisitos previos

- Node.js (v14 o superior)
- npm (v6 o superior)

### Instalación

```bash
# Clonar el repositorio
git clone [URL_DEL_REPOSITORIO]

# Instalar dependencias
npm install
```

### Ejecución

```bash
# Modo desarrollo
npm run dev

# Modo producción
npm start
```

El servidor estará disponible en [http://localhost:3000](http://localhost:3000)