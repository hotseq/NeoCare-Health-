# NeoCare-Health- Es una paltaforma de soluciones de tecnologia sanitaria.
Proyecto Full Stack desarrollado con React + TypeScript, FastAPI y PostrgeSQL con objetivo de crear una web real, moderna y accesible.

Aplicación orientada a:
- Gestionar tareas en un tablero Kanban
- Resgistrar las horas trabajadas
- Mover tarjetas entre estados de trabajo
- Generar informes semanales
- Mejorar la coordinación y la visibilidad del progreso
- Depender menos de hojas Excel y correos dispersos

---

## 1. Tecnologias utilizadas 
- **Frontend:** React + TypeScript + Vite
- **Backend:** FastAPI (Python)
- **Base de datos:** PostgreSQL
- **Autenticación:** JWT  
- **ORM :** SQLAlchemy
- **Deploy futuro:**
  - Backend en Render
  - Frontend en Vercel

---

## 2.Arquitecura general del proyecto
Se compone de tres partes:

### Frontend (React)
- Pantalla de login
- Redirecciion al tablero
- Pantalla del tablero vacía
- Comunicación mediante peticiones HTTP al backend

### Backend (FastAPI)
- Endpoints `/auth/register` y `/auth/login`
- Generación y validación de tokens JWT
- Conexión a PostgreSQL mediante SQLAlchemy
- Creación automática del primer tablero con sus tres columnas por defecto

### Base de datos (PosrgreSQL)
Tablas iniciales:
-**users**
-**boards**
-**lists**

---
## 3.Variables de entorno

###Frontend 

###Backend 

## 3.1.Como ejecutar el frontend 
  - **Requisitos:**
    - Tener Node.js instalado
  - **1.Descargar el ZIP del proyecto y descomprimirlo**
  - **2.Abrir carpeta en VS Code**
  - **3.Instalar dependencias**
    - npm install
  -**4.Ejecutar servidor 
  - Instalar React router: npm run dev
  - **5.Abir enlace de que aparece en el terminal:**
    - http://localhost:5173/.

## 3.2.Como ejecutar el backend 

-


## 3.3.Como configurar PostgreSQL 



