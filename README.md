# Entorno de colaboración empresarial en GitHub

Proyecto listo para desplegar: un entorno de colaboración para una pequeña empresa tecnológica que desarrolla una **aplicación móvil** con equipos de programación, diseño, análisis y marketing que trabajan parcialmente a distancia.

Cubre las tareas 31 a 35:

| Tarea | Qué incluye este proyecto | Dónde está |
|---|---|---|
| 31. Departamento de TI y cargos | Equipos (Teams), roles y permisos | `config/equipos.json`, `scripts/setup.sh` |
| 32. Etapas del proyecto | 6 Milestones con fechas | `config/milestones.json` |
| 33. Espacio colaborativo | 5 repositorios, Discussions, Wiki, plantillas | carpetas `organizacion/`, `app-movil/`, `backend-api/`, `diseno-ui/`, `documentacion/` |
| 34. Tablero de tareas | GitHub Project (Kanban) + etiquetas + plantillas de Issues | `config/etiquetas.json`, `scripts/crear-tablero.sh` |
| 35. Reuniones, documentos y seguridad | Calendario de reuniones, repo de documentos, 2FA, protección de ramas, Dependabot, CodeQL, secret scanning | `documentacion/`, `organizacion/.github/`, `scripts/setup.sh` |

## Estructura

```
proyecto/
├── config/                  # Datos de configuración (equipos, etiquetas, milestones)
├── scripts/                 # Automatización con GitHub CLI
├── organizacion/.github/    # Contenido del repo ".github" de la organización
├── documentacion/           # Contenido del repo "documentacion"
├── app-movil/               # Contenido inicial del repo "app-movil"
├── backend-api/             # Contenido inicial del repo "backend-api"
└── diseno-ui/               # Contenido inicial del repo "diseno-ui"
```

Cada carpeta de primer nivel con código o documentos se publica como **un repositorio** de la organización.

## Despliegue en 6 pasos

### Requisitos previos
- Cuenta de GitHub y una **Organization** creada (Settings → Organizations → New organization).
- [GitHub CLI](https://cli.github.com/) instalado (`gh --version`).
- Permisos de *Owner* en la organización.
- Plan **Team** o superior si quieres protección de ramas en repositorios privados.

### Pasos

```bash
# 1. Iniciar sesión con los permisos necesarios
gh auth login
gh auth refresh -s admin:org -s project -s repo

# 2. Ejecutar la configuración (reemplaza MI-ORG por el nombre real de tu organización)
chmod +x scripts/*.sh
./scripts/setup.sh MI-ORG

# 3. Crear el tablero Kanban
./scripts/crear-tablero.sh MI-ORG

# 4. Invitar a los miembros a sus equipos (edita primero config/miembros.csv)
./scripts/invitar-miembros.sh MI-ORG
```

### Pasos manuales (GitHub no los permite por API)
5. **Exigir 2FA:** Organization → Settings → Authentication security → *Require two-factor authentication*.
6. **Automatizaciones del tablero:** en el Project → ⋯ → Workflows, activar *Item added to project → Backlog*, *Pull request merged → Done*, *Item closed → Done*.

Detalle completo en `documentacion/manuales/guia-despliegue.md`.

## Contenido de cada repositorio

| Repositorio | Propósito | Equipos con escritura |
|---|---|---|
| `.github` | Plantillas, normas y perfil de la organización | admin-ti |
| `app-movil` | Código de la aplicación | desarrollo |
| `backend-api` | Servidor y base de datos | desarrollo |
| `diseno-ui` | Prototipos y recursos gráficos | diseno |
| `documentacion` | Requisitos, actas, manuales | analisis, direccion |

## Seguridad incluida

Autenticación en dos pasos · protección de la rama `main` · `CODEOWNERS` · secret scanning y push protection · Dependabot · CodeQL · repositorios privados · `SECURITY.md` · revisión trimestral de accesos.

---
*Reemplaza el texto `TU-ORG` en los archivos por el nombre de tu organización (el script `setup.sh` lo hace automáticamente).*
