# CRM Dashboard Example

## Descripción

Este proyecto es un CRM (Customer Relationship Management) básico con funcionalidades de gestión y visualización de datos. Incluye las siguientes vistas principales:

1. **Dashboard de Gráficos**: Visualización de estadísticas de ventas (Datos estáticos).
2. **Gestión de Usuarios**: Administración de usuarios.
3. **Configuración**: Personalización del sistema.

### Estructura del Proyecto
El sistema está compuesto por dos submódulos:
- **Frontend**: Construido con Next.js 15 y Tailwind CSS, consume servicios desde el backend mediante Apollo Client.
- **Backend**: API desarrollada con Node.js y GraphQL, utilizando Apollo Server y Express.

## Tecnologías

- **Frontend**: Next.js, Tailwind CSS, Apollo Client.
- **Backend**: Node.js, GraphQL, Apollo Server.
- **Contenedores**: Docker y Docker Compose.
- **Base de Datos**: SQLite (u otra según configuración).

## Funcionalidades

### General
- Soporte para modo oscuro.
- Diseño con Tailwind CSS.
- Integración entre frontend y backend mediante Apollo Client.
- Ingreso y registro de usuarios.
  
### Vistas

#### Ingreso
- Ingreso a la plataforma con correo con número máximo de intentos.

#### Registro
- Registro a la plataforma con nombre, correo y confirmación de contraseña.
    
#### Dashboard
- Gráficos de barras y pastel.
- Panel de últimas ventas.
- Panel de notificaciones.

#### Dashboard
- Gráficos de barras y pastel.
- Panel de últimas ventas.
- Panel de notificaciones.

#### Gestión de Usuarios
- Operaciones de gestión de acceso y perfiles (Administrador y Operador).
- Validación de datos en frontend y backend.

#### Configuración
- Activación y desactivación del modo oscuro.

## Instalación y Configuración

### Prerrequisitos
- **Docker** y **Docker Compose** instalados en tu máquina.

### Clonar repositorios
```
git submodule init
git submodule update
```
### Variables de Entorno
#### Frontend (`dashboard-app/.env`)
```env
NEXT_PUBLIC_GRAPHQL_API=http://localhost:4000/graphql
PORT=3000
```
#### Backend (`dashboard-service/.env`)
```env
JWT_SECRET_KEY=your_secret_key
PORT=4000
```
### Despliegue Local
#### Construir y ejecutar los servicios
```
docker-compose up --build
```

#### Accede a la aplicación
- Frontend: [http://localhost:3000](http://localhost:3000)
- Backend: [http://localhost:4000/graphql](http://localhost:4000/graphql)

#### Detener los servicios
```
docker-compose down
```


