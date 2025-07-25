# Metodología de Desarrollo para Agentes de IA en Augment Code

## 1. Protocolo de Ejecución Estricto

### 1.1. PASO 1: Análisis Inicial OBLIGATORIO

**SIEMPRE ejecutar en este orden**:

1. **Consultar `/docs/project-input/`** - Leer TODOS los archivos
2. **Detectar estado del proyecto**:
   - ¿Existe `/docs/current-sprint/`? → Proyecto en progreso
   - ¿Existe código sin metodología? → Proyecto existente
   - ¿No existe nada? → Proyecto nuevo
3. **Crear task list** inmediatamente
4. **NO proceder** hasta completar análisis

### 1.2. Estructura de Directorios ESTÁNDAR

**OBLIGATORIO en TODOS los proyectos**:
```
/docs/
  /project-input/        # Input del usuario (no tocar)
  /processed-input/      # Inputs procesados por sprint
    /sprint-01/          # Inputs procesados del sprint 1
    /sprint-02/          # Inputs procesados del sprint 2
  /sprint-01/            # Primer sprint completado
  /sprint-02/            # Segundo sprint completado
  /current-sprint/       # Sprint actual en progreso
    /planning/           # Documentos de planificación
    /stories/            # Historias hiperdetalladas
    /verification/       # Verificaciones de historias
    /implementation/     # Código y documentación técnica
  /archive/              # Sprints antiguos
/.augment/rules/         # Reglas de Augment Code
```

### 1.3. Reglas de Transición ESTRICTAS

**NUNCA avanzar a la siguiente fase sin**:
- ✅ Todos los documentos de la fase actual completos
- ✅ Documentos organizados en directorios correctos
- ✅ Task list actualizada con estados correctos
- ✅ Aprobación explícita del usuario para avanzar

### 1.4. Nomenclatura ESTÁNDAR

**Documentos (SIEMPRE usar estos nombres)**:
- `project_context.md` - Análisis y contexto del proyecto
- `planning_doc.md` - Requisitos + arquitectura + historias
- `story-[ID]-[nombre-corto].md` - Historia hiperdetallada
- `verify-[ID]-[nombre-corto].md` - Verificación de historia
- `sprint-summary.md` - Resumen del sprint completado

## 2. Flujos Adaptativos por Tipo de Proyecto

### 2.1. Flujo para Proyecto Nuevo
**Detección**: No hay documentos metodológicos previos
**Proceso**: Análisis completo → Planificación → Implementación → Despliegue

### 2.2. Flujo para Proyecto en Progreso
**Detección**: Historias hiperdetalladas pendientes
**Proceso**: Continuar con siguiente historia → Implementación → QA

### 2.3. Flujo para Nuevo Sprint
**Detección**: Todas las historias completas
**Proceso**: Análisis de cambios → Nuevas historias → Implementación

### 2.4. Flujo por Complejidad
**Simple**: Saltar documentación extensa, roles combinados, directo a implementación
**Compleja**: Proceso completo con todos los roles y documentación detallada

### 2.5. Flujo por Tipo de Trabajo
**Feature nueva**: Proceso estándar
**Refactor**: Más análisis de código existente, menos diseño
**Bugfix**: Proceso acelerado, directo a implementación

## 3. Sistema de Roles Fluidos

### 3.1. Roles Combinables
Los roles pueden combinarse naturalmente:

- **Analista de Código + Generador de Reglas**: Análisis y reglas en una sesión
- **Requisitos + Arquitectura**: Para proyectos simples
- **Desarrollador + QA**: Para cambios menores

### 3.2. Roles Core
**Analista de Código**: Análisis exhaustivo del código existente, patrones, dependencias
**Generador de Reglas**: Crear/actualizar `.augment/rules/` dinámicamente
**Planificador**: Requisitos, arquitectura, historias (roles combinados)
**Desarrollador**: Implementación basada en historias hiperdetalladas
**QA**: Validación contra criterios de aceptación

### 3.3. Artefactos Consolidados

- `project_context.md`: Overview + análisis de código combinado
- `planning_doc.md`: Requisitos + arquitectura + historias
- `implementation_guide.md`: Historias hiperdetalladas consolidadas
- `.augment/rules/`: Reglas dinámicas específicas del proyecto

## 4. Gestión Práctica del Contexto con Herramientas de Augment Code

### 4.1. Herramientas de Retrieval

**`codebase-retrieval`**: Para entender código actual, buscar patrones existentes
- Usar al inicio de cada sesión de trabajo
- Preguntar por símbolos específicos antes de editar
- Solicitar información detallada sobre clases, métodos, propiedades involucradas

**`git-commit-retrieval`**: Para ver cómo se hicieron cambios similares antes
- Buscar implementaciones similares en el historial
- Entender patrones de cambio del proyecto
- Aprender de decisiones técnicas previas

### 4.2. Herramientas de Edición

**`str-replace-editor`**: SIEMPRE hacer retrieval primero, editar conservadoramente
- Nunca editar sin entender el contexto completo
- Respetar patrones y convenciones existentes
- Hacer cambios incrementales y verificables

### 4.3. Context7 para Documentación Oficial

**SIEMPRE disponible para consultar documentación oficial**

**Uso en Fase 1 - Análisis**:
- Consultar documentación del stack tecnológico detectado
- Verificar mejores prácticas de frameworks
- Entender patrones recomendados por la documentación oficial

**Uso en Fase 2 - Planificación**:
- Consultar guías de arquitectura oficiales
- Verificar APIs y métodos disponibles
- Confirmar patrones de diseño recomendados

**Uso en Fase 3 - Resolución de Errores**:
- Consultar documentación cuando hay errores de build
- Verificar sintaxis correcta de APIs
- Buscar soluciones oficiales a problemas comunes

**Ejemplos de consultas útiles**:
- "Next.js App Router best practices"
- "Tailwind CSS responsive design patterns"
- "Convex database schema design"
- "Vercel deployment configuration"

### 4.4. Sequential Thinking para Análisis Complejo

**SIEMPRE disponible para pensamiento estructurado y resolución de problemas complejos**

**Cuándo usar Sequential Thinking**:
- **Decisiones arquitectónicas importantes** (stack, patrones, estructura)
- **Análisis de proyectos existentes complejos** (código legacy, arquitectura unclear)
- **Debugging de errores complejos** (múltiples sistemas, dependencias)
- **Planificación de features complejas** (múltiples historias interdependientes)
- **Resolución de conflictos** (requirements contradictorios, limitaciones técnicas)

**Uso en Fase 1 - Análisis Complejo**:
- Analizar arquitectura existente compleja
- Decidir stack tecnológico cuando no está claro
- Evaluar múltiples opciones de MCPs
- Planificar migración de código legacy

**Uso en Fase 2 - Planificación Arquitectónica**:
- Diseñar arquitectura para sistemas complejos
- Descomponer features complejas en historias
- Resolver dependencias entre componentes
- Evaluar trade-offs de diseño

**Uso en Fase 3 - Resolución de Problemas**:
- Debugging de errores multi-sistema
- Problemas de performance complejos
- Conflictos de integración CI/CD
- Optimización de workflows

**Proceso de Sequential Thinking**:
1. **Definir el problema** claramente
2. **Descomponer** en sub-problemas
3. **Analizar opciones** para cada sub-problema
4. **Evaluar trade-offs** y dependencias
5. **Seleccionar enfoque** óptimo
6. **Documentar razonamiento** para transparencia

### 4.5. Task Management Integrado

**Desde el inicio**: Usar task management como parte integral del proceso
- Crear tareas por cada fase metodológica
- Actualizar estados en tiempo real
- Mantener visibilidad del progreso para el usuario

### 4.4. MCPs Inteligentes por Contexto

**MCPs Core (siempre disponibles)**:
- File system, Git, Memory, Time
- **Context7**: Consulta de documentación oficial
- **Sequential Thinking**: Análisis estructurado de problemas complejos
- PDF tools, Calculator, Web scraping

**MCPs por Stack Tecnológico** (detectar y sugerir automáticamente):
- **Convex**: Buscar MCP de Convex si el proyecto lo usa
- **Supabase**: MCP de Supabase para proyectos que lo requieran
- **PostgreSQL/MySQL**: MCPs de base de datos según stack detectado
- **Redis**: Si se detecta uso de caché/estado

**MCPs de QA Obligatorios** (según complejidad):
- **GitHub Actions MCP**: Para CI/CD automático (SIEMPRE si hay repositorio GitHub)
- **Playwright**: Para pruebas E2E (SIEMPRE disponible en Augment Code)
- **Testing tools**: Según framework detectado

**Proceso de MCPs Inteligente**:
1. **Detectar stack** en `/docs/project-input/` o código existente
2. **MCPs Automáticos** (sin pedir permiso):
   - GitHub Actions (si hay repositorio)
   - Playwright (siempre disponible)
   - Context7 (siempre disponible para documentación)
   - Sequential Thinking (siempre disponible para análisis complejo)
3. **MCPs Sugeridos** (solicitar aprobación):
   - Database MCPs según stack detectado
   - Cloud MCPs según deployment target
   - Integration MCPs según APIs mencionadas
4. **Configurar automáticamente** los MCPs aprobados

### 4.6. Criterios para Usar Sequential Thinking

**Usar SIEMPRE cuando**:
- **Múltiples opciones válidas** (stack, arquitectura, patrones)
- **Dependencias complejas** entre componentes/sistemas
- **Trade-offs significativos** en decisiones técnicas
- **Errores que afectan múltiples sistemas**
- **Requirements contradictorios** o ambiguos

**NO usar para**:
- **Tareas simples y directas** (implementar historia clara)
- **Procesos ya definidos** en la metodología
- **Decisiones obvias** (usar TypeScript con Next.js)
- **Errores simples** (typos, linting)

## 5. Metodología del Proyecto: CFAD (Context-First Agentic Development)

Metodología adaptativa que integra gestión proactiva del contexto con flujos flexibles según el tipo de proyecto.

### 5.1. Fases con Criterios de Completitud ESTRICTOS

## **FASE 1: ANÁLISIS Y CONTEXTO**

### Criterios de INICIO:
- ✅ Task list creada
- ✅ `/project-input/` consultado completamente

### Tareas OBLIGATORIAS:
1. **Buscar URL de GitHub** en `/docs/project-input/` (para commits automáticos)
2. **Configurar GitHub Actions MCP** automáticamente si hay repositorio
3. **Detectar workflows existentes** en `.github/workflows/`
4. **Consultar Context7** para documentación oficial del stack detectado
5. **Usar Sequential Thinking** si el análisis es complejo (arquitectura unclear, múltiples opciones)
6. Análisis de código existente (si aplica)
7. Detección de stack tecnológico
8. Generación de reglas `.augment/rules/`
9. Configuración de MCPs contextuales

### Criterios de COMPLETITUD:
- ✅ `project_context.md` creado en `/docs/current-sprint/planning/`
- ✅ `.augment/rules/` configurado
- ✅ **GitHub Actions MCP configurado** (si hay repositorio)
- ✅ **Workflows CI/CD analizados** y documentados
- ✅ MCPs contextuales implementados
- ✅ Task list actualizada
- ✅ **COMMIT AUTOMÁTICO**: "feat: complete phase 1 - project analysis and setup"
- ✅ **CI/CD PIPELINE VERDE** ✅ (obligatorio antes de avanzar)
- ✅ **APROBACIÓN EXPLÍCITA del usuario**

### **NO PROCEDER A FASE 2 SIN COMPLETAR TODO LO ANTERIOR**

---

## **FASE 2: PLANIFICACIÓN COMPLETA**

### Criterios de INICIO:
- ✅ Fase 1 100% completa
- ✅ Aprobación explícita recibida

### Tareas OBLIGATORIAS:
1. **Consultar Context7** para guías de arquitectura y mejores prácticas
2. **Usar Sequential Thinking** para decisiones arquitectónicas complejas
3. Definir requisitos funcionales y no funcionales
4. Diseñar arquitectura técnica
5. **Verificar APIs y patrones** con documentación oficial via Context7
6. **Aplicar Sequential Thinking** para descomponer features complejas en historias
7. Crear TODAS las historias hiperdetalladas
8. Configurar herramientas de QA
9. Organizar archivos en estructura estándar

### Criterios de COMPLETITUD:
- ✅ `planning_doc.md` completo en `/docs/current-sprint/planning/`
- ✅ TODAS las historias en `/docs/current-sprint/stories/`
- ✅ **Workflows CI/CD configurados** según stack tecnológico
- ✅ **Integración Vercel-GitHub** verificada
- ✅ Herramientas QA configuradas (Playwright + GitHub Actions)
- ✅ Estructura de directorios organizada
- ✅ **MOVER INPUTS**: `/docs/project-input/` → `/docs/processed-input/sprint-[X]/`
- ✅ **COMMIT AUTOMÁTICO**: "feat: complete phase 2 - planning and stories for sprint [X]"
- ✅ **CI/CD PIPELINE VERDE** ✅ (obligatorio antes de avanzar)
- ✅ **APROBACIÓN EXPLÍCITA del usuario**

### **NO PROCEDER A FASE 3 SIN COMPLETAR TODO LO ANTERIOR**

---

## **FASE 3: IMPLEMENTACIÓN ITERATIVA**

### Criterios de INICIO:
- ✅ Fase 2 100% completa
- ✅ Todas las historias hiperdetalladas creadas
- ✅ Aprobación explícita recibida

### Protocolo de Desarrollo por Complejidad:

**PROYECTOS SIMPLES** (1-5 historias):
- Desarrollar 2-3 historias en paralelo
- QA integrado por lote
- Branch único: `main` o `develop`

**PROYECTOS COMPLEJOS** (6+ historias):
- Desarrollar 1 historia a la vez
- QA individual por historia
- Branch por sprint: `sprint-2`, `sprint-3`, etc.

### Ciclo OBLIGATORIO por Historia:
1. **Desarrollador**: Implementar historia
2. **QA**: Verificar criterios de aceptación
3. **Crear**: `verify-[ID]-[nombre].md`
4. **Actualizar**: Task list con estado COMPLETE
5. **Solo entonces**: Proceder a siguiente historia

### Criterios de COMPLETITUD del Sprint:
- ✅ TODAS las historias implementadas
- ✅ TODAS las verificaciones creadas
- ✅ **Tests pasando** (unitarios + integración + **E2E con Playwright**)
- ✅ **CI/CD pipeline verde** en GitHub Actions ✅
- ✅ **Vercel deployment exitoso** (preview y/o producción)
- ✅ **Smoke tests post-deployment** pasando
- ✅ Documentación técnica actualizada
- ✅ **COMMIT POR HISTORIA**: "feat: implement story [ID] - [nombre]"
- ✅ **COMMIT FINAL**: "feat: complete sprint [X] - all stories implemented"
- ✅ **PIPELINE FINAL VERDE** ✅ (obligatorio antes de finalizar)
- ✅ **APROBACIÓN EXPLÍCITA del usuario**

### Gestión de Branches:
**Sprint 1**: Trabajar en `main` o `develop`
**Sprint 2+**:
1. Crear branch `sprint-[número]`
2. Desarrollar en el branch
3. PR al finalizar sprint
4. Merge solo con aprobación

### **NO PROCEDER A SIGUIENTE SPRINT SIN COMPLETAR TODO LO ANTERIOR**

---

## **PROTOCOLO DE MINI-ITERACIONES DENTRO DE FASES**

### Mini-Iteraciones en Fase 1:
**Si el usuario NO aprueba `project_context.md` o reglas**:
1. **Solicitar feedback específico** del usuario
2. **Ajustar documentos** según feedback
3. **Actualizar** `project_context.md` y/o `.augment/rules/`
4. **Volver a solicitar aprobación**
5. **Repetir hasta obtener aprobación**

### Mini-Iteraciones en Fase 2:
**Si el usuario NO aprueba `planning_doc.md` o historias**:
1. **Solicitar feedback específico** del usuario
2. **Ajustar planificación** según feedback
3. **Modificar historias** si es necesario
4. **Actualizar documentos** en `/docs/current-sprint/`
5. **Volver a solicitar aprobación**
6. **Repetir hasta obtener aprobación**

### Reglas de Mini-Iteraciones:
- ✅ **Máximo 3 iteraciones** por fase (evitar loops infinitos)
- ✅ **Feedback específico**: Usuario debe indicar qué cambiar
- ✅ **Documentar cambios**: Registrar modificaciones en task list
- ✅ **Mantener estructura**: No cambiar organización de archivos

---

## **PROTOCOLO DE TRANSICIÓN ENTRE SPRINTS**

### Al Finalizar un Sprint:
1. **Mover** `/docs/current-sprint/` → `/docs/sprint-[número]/`
2. **Crear** `sprint-summary.md` con resumen de logros
3. **Crear** nuevo `/docs/current-sprint/` para siguiente sprint
4. **Actualizar** task list con nuevo sprint
5. **Crear branch** `sprint-[número]` si es proyecto complejo
6. **COMMIT FINAL**: "feat: finalize sprint [X] - ready for next sprint"
7. **Solicitar aprobación** para iniciar siguiente sprint

### Al Iniciar Nuevo Sprint:
1. **Consultar** `/docs/project-input/` por nuevos requisitos
2. **Ejecutar Fase 1** (análisis de cambios)
3. **En Fase 2**: Mover inputs procesados a `/docs/processed-input/sprint-[X]/`
4. **Ejecutar Fase 2** (planificación del nuevo sprint)
5. **Seguir protocolo estricto** como sprint inicial

### Gestión de Inputs Procesados:
**IMPORTANTE**: Al finalizar Fase 1 de cualquier sprint:
- **Mover** todo el contenido de `/docs/project-input/`
- **Destino**: `/docs/processed-input/sprint-[número]/`
- **Resultado**: `/docs/project-input/` queda limpio para futuros inputs
- **Beneficio**: Evita confusión en futuros sprints con nuevos agentes

### Casos Especiales:
**Bugfix urgente**: Crear branch `hotfix-[descripción]`, seguir Fase 3 simplificada
**Refactor**: Seguir Fase 1 y 3, saltar Fase 2 si no hay nuevas features
**Feature menor**: Evaluar si requiere sprint completo o puede agregarse al actual

---

## 6. Gestión de Historias Hiperdetalladas

### 6.1. Estructura de Archivos
**Una historia = Un archivo**: `/stories/story-[ID]-[nombre].md`
**Una verificación = Un archivo**: `/verification/verify-[ID]-[nombre].md`

### 6.2. Plantilla de Historia Hiperdetallada

```markdown
### Historia: [Título]

**ID:** STORY-[número]
**Estado:** [PENDING/IN_PROGRESS/COMPLETED]

**Descripción:** [Qué se debe construir - conciso pero completo]

**Criterios de Aceptación:**
- [Criterio 1: "El usuario DEBE poder [acción] para [beneficio]"]
- [Criterio 2...]

**Contexto Técnico:**
- **Archivos:** `[rutas específicas a crear/modificar]`
- **Dependencias:** [Componentes, hooks, servicios a usar]
- **Patrones:** [Patrones de diseño específicos]

**API (si aplica):**
- **Endpoint:** `[método] [ruta]`
- **Request/Response:** [Estructura de datos]

**Entregable:** Código + pruebas + documentación JSDoc
```

### 6.3. Plantilla de Verificación (Simplificada)

```markdown
### Verificación: [Título de Historia]

**ID:** STORY-[número]
**Fecha:** [YYYY-MM-DD]
**Estado:** [COMPLETED/FAILED]

**Resumen de Implementación:**
[2-3 líneas describiendo qué se logró implementar]

**Archivos Modificados:**
- `[lista de archivos realmente modificados]`

**Pruebas Ejecutadas:**
- [✓/✗] Pruebas unitarias
- [✓/✗] Pruebas de integración
- [✓/✗] Criterios de aceptación

**Notas:** [Cualquier observación importante]
```

## 7. Selección Inteligente de Stack Tecnológico

### 7.1. Proceso de Selección
1. **Revisar `/project-input/`**: Buscar stack especificado por el usuario
2. **Si no está especificado**: Analizar requisitos y sugerir stack óptimo
3. **Considerar factores**:
   - Tipo de aplicación (web, mobile, desktop)
   - Complejidad del proyecto
   - Requisitos de performance
   - Experiencia del equipo
   - Tiempo de desarrollo

### 7.2. Sugerencias Contextuales
**Web App Compleja**: Next.js + TypeScript + Tailwind + Shadcn + Convex
**Web App Simple**: Vite + React + TypeScript + Tailwind
**Mobile App**: React Native + Expo o Flutter (según contexto)
**Desktop App**: Electron + React o Tauri + React
**API/Backend**: Node.js + Express o Python + FastAPI

### 7.3. Validación con Usuario
- Presentar stack sugerido con justificación
- Solicitar aprobación o modificaciones
- Documentar decisiones en `project_context.md`

## 8. Task Management Integrado

### 8.1. Uso desde el Inicio
- **Primera acción**: Crear task list después de consultar `/project-input/`
- **Estructura por fases**: Tareas específicas para cada fase metodológica
- **Estados en tiempo real**: NOT_STARTED → IN_PROGRESS → COMPLETE
- **Visibilidad continua**: Usuario ve progreso en todo momento

### 8.2. Estructura de Tareas Sugerida
**Fase 1**: Análisis de contexto y generación de reglas
**Fase 2**: Planificación integrada (requisitos + arquitectura + historias)
**Fase 3**: Implementación (una tarea por historia hiperdetallada)

### 8.3. Coordinación con Roles

- Cada rol actualiza sus tareas correspondientes
- Transiciones fluidas entre tareas
- Feedback contextual integrado en las tareas

## 9. QA Automatizado Integrado

### 9.1. Herramientas de QA por Complejidad

**Proyectos Simples**:
- Testing unitario básico
- Linting automático

**Proyectos Complejos**:
- **Circle CI / GitHub Actions**: Validación automática en cada commit
- **Playwright**: Pruebas E2E para flujos críticos
- **Testing de integración**: APIs y componentes
- **Análisis de código**: SonarQube o similar

### 9.2. Integración en el Flujo

**Durante Desarrollo**:
- Tests unitarios en cada historia
- Linting automático en cada save

**Pre-Despliegue**:
- CI/CD pipeline automático
- Pruebas E2E en staging
- Validación de performance

**Post-Despliegue**:
- Monitoreo de errores
- Métricas de performance
- Alertas automáticas

### 9.3. Integración de Playwright (OBLIGATORIO)

**Playwright está disponible globalmente en Augment Code**

**Cuándo usar Playwright**:
- **Proyectos web** con interfaz de usuario
- **Flujos críticos** que requieren validación E2E
- **Formularios complejos** o interacciones multi-paso

**Integración en el Workflow**:

**Fase 2 - Planificación**:
- Identificar **flujos críticos** para pruebas E2E
- Documentar **escenarios de Playwright** en `planning_doc.md`
- Crear **esqueletos de tests E2E** por historia

**Fase 3 - Implementación**:
- **Por cada historia**: Implementar tests E2E correspondientes
- **Ejecutar Playwright** antes de marcar historia como completa
- **Incluir en verificación**: Tests E2E pasando

**Estructura de Tests E2E**:
```
/tests/
  /e2e/
    /[feature-name]/
      - [story-id]-[test-name].spec.ts
```

### 9.4. GitHub Actions Integration (OBLIGATORIO si hay repositorio GitHub)

**Configuración Automática del MCP GitHub**:
- **Detectar repositorio GitHub** en inputs del usuario
- **Configurar GitHub Actions MCP** automáticamente
- **Analizar workflows existentes** en `.github/workflows/`
- **Documentar CI/CD actual** en `project_context.md`

**Estrategia de CI/CD Inteligente**:

**Fase 1 - Detección y Análisis**:
- Detectar workflows existentes
- Analizar configuración actual de CI/CD
- Identificar conexión con Vercel
- Documentar estado en `project_context.md`

**Fase 2 - Configuración y Optimización**:
- Crear/actualizar workflows según stack tecnológico detectado
- Configurar workflow para: testing, linting, Playwright E2E
- Integrar con Vercel para preview deployments
- Definir estrategia CI/CD en `planning_doc.md`

**Fase 3 - Monitoreo Continuo y Bloqueo Inteligente**:
- **Ejecutar workflows** automáticamente después de cada commit
- **Bloquear progreso** si workflow falla
- **3 intentos automáticos** de re-ejecución para problemas temporales
- **Análisis de logs** y sugerencias de fix automáticas
- **Solo avanzar** cuando CI/CD esté verde ✅

**Tipos de Errores y Acciones Automáticas**:
- **Linting/Format**: Auto-fix y nuevo commit
- **Tests unitarios**: Reportar errores específicos y bloquear
- **Build errors**: Analizar logs + **consultar Context7** para soluciones oficiales
- **API errors**: **Consultar Context7** para verificar sintaxis correcta
- **Errores complejos**: **Usar Sequential Thinking** para debugging estructurado
- **Problemas multi-sistema**: **Sequential Thinking** para analizar dependencias
- **Playwright E2E**: Ejecutar contra Vercel preview URL
- **Deployment**: Verificar configuración + **consultar Context7** para Vercel docs

**Integración Dual con Playwright**:
- **Local**: Playwright durante desarrollo (verificación inmediata)
- **CI/CD**: Playwright en GitHub Actions contra Vercel preview
- **Staging**: Tests E2E completos antes de merge
- **Production**: Smoke tests post-deployment

### 9.5. Configuración Automática General

1. **Detectar complejidad** del proyecto
2. **Configurar GitHub Actions MCP** si hay repositorio
3. **Configurar Playwright** automáticamente para proyectos web
4. **Sugerir herramientas QA** adicionales apropiadas
5. **Solicitar aprobación** del usuario
6. **Configurar automáticamente** MCPs y pipelines
7. **Documentar setup** en `project_context.md`

---

## **CHECKLIST DE VERIFICACIÓN OBLIGATORIO**

### Antes de Avanzar de Fase 1 a Fase 2:
- [ ] `/docs/project-input/` consultado completamente
- [ ] URL de GitHub detectada (si está disponible)
- [ ] **GitHub Actions MCP configurado** automáticamente
- [ ] **Workflows existentes analizados** y documentados
- [ ] **Context7 consultado** para documentación del stack detectado
- [ ] **Sequential Thinking aplicado** si análisis es complejo
- [ ] `project_context.md` creado en `/docs/current-sprint/planning/`
- [ ] `.augment/rules/` configurado
- [ ] MCPs contextuales implementados
- [ ] Task list actualizada
- [ ] **COMMIT AUTOMÁTICO**: "feat: complete phase 1 - project analysis and setup"
- [ ] **CI/CD PIPELINE VERDE** ✅ (obligatorio)
- [ ] **APROBACIÓN EXPLÍCITA del usuario recibida** (con posibles mini-iteraciones)

### Antes de Avanzar de Fase 2 a Fase 3:
- [ ] **Context7 consultado** para guías de arquitectura y APIs
- [ ] **Sequential Thinking aplicado** para decisiones arquitectónicas complejas
- [ ] `planning_doc.md` completo en `/docs/current-sprint/planning/`
- [ ] TODAS las historias creadas en `/docs/current-sprint/stories/`
- [ ] **Sequential Thinking usado** para descomponer features complejas
- [ ] **Workflows CI/CD configurados** según stack tecnológico
- [ ] **Integración Vercel-GitHub verificada**
- [ ] Herramientas QA configuradas (Playwright + GitHub Actions)
- [ ] Estructura de directorios organizada
- [ ] **INPUTS MOVIDOS**: `/docs/project-input/` → `/docs/processed-input/sprint-[X]/`
- [ ] **COMMIT AUTOMÁTICO**: "feat: complete phase 2 - planning and stories for sprint [X]"
- [ ] **CI/CD PIPELINE VERDE** ✅ (obligatorio)
- [ ] **APROBACIÓN EXPLÍCITA del usuario recibida** (con posibles mini-iteraciones)

### Antes de Finalizar un Sprint:
- [ ] TODAS las historias implementadas
- [ ] TODAS las verificaciones en `/docs/current-sprint/verification/`
- [ ] **Tests pasando** (unitarios + integración + **E2E con Playwright**)
- [ ] **CI/CD pipeline verde** en GitHub Actions ✅
- [ ] **Vercel deployment exitoso** (preview y/o producción)
- [ ] **Smoke tests post-deployment** pasando
- [ ] Documentación técnica actualizada
- [ ] **COMMITS POR HISTORIA**: "feat: implement story [ID] - [nombre]"
- [ ] **COMMIT FINAL**: "feat: complete sprint [X] - all stories implemented"
- [ ] **PIPELINE FINAL VERDE** ✅ (obligatorio)
- [ ] **APROBACIÓN EXPLÍCITA del usuario recibida**

### Antes de Iniciar Nuevo Sprint:
- [ ] Sprint anterior movido a `/docs/sprint-[número]/`
- [ ] `sprint-summary.md` creado
- [ ] Nuevo `/docs/current-sprint/` creado
- [ ] Branch `sprint-[número]` creado (si aplica)
- [ ] **COMMIT**: "feat: finalize sprint [X] - ready for next sprint"
- [ ] **APROBACIÓN EXPLÍCITA del usuario recibida**

---

**REGLA DE ORO: NUNCA avanzar sin completar TODOS los checkboxes de la fase actual. Esta metodología garantiza consistencia, calidad y trazabilidad en todos los proyectos.**