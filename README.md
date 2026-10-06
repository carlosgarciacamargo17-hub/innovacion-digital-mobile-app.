# 🚀 Innovación Digital — Entorno de Colaboración Empresarial

Proyecto del **Caso 7**: startup tecnológica que desarrolla una aplicación móvil con un equipo mixto (programadores, diseñadores, analistas y marketing) que trabaja parcialmente a distancia.

**Problema:** coordinar actividades y mantener la información del proyecto actualizada.
**Solución:** un entorno de colaboración (organización, etapas, espacio compartido, tablero, reuniones, repositorio y seguridad) + un tablero Kanban funcional incluido en este repo.

## 📂 Estructura

| Ruta | Contenido | Tarea |
|---|---|---|
| [`docs/01-departamento-ti.md`](docs/01-departamento-ti.md) | Departamento de TI, cargos y funciones | 31 |
| [`docs/02-etapas-proyecto.md`](docs/02-etapas-proyecto.md) | Etapas, entregables y cronograma | 32 |
| [`docs/03-espacio-colaborativo.md`](docs/03-espacio-colaborativo.md) | Espacio colaborativo y canales | 33 |
| [`docs/04-tablero-tareas.md`](docs/04-tablero-tareas.md) | Metodología del tablero Kanban | 34 |
| [`docs/05-reuniones-repositorio-seguridad.md`](docs/05-reuniones-repositorio-seguridad.md) | Reuniones, repositorio y seguridad | 35 |
| [`app/index.html`](app/index.html) | **Tablero Kanban funcional** (abrir en el navegador) | 34 |
| `.github/` | Plantillas de issues, PR y CI | 33/35 |
| `SECURITY.md`, `CONTRIBUTING.md`, `CODEOWNERS` | Políticas de seguridad y colaboración | 35 |

## ▶️ Cómo usar el tablero
1. Descarga o clona el repositorio.
2. Abre `app/index.html` en cualquier navegador (no requiere instalación).
3. Crea tareas, arrástralas entre columnas; los datos se guardan en el navegador. Puedes exportar/importar JSON.

## 🌐 Publicar en GitHub Pages
`Settings → Pages → Branch: main → /app` (o mueve `index.html` a `/docs`).

## ⬆️ Subir a GitHub
```bash
git init && git add . && git commit -m "feat: entorno de colaboración Innovación Digital"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/innovacion-digital.git
git push -u origin main
```

## 👥 Equipo
Ver [`docs/01-departamento-ti.md`](docs/01-departamento-ti.md). Licencia: MIT.
