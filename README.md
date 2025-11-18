# Los Gitadores
Portafolio colaborativo del equipo Los Gitadores.

## Miembros del equipo

- **Pablo** – Jefe del equipo – @Pablosky2806
- **Erik** – Frontend Developer – @Hawaiiiiii
- **Marcos** – Diseñador UI
- **Iván** – Responsable de Proyectos

## Estructura del proyecto

- `index.html` → Página principal del portafolio
- `proyectos.html` → Listado de proyectos
- `styles.css` → Estilos del sitio
- `config.js` → Configuración y datos del equipo
- `CHANGELOG.md` → Registro de cambios del proyecto
- `docs/` → Documentación adicional del proyecto

## Metodología Gitflow

Este proyecto utiliza una metodología Gitflow optimizada para desarrollo colaborativo eficiente.

### Estructura de Ramas

**Ramas Principales (Larga Duración):**
- `main`: Código listo para producción, historial de lanzamientos oficiales
- `develop`: Rama de integración para nuevas funcionalidades

**Ramas de Soporte (Temporales):**
- `feature/*`: Desarrollo de nuevas funcionalidades
- `release/*`: Preparación de lanzamientos y correcciones finales
- `hotfix/*`: Correcciones urgentes en producción

### Flujo de trabajo recomendado

1. **Configuración inicial:**
   ```bash
   git clone https://github.com/Pablosky2806/los-gitadores.git
   cd los-gitadores
   git checkout develop
   ```

2. **Desarrollo de nuevas funcionalidades:**
   ```bash
   git checkout develop
   git checkout -b feature/nueva-funcionalidad
   # Trabajar y hacer commits
   git push origin feature/nueva-funcionalidad
   # Crear Pull Request hacia develop
   ```

3. **Preparación de release:**
   ```bash
   git checkout develop
   git checkout -b release/1.0.0
   # Correcciones finales y testing
   git checkout main
   git merge release/1.0.0
   git tag -a v1.0.0 -m "Version 1.0.0"
   ```

4. **Hotfix urgente:**
   ```bash
   git checkout main
   git checkout -b hotfix/1.0.1
   # Corrección crítica
   git checkout main
   git merge hotfix/1.0.1
   git checkout develop
   git merge hotfix/1.0.1
   ```

### Buenas prácticas

- **Commits descriptivos**: Usar conventional commits (feat:, fix:, docs:, etc.)
- **Pull Requests**: Todos los cambios deben pasar por code review
- **Ramas cortas**: Mantener features y releases de duración corta
- **Testing**: Validar cambios antes de merge
- **Comunicación**: Notificar cambios mayores al equipo

### Documentación disponible

- `docs/release-branches-guide.md` → Guía completa para ramas release/*
- `docs/hotfix-branches-guide.md` → Guía completa para ramas hotfix/*
- `docs/project-completion-plan.md` → Plan de finalización del proyecto
- `docs/guia-metodologia-agil-2025.md` → Guía de metodología ágil actualizada

### Control de calidad

- Mínimo 2 aprobaciones en Pull Requests
- Tests antes de merge a develop
- Validación en rama release antes de producción
- Documentación actualizada en cada release

## Estructura de directorios

```
los-gitadores/
├── index.html              # Página principal
├── proyectos.html          # Página de proyectos
├── styles.css             # Estilos principales
├── config.js              # Configuración JavaScript
├── CHANGELOG.md           # Historial de cambios
└── docs/                  # Documentación
    ├── release-branches-guide.md
    ├── hotfix-branches-guide.md
    ├── project-completion-plan.md
    └── guia-metodologia-agil-2025.md
```

## Próximos pasos

- Completar tarjetas de todos los miembros del equipo
- Implementar funcionalidades pendientes
- Optimizar diseño y experiencia de usuario
- Documentar procesos y mejores prácticas

## Contribuir

1. Fork el repositorio
2. Crear rama feature desde develop
3. Realizar cambios y commits descriptivos
4. Crear Pull Request hacia develop
5. Esperar aprobación y merge

Para hotfixes urgentes, crear rama hotfix desde main siguiendo las guías en `docs/hotfix-branches-guide.md`.

---

*Metodología Gitflow optimizada implementada como testing de automatización*