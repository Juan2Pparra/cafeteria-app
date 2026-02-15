# Cafeteria-Full-Stack (PROYECTO EN DESARROLLO)
Aplicación fullstack de e-commerce tipo cafetería desarrollada con Node.js, Express, MongoDB y jQuery. Incluye autenticación con JWT, arquitectura MVC, gestión de productos, carrito de compras y sistema de pedidos.




## Funcionalidades
- Autenticación
-Registro de usuarios
-Inicio de sesión
-Autenticación con JWT
-Productos
-Listado dinámico de productos
Visualización desde el frontend con AJAX
-Carrito de compras
-Agregar productos
-Eliminar productos
-Cambiar cantidades (+ / -)
-Interfaz hecha con HTML, CSS y jQuery
-Consumo de API con AJAX
-Diseño responsive (adaptable a celular, tablet y PC)

## Tecnologías
-Backend
-Node.js
-Express
-MongoDB
-Mongoose
-JSON Web Token (JWT)

-Frontend
-HTML5
-CSS3 (Responsive con Flexbox)
-jQuery
-AJAX
## Endpoints principales
-POST   /api/auth/register
-POST   /api/auth/login
-GET    /api/products
-POST   /api/cart
-PUT    /api/cart/:id
-DELETE /api/cart/:id


## servidor corre en:
http://localhost:3000

##Variables de entorno (.env)
PORT=3000
MONGO_URI=tu_conexion_a_mongodb
JWT_SECRET=tu_clave_secreta

## Cómo ejecutar
```bash
npm install
npm run dev
--npx nodemon server.js--
