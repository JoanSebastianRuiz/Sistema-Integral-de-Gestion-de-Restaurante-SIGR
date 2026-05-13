# 🍽️ SIGR — Sistema Integral de Gestión de Restaurante

Sistema web para automatizar y optimizar los procesos operativos de un restaurante: pedidos en tiempo real, reservas, menú digital, control de usuarios y reportes de ventas.

---

## 📋 Descripción

SIGR centraliza la gestión de un restaurante en una sola plataforma, reduciendo errores manuales y mejorando la coordinación entre áreas. Incluye control de acceso por roles (administrador, mesero, cliente), seguimiento de pedidos, administración del menú y cierre de caja diario.

---

## 🚀 Módulos Principales

| Módulo | Descripción |
|---|---|
| **Autenticación** | Inicio de sesión y control de acceso por roles |
| **Menú Digital** | CRUD de platos y categorías |
| **Pedidos** | Registro y seguimiento en tiempo real |
| **Reservas** | Gestión de reservas por fecha y hora |
| **Reportes** | Cierre de caja y ventas diarias |

---

## 🛠️ Tecnologías

**Frontend**
- React + Vite
- React Router
- Context API

**Backend**
- Node.js + Express
- Arquitectura modular (controller / service / routes / model)
- JWT para autenticación

---

## 📁 Estructura del Proyecto

```
sigr/
├── frontend/
│   ├── public/
│   └── src/
│       ├── components/    # Componentes reutilizables (common, layout, ui)
│       ├── pages/         # Vistas por módulo (auth, menu, orders, reservations, reports)
│       ├── services/      # Llamadas a la API
│       ├── context/       # Estado global (AuthContext, AppContext)
│       ├── hooks/         # Hooks personalizados
│       ├── routes/        # Configuración de rutas
│       └── utils/         # Funciones auxiliares y constantes
│
└── backend/
    └── src/
        ├── config/        # Conexión a BD y variables de entorno
        ├── modules/       # Módulos funcionales (auth, users, menu, orders, reservations, reports)
        ├── middlewares/   # Autenticación, errores, logger
        └── utils/         # Helpers reutilizables
```

---

## ⚙️ Instalación y Ejecución

### Requisitos Previos

- Node.js v18+
- npm v9+
- Base de datos (ver configuración en `.env`)

### 1. Clonar el repositorio

```bash
git clone https://github.com/<usuario>/sigr.git
cd sigr
```

### 2. Configurar variables de entorno

Copia los archivos de ejemplo y completa los valores:

```bash
# Backend
cp backend/.env.example backend/.env

# Frontend
cp frontend/.env.example frontend/.env
```

### 3. Instalar dependencias

```bash
# Backend
cd backend
npm install

# Frontend
cd ../frontend
npm install
```

### 4. Ejecutar en desarrollo

```bash
# Backend (desde /backend)
npm run dev

# Frontend (desde /frontend)
npm run dev
```

El frontend estará disponible en `http://localhost:5173` y el backend en `http://localhost:3000`.

---

## 🔐 Roles de Usuario

| Rol | Permisos |
|---|---|
| **Administrador** | Acceso completo al sistema |
| **Mesero** | Registro de pedidos, consulta de mesas y órdenes activas |
| **Cliente** | Consulta del menú y gestión de reservas |

---

## 📐 Convenciones de Código

- **Variables y funciones:** `camelCase`
- **Componentes React:** `PascalCase`
- **Archivos backend:** `modulo.responsabilidad.js` (ej. `user.controller.js`)
- **Rutas API:** REST estándar, nombres en plural y en inglés (`GET /api/orders`)
- **Commits:** Conventional Commits (`feat:`, `fix:`, `docs:`, `refactor:`, `style:`)

---

## 🗂️ Control de Versiones

- **Herramienta:** Git
- **Plataforma:** GitHub
- **Rama principal:** `main`
- **Línea base v1.0.0:** commit `a93b4f1`

---

## 📄 Licencia

Este proyecto está bajo la licencia **MIT**. Consulta el archivo [LICENSE.txt](./LICENSE.txt) para más detalles.

---

## 👤 Autor

**Joan Sebastian Ruiz Angarita**
