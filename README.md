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
  **Aplicación**
  `DEBUG=True`

  **JWT/Verificacion**
  `SECRET_KEY=secretkeynexeusomega123`
  `ALGORITHM=HS256`
  `ACCESS_TOKEN_EXPIRE_MINUTES=30`

  **Base de datos**
  `DATABASE_URL=postgresql+psycopg2://fastapi_user:Postgres123@localhost:5432/fastapi_db`


## 3.1.Como ejecutar el frontend 
  - **Requisitos:**
    - Tener Node.js v24.11.1
      
  - **1.Descargar el ZIP del proyecto y descomprimirlo**
  - **2.Abrir carpeta en VS Code**
  - **3.Instalar dependencias**
    - npm install
  -**4.Ejecutar servidor 
  - Instalar React router: npm run dev
  - **5.Abir enlace de que aparece en el terminal:**
    - http://localhost:5173/.

## 3.2.Como ejecutar el backend 

  - **Requisitos:**
    - Tener Python v3.12.3
    - Tener acceso a la una base de datos PostgreSQL
    - Haber configurado las variables de entorno
        
  - **1.Descargar el ZIP del pryecto y descomprimirlo** 
    - cd backend-fastapi
  - **2.Crear un entorno virtual**
    - python -m venv venv
    - source venv/bin/activate
  - **3.Instalar dependencias:** 
    - pip install -r requirements.txt
  - **4.Lanzar el servidor de la FastAPI:**
    - uvicorn app.main:app --reload
    - Este quedará disponible en http://localhost:8000

## 3.3.Como configurar PostgreSQL 
El proyecto usa PostgreSQL como base de datos para almacenar usuarios, tableros y listas.
Para que funcine, es necesario crear una base de datos y configurar la variable `DATABASE_URL`

  ### 1. Instalar PostgreSQL 
    - La base de datos se instaló de forma local en el sistema Linux.
    - Se creó un usuario especifico para el backend y una base de datos 
    - La conexión se realiza mediante SQLAlchemy usando una URL de conexión definida en variables de entorno.
  ### 2. Crear la base de datos 
  -**En el terminal del sistema:**
    - `sudo apt install postgresql postgresql-contrib`
    - `sudo -u postgres psql`
  -**En Python:**
    - `CREATE DATABASE fastapi_db;´`
    - `CREATE USER fastapi_user WITH PASSWORD 'Postgres123'; (en este caso)`
    - `GRANT ALL PRIVILEGES ON DATABASE fastapi_db TO fastapi_user;`




