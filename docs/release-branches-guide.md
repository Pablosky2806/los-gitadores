# Documentación de Ramas de Release

*Testing de automatización - Metodología Gitflow optimizada*

## Propósito de las Ramas release/*

Las ramas de release/* sirven para preparar lanzamientos de versión. Son ramas temporales que se desprenden de develop y se utilizan para:

1. **Preparación final del lanzamiento**: Últimas correcciones y ajustes
2. **Testing y QA**: Pruebas finales antes de producción
3. **Actualización de versión**: Cambios en números de versión
4. **Documentación final**: Preparación de notas de release

## Cómo Crear una Rama release

```bash
# Desde develop
git checkout develop
git pull origin develop
git checkout -b release/1.0.0
```

## Contenido Típico en rama release

- Correcciones menores de bugs
- Actualizaciones de documentación
- Cambios en números de versión
- Notas de release
- Pruebas finales de regresión

## Finalización de rama release

```bash
# Merge a main y develop
git checkout main
git merge release/1.0.0
git tag -a v1.0.0 -m "Version 1.0.0 released"
git push origin main --tags
git checkout develop
git merge release/1.0.0
git branch -d release/1.0.0
```

## Buenas Prácticas

1. **Duración máxima**: 1-2 semanas máximo
2. **Sin nuevas características**: Solo correcciones menores
3. **Testing exhaustivo**: Pruebas completas antes del merge
4. **Documentación**: Actualizar CHANGELOG y README

---

*Creado como parte del testing de metodología Gitflow optimizada*