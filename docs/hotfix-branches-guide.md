# Documentación de Ramas Hotfix

*Testing de automatización - Metodología Gitflow optimizada*

## Propósito de las Ramas hotfix/*

Las ramas hotfix/* son para correcciones urgentes en producción. Son las únicas ramas que se pueden crear directamente desde main:

1. **Correcciones críticas**: Bugs que afectan usuarios en producción
2. **Respuesta rápida**: Soluciones inmediatas sin esperar el siguiente release
3. **Mínimo impacto**: Cambios enfocados únicamente en la corrección
4. **Validación inmediata**: Testing y deployment acelerado

## Cómo Crear una Rama hotfix

```bash
# Desde main (producción)
git checkout main
git pull origin main
git checkout -b hotfix/1.0.1
```

## Flujo de Trabajo hotfix

1. **Crear desde main**: La rama hotfix se basa en código de producción
2. **Implementar corrección**: Cambios mínimos y enfocados
3. **Testing urgente**: Validación rápida pero completa
4. **Merge urgente**: A main y develop simultáneamente

## Finalización de rama hotfix

```bash
# Merge a main
git checkout main
git merge hotfix/1.0.1
git tag -a v1.0.1 -m "Hotfix critical bug"
git push origin main --tags

# Merge a develop
git checkout develop
git merge hotfix/1.0.1

# Eliminar rama
git branch -d hotfix/1.0.1
```

## Ejemplos de hotfix válidos

- Error en formulario de contacto
- Enlace roto en footer
- Bug de visualización en móvil
- Error tipográfico en contenido
- Problema de compatibilidad urgente

## Criterios para hotfix

✅ **Crear hotfix si**:
- El error afecta usuarios reales
- Es una corrección simple y puntual
- No se puede esperar al siguiente release
- No requiere nueva funcionalidad

❌ **NO crear hotfix si**:
- Requiere nueva funcionalidad
- Es una mejora menor
- Puede esperar al siguiente release
- Es un cambio de diseño

---

*Creado como parte del testing de metodología Gitflow optimizada*