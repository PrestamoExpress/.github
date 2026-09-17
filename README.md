# 🏢 Bienvenidos a la Organización de Prestamo Express

¡Hola! Si estás aquí, es porque formas parte del equipo de desarrollo. Este repositorio centraliza las normativas, guías de configuración y buenas prácticas para que nuestra colaboración en GitHub sea lo más eficiente y organizada posible.

---

## 👤 1. Configuración Obligatoria del Perfil

Para mantener una comunicación fluida y saber exactamente con quién estamos colaborando en los *Pull Requests* e *Issues*, todos los miembros deben configurar su perfil de GitHub con datos profesionales:

* **Nombre para mostrar (Name):** Coloca tu **Nombre y Apellido real** (ej. *Enrique Chávez*). Evita usar solo alias o apodos.
* **Empresa (Company):** Escribe `Prestamo Express`.
* **Correo Electrónico:** Añade y verifica tu correo corporativo en tu configuración de GitHub (`Settings > Emails`). Puedes mantenerlo como privado si lo deseas, pero asegúrate de que esté vinculado a tu cuenta.

> 🔗 Puedes actualizar estos datos directamente en tu [Configuración de Perfil de GitHub](https://github.com).

---

## 👥 2. Estructura de Equipos

El acceso a los proyectos se gestiona a través de los **GitHub Teams**. Al ingresar, se te asignará a uno o varios de los siguientes equipos:

* **`@organizacion/backend`** - Desarrollo de APIs, servicios y base de datos.
* **`@organizacion/frontend`** - Desarrollo de interfaces web y aplicaciones móviles.
* **`@organizacion/design`** - Equipo de diseño UI/UX y maquetación.
* **`@organizacion/qa`** - Pruebas, automatización y control de calidad.

*Si notas que te falta acceso a algún repositorio del equipo, contacta a un Administrador.*

---

## 🚀 3. Flujo de Trabajo (Git Workflow)

Para mantener el código limpio y los repositorios ordenados, seguimos estas reglas:

### 🌿 Ramas (Branches)
* **`main` / `master`:** Código en producción. Nadie puede hacer `push` directo aquí.
* **`develop`:** Rama de integración. Aquí se unen las nuevas funciones.
* **Funcionalidades:** Crea una rama desde `develop` usando la nomenclatura: `feature/nombre-de-la-mejora` o `bugfix/nombre-del-error`.

### 🔄 Pull Requests (PR)
1. **Asignados:** Asegúrate de asignarte el PR a ti mismo y etiquetar al equipo correspondiente para la revisión.
2. **Revisiones:** Todo PR requiere la aprobación de al menos **1 miembro** del equipo antes de fusionarse (*merge*).
3. **Mensajes de Commit:** Usa mensajes claros y descriptivos en presente (ej. `Fix: corrige error de inicio de sesión en móviles`).

---

## 💻 4. Comandos de Git Recomendados

Esta es la guía rápida de comandos que utilizamos en el día a día para mantener nuestro flujo de trabajo ordenado y evitar conflictos de código.

### 🌿 Comenzar a trabajar en una nueva tarea
Antes de crear una rama, asegúrate siempre de tener la última versión del código de integración:
```bash
# 1. Cambiar a la rama de desarrollo
git checkout develop

# 2. Descargar los últimos cambios del servidor
git pull origin develop

# 3. Crear y cambiar a tu nueva rama de trabajo
git checkout -b feature/nombre-de-tu-tarea
```

### 💾 Guardar y subir tus cambios
Haz commits pequeños y descriptivos mientras avanzas en tu tarea:
```bash
# 1. Ver qué archivos has modificado
git status

# 2. Agregar los cambios al área de preparación (staging)
git add .

# 3. Guardar tus cambios con un mensaje claro
git commit -m "Feat: agrega validación al formulario de registro"

# 4. Subir tu rama a GitHub por primera vez
git push -u origin feature/nombre-de-tu-tarea
```

### 🔄 Mantener tu rama actualizada
Si tus compañeros subieron cambios a `develop` mientras tú trabajabas, actualiza tu rama para evitar conflictos antes de abrir un Pull Request:
```bash
# 1. Traer los cambios de develop a tu rama actual
git merge develop
```
*Si aparecen conflictos en los archivos, resuélvelos en tu editor de código (como VS Code), haz un nuevo `git commit` y luego un `git push`.*

### 🧹 Limpieza local (Opcional)
Para borrar ramas antiguas en tu computadora una vez que tu Pull Request fue aprobado y fusionado en GitHub:
```bash
# 1. Volver a develop
git checkout develop

# 2. Borrar la rama localmente
git branch -d feature/nombre-de-tu-tarea

# 3. Limpiar referencias de ramas que ya se borraron en GitHub
git fetch --prune
```
***

---

## 🛠️ 5. Contacto y Soporte

Si tienes dudas sobre los accesos, la estructura de los repositorios o necesitas soporte técnico interno:

* **Administradores de GitHub:** `@EnriqueChavez`, `@AngelGaytan`
* **Canal de Comunicación Principal:** [Teams / WhatsApp]
* **Correo de Soporte:** `sistemas.desarrollo@prestamoexpress.com`

---

*Este documento es dinámico. Si encuentras algo que se pueda mejorar en nuestro flujo de trabajo, propón un cambio mediante un Pull Request.*
