# API-REST-con-JWT
<div align="center">
  <img src="https://jwt.io/img/pic_logo.svg" alt="JWT Logo" width="120" />
  <img src="https://www.vectorlogo.zone/logos/prisma/prisma-icon.svg" alt="Prisma Logo" width="110" />
  
  <h1>🚀 API REST con JWT & Prisma</h1>
  <p><i>Una API robusta, segura y escalable desarrollada con Node.js y TypeScript</i></p>

  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white" alt="Prisma" />
  <img src="https://img.shields.io/badge/pnpm-%234a4a4a.svg?style=for-the-badge&logo=pnpm&logoColor=f69220" alt="pnpm" />
</div>

<br />

## 📖 Acerca del Proyecto

Este repositorio contiene el backend completo para un sistema basado en una **API REST**. Está diseñado con un enfoque en la seguridad y el rendimiento, utilizando **JSON Web Tokens (JWT)** para la gestión de sesiones y autorizaciones, y **Prisma ORM** para una interacción moderna y tipada con la base de datos.

---

## 🔐 Flujo de Autenticación con JWT

El sistema protege las rutas privadas mediante el siguiente flujo:
1. **Login/Registro:** El cliente envía sus credenciales (email/contraseña).
2. **Validación:** El servidor verifica los datos en la base de datos a través de Prisma.
3. **Generación del Token:** Si son válidos, el servidor firma un **JWT** (con un tiempo de expiración) y lo devuelve al cliente.
4. **Acceso Seguro:** Para futuras peticiones, el cliente envía el token en el *Header* de la petición (`Authorization: Bearer <token>`).
5. **Verificación:** Un *middleware* en Node.js intercepta la petición, verifica la firma del token y permite el acceso a la ruta protegida.

---

## 📋 Requisitos Previos

Asegúrate de tener instalado en tu entorno local:
* **[Node.js](https://nodejs.org/)** (v18 o superior recomendado).
* **[pnpm](https://pnpm.io/)** como gestor de paquetes (`npm install -g pnpm`).
* Motor de base de datos (Ej: PostgreSQL, MySQL) en ejecución.

---

## ⚙️ Instalación y Configuración

**1. Clonar el repositorio:**
```bash
git clone [https://github.com/Juanfrank2025/API-REST-con-JWT.git](https://github.com/Juanfrank2025/API-REST-con-JWT.git)
cd API-REST-con-JWT
