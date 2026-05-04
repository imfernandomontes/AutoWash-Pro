# AutoWash Pro 🚗
Sistema de gestión para lavado de autos con Supabase + Vercel.

---

## Paso 1 — Crear proyecto en Supabase

1. Ve a **https://supabase.com** y crea una cuenta gratuita
2. Clic en **"New project"**
3. Ponle nombre: `autowash-pro`
4. Elige una contraseña segura para la base de datos
5. Selecciona la región más cercana (ej: **us-east-1**)
6. Espera ~2 minutos a que el proyecto se cree

---

## Paso 2 — Crear las tablas (schema)

1. En tu proyecto de Supabase, ve al menú izquierdo → **SQL Editor**
2. Clic en **"New query"**
3. Copia todo el contenido del archivo `schema.sql`
4. Pégalo en el editor y clic en **"Run"** (botón verde)
5. Deberías ver: `Success. No rows returned`

Esto crea todas las tablas y carga datos de ejemplo automáticamente.

---

## Paso 3 — Obtener tus credenciales

1. En Supabase, ve a **Project Settings** (ícono de engranaje, abajo a la izquierda)
2. Clic en **"API"**
3. Copia estos dos valores:
   - **Project URL** → algo como `https://xyzabc.supabase.co`
   - **anon / public key** → texto largo que empieza con `eyJ...`

---

## Paso 4 — Conectar la app

1. Abre el archivo `index.html` en tu navegador (doble clic)
2. Pega tu **Project URL** y tu **anon key** en el formulario
3. Clic en **"Conectar y guardar"**
4. ¡Listo! El sistema arranca con los datos de ejemplo

> Tus credenciales quedan guardadas en el navegador. La próxima vez que abras el archivo, entra directo sin pedirte nada.

---

## Paso 5 — Publicar en internet gratis (Vercel)

Para acceder desde tu celular, tablet o cualquier computadora:

1. Ve a **https://vercel.com** y crea cuenta gratuita (puedes entrar con Google)
2. Clic en **"Add New Project"**
3. Selecciona **"Deploy from file"** o arrastra tu carpeta
4. Sube únicamente el archivo `index.html`
5. Clic en **Deploy**
6. En ~30 segundos tendrás una URL como:
   `https://autowash-pro.vercel.app`

> Esa URL funciona en cualquier dispositivo, 24/7, sin costo.

---

## Estructura de archivos

```
autowash-pro/
├── index.html    ← La app completa (sube este a Vercel)
├── schema.sql    ← Ejecutar UNA sola vez en Supabase
└── README.md     ← Este archivo
```

---

## Módulos del sistema

| Módulo | Descripción |
|---|---|
| Dashboard | Métricas del día, gráfica semanal, citas y últimas ventas |
| Ventas | Registro de servicios, cobro pendiente, historial |
| Agenda | Vista semanal, citas por presencial / WhatsApp / llamada |
| Empleados | Equipo activo, rendimiento del mes |
| Bonos | Progreso hacia metas, cálculo automático de bonos |
| Promociones | Descuentos activos, impacto en ventas |
| Clientes | Base de clientes, historial, referidos |

---

## Costos

| Servicio | Plan | Costo |
|---|---|---|
| Supabase | Free tier (500MB, ilimitadas peticiones) | **$0/mes** |
| Vercel | Hobby (ilimitados deploys, HTTPS incluido) | **$0/mes** |
| Dominio propio (opcional) | .com en Namecheap | ~**$12/año** |

---

## Preguntas frecuentes

**¿Puedo usar el sistema desde mi celular?**
Sí. Una vez en Vercel, la URL funciona en cualquier dispositivo.

**¿Puedo tener varios empleados usando el sistema al mismo tiempo?**
Sí. Supabase es una base de datos en tiempo real, todos ven los mismos datos.

**¿Qué pasa si se va la luz o cierro el navegador?**
Nada. Todos los datos están en Supabase, no en el dispositivo.

**¿Cómo hago backup de mis datos?**
En Supabase → Table Editor → cualquier tabla → Export CSV.

---

## Próximos pasos sugeridos

- [ ] Agregar autenticación por usuario (login con email)
- [ ] Notificaciones WhatsApp automáticas al confirmar cita
- [ ] Reporte mensual exportable a PDF
- [ ] App móvil nativa (PWA)
