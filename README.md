# Cafetería Web App – Full Stack

Aplicación web de pedidos online tipo cafetería desarrollada con **Node.js, Express, MongoDB y jQuery**, siguiendo arquitectura **MVC** y autenticación con **JWT**.

El sistema permite a los clientes registrarse, realizar pedidos personalizados y a los administradores gestionar productos y pedidos desde un panel administrativo.

---

## Demo Local

Servidor corre en:
http://localhost:3000

---

# Funcionalidades Implementadas

## Autenticación y Roles

- Registro de usuarios
- Inicio de sesión
- Autenticación con JSON Web Token (JWT)
- Protección de rutas con middleware
- Sistema de roles:
  - Cliente
  - Administrador

---

## Productos

- Listado dinámico desde MongoDB
- Carga mediante AJAX
- Visualización con imagen, descripción y precio
- Subida de imágenes desde:
  - Archivo local
  - Ctrl + V (pegado directo)
- Almacenamiento de imágenes en `/uploads`
- Gestión completa desde panel admin:
  - Crear
  - Editar
  - Eliminar

---

## Carrito de Compras

- Agregar productos
- Seleccionar cantidad (+ / -)
- Seleccionar opción:
  - Con azúcar
  - Sin azúcar
- Modificar cantidades
- Eliminar productos
- Cálculo automático del total
- Persistencia en base de datos por usuario

---

## Sistema de Pedidos

- Conversión del carrito en pedido real
- Formulario obligatorio de:
  - Nombre
  - Teléfono
  - Dirección
- Campo opcional:
  - Descripción adicional (ej: apartamento, casa, etc.)
- Generación de mini factura con:
  - Productos
  - Cantidades
  - Opciones
  - Total
  - Fecha
  - Estado del pedido
- Historial de pedidos por usuario

---

## Panel de Administración

### Gestión de Productos
- CRUD completo
- Subida y gestión de imágenes
- Interfaz estilizada y responsive

### Gestión de Pedidos
- Visualización de todos los pedidos
- Información del cliente
- Cambio de estado:
  - Pendiente
  - Preparando
  - Listo
  - Entregado
  - Cancelado

---

# Frontend

Diseño moderno inspirado en landing profesional con:

- HTML5
- CSS3 (Flexbox + Responsive)
- jQuery
- AJAX
- Font Awesome
- Parallax
- Slider dinámico
- Modal de imágenes
- Scroll suave
- Sticky header
- Diseño adaptable a móvil, tablet y escritorio

---

# Arquitectura

Proyecto estructurado con arquitectura MVC:
src
├── models
├── controllers
├── services
├── routes
├── middleware
└── config

Separación clara entre:
- Lógica de negocio
- Controladores
- Rutas
- Modelos
- Servicios

---

# Tecnologías

## Backend
- Node.js
- Express
- MongoDB
- Mongoose
- JSON Web Token (JWT)
- Multer (subida de imágenes)

## Frontend
- HTML5
- CSS3
- jQuery
- AJAX
- Font Awesome

---
# Variables de entorno 
PORT=3000
MONGO_URI=tu_conexion_mongodb
JWT_SECRET=tu_clave_secreta

#Cómo ejecutar el proyecto
npm install
npm run dev
npx nodemon server.js

#Estado del Proyecto
-Autenticación completa
-Carrito persistente
-Sistema de pedidos con mini factura
-Panel administrativo
-Subida de imágenes
-Diseño responsive y moderno

Proyecto listo para despliegue y mejoras futuras (pagos online, dashboard estadístico, etc.).

# Endpoints Principales

```http
POST   /api/auth/register
POST   /api/auth/login
GET    /api/auth/me

GET    /api/products
POST   /api/products        (admin)
PUT    /api/products/:id    (admin)
DELETE /api/products/:id    (admin)

GET    /api/cart
POST   /api/cart/add
PUT    /api/cart/:id
DELETE /api/cart/:id

POST   /api/orders
GET    /api/orders
GET    /api/orders/all      (admin)
PUT    /api/orders/:id      (admin)
