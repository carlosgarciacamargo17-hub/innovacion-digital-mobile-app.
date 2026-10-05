# 🚀 Entorno de Colaboración Empresarial – Desarrollo de App Móvil

Proyecto que define e implementa el entorno de trabajo colaborativo de una pequeña empresa tecnológica que desarrolla una **aplicación móvil**, con un equipo híbrido (presencial + remoto) formado por **programadores, diseñadores, analistas y marketing**.

## 🎯 Problema
Los integrantes necesitan **coordinar actividades** y **mantener actualizada la información del proyecto**.

## ✅ Solución (Tareas 31–35)

| # | Tarea | Documento | Estado |
|---|-------|-----------|--------|
| 31 | Formar el Departamento de TI y asignar cargos | [docs/01-departamento-ti.md](docs/01-departamento-ti.md) | ✅ Completada |
| 32 | Definir las etapas del proyecto | [docs/02-etapas-proyecto.md](docs/02-etapas-proyecto.md) | ✅ Completada |
| 33 | Crear un espacio colaborativo | [docs/03-espacio-colaborativo.md](docs/03-espacio-colaborativo.md) | ✅ Completada |
| 34 | Organizar tareas mediante un tablero | [docs/04-tablero-tareas.md](docs/04-tablero-tareas.md) | ✅ Completada |
| 35 | Reuniones virtuales, repositorio de documentos y seguridad | [docs/05-reuniones-virtuales.md](docs/05-reuniones-virtuales.md), [docs/06-repositorio-documentos.md](docs/06-repositorio-documentos.md), [docs/07-seguridad.md](docs/07-seguridad.md) | ✅ Completada |

## 🗂️ Estructura del repositorio
```
.
├── README.md
├── CONTRIBUTING.md · SECURITY.md · CODE_OF_CONDUCT.md · LICENSE
├── docs/                 # Documentación de las tareas 31-35 + conclusiones
├── templates/            # Plantillas: acta, informe semanal, retrospectiva
├── scripts/              # Automatización con GitHub CLI (etiquetas, issues)
└── .github/
    ├── ISSUE_TEMPLATE/   # Plantillas de tarea, bug y reunión
    ├── workflows/        # CI: validación de Markdown y enlaces
    ├── CODEOWNERS
    └── PULL_REQUEST_TEMPLATE.md
```

## ⚙️ Puesta en marcha (5 minutos)
```bash
# 1. Subir el repositorio
git remote add origin https://github.com/<tu-usuario>/entorno-colaboracion.git
git push -u origin main

# 2. Crear etiquetas y tareas iniciales (requiere GitHub CLI: gh auth login)
bash scripts/setup-labels.sh
bash scripts/crear-issues-iniciales.sh

# 3. Crear el tablero: GitHub → Projects → New project → Board
#    (columnas y reglas en docs/04-tablero-tareas.md)
```

## 🧰 Stack de herramientas
GitHub (código, issues, Projects, Wiki, Discussions) · Slack/Discord (chat) · Google Meet/Zoom (reuniones) · Figma (diseño) · Google Drive/Notion (documentos) · Bitwarden (contraseñas).

## 📈 Resultados esperados
- Visibilidad única del estado del proyecto (tablero + issues).
- Reducción de reuniones largas gracias a la comunicación asíncrona.
- Información centralizada, versionada y con control de acceso.
- Cumplimiento de medidas mínimas de seguridad (MFA, roles, copias, cifrado).

## 📄 Licencia
MIT – ver [LICENSE](LICENSE).
