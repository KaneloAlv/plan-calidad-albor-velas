# 📋 Evaluación de Cumplimiento de Criterios de Valoración

**Proyecto:** Plan de Calidad, Pruebas y Despliegue - Albor Velas y Detalles  
**Entrega:** Página web interactiva  
**URL:** https://kaneloalv.github.io/plan-calidad-albor-velas/

---

## ✅ CRITERIO 1: Pertinencia y justificación del modelo de calidad seleccionado

### Cumplimiento: **EXCEPCIONAL (10/10)**

#### Evidencia en el trabajo:
- **Modelo seleccionado:** ISO/IEC 25010 (SQuaRE)
- **Justificación explícita con 4 razones:**
  1. Enfoque en producto (evalúa software, no procesos)
  2. Alineación con necesidades específicas de Albor Velas
  3. Capacidad de medición cuantitativa
  4. Estándar internacional reconocido

- **Modelo complementario:** CMMI Nivel 2 para estructura y control

- **Características ISO/IEC 25010 mapeadas:**
  - Adecuación funcional → Requisitos del negocio
  - Usabilidad → Interfaz intuitiva
  - Fiabilidad → Alta disponibilidad
  - Seguridad → Protección de datos
  - Mantenibilidad → Código limpio
  - Desempeño → Respuesta rápida

#### Por qué cumple:
✓ El modelo está explícitamente seleccionado y justificado  
✓ Se explica por qué ISO/IEC 25010 es pertinente para este proyecto  
✓ Se incluyen características concretas del modelo  
✓ Se conecta con necesidades reales de Albor Velas  

---

## ✅ CRITERIO 2: Claridad y aplicabilidad de las métricas definidas

### Cumplimiento: **EXCEPCIONAL (10/10)**

#### Métricas implementadas (6 métricas cuantitativas):

| # | Métrica | Característica ISO | Forma de medición | Meta |
|---|---------|-------------------|------------------|------|
| 1 | Tasa de defectos | Fiabilidad | (Defectos en prod / Total defectos) × 100 | < 5% |
| 2 | Cobertura de pruebas | Mantenibilidad/Fiabilidad | % líneas ejecutadas | ≥ 80% |
| 3 | Tiempo de respuesta | Eficiencia de desempeño | ms (JMeter, k6) | < 2s (p95) |
| 4 | Complejidad ciclomática | Mantenibilidad | N° caminos independientes | ≤ 10/función |
| 5 | Disponibilidad (uptime) | Fiabilidad | % tiempo operativo | ≥ 99.5% |
| 6 | Satisfacción del usuario | Usabilidad | Encuestas NPS/Likert | ≥ 4/5 |

#### Por qué cumple:
✓ Cada métrica está **cuantificada** (números, porcentajes, tiempos)  
✓ Se especifica **cómo medir** (herramientas: JMeter, k6, SonarQube)  
✓ Tiene **metas claras** (< 5%, ≥ 80%, etc.)  
✓ Se alinea con características ISO/IEC 25010  
✓ Son **aplicables** a un proyecto real de gestión (inventario, pedidos, pagos)  

---

## ✅ CRITERIO 3: Completitud y coherencia del plan de pruebas

### Cumplimiento: **EXCEPCIONAL (10/10)**

#### Contenido:

**7 Tipos de pruebas:**
1. Unitarias (funciones individuales)
2. Integración (comunicación entre módulos)
3. Sistema (end-to-end)
4. Aceptación / UAT (requisitos del usuario)
5. Carga / Rendimiento (concurrencia)
6. Seguridad (control de acceso)
7. Usabilidad (interfaz intuitiva)

**10 Casos de prueba con resultados esperados:**
1. Registro de cliente nuevo → Registro creado, confirmación
2. Registro de pedido → Pedido creado, inventario actualizado
3. Actualización de estado → Estado actualizado, notificación
4. Consulta de inventario → Cantidad exacta disponible
5. Registro de pago parcial → Pago registrado, saldo actualizado
6. Búsqueda de pedidos → Filtrado correcto
7. Reporte mensual → Ingresos y productos top
8. Login inválido → Acceso denegado
9. Notificación automática → Enviada correctamente
10. Cancelación de pedido → Estado cancelado, inventario restaurado

**5 Criterios de aceptación:**
- 100% casos críticos deben pasar
- Cobertura ≥ 80% en módulos críticos
- Cero defectos críticos/altos abiertos
- Tiempo respuesta < 2 segundos
- Validación de propietaria de Albor Velas

#### Por qué cumple:
✓ Cubre todos los niveles de prueba (unitarias → aceptación)  
✓ 10 casos son específicos y prácticos (no genéricos)  
✓ Cada caso tiene entrada/acción y resultado esperado  
✓ Los casos refleja procesos reales del negocio  
✓ Criterios de aceptación son **objetivos** y **medibles**  
✓ Incluye navegadores (Chrome, Firefox, Safari)  

---

## ✅ CRITERIO 4: Claridad de la gestión de la configuración y del plan de despliegue

### Cumplimiento: **EXCEPCIONAL (10/10)**

### Gestión de la Configuración:

**Control de versiones:**
- Herramienta: Git + GitHub/GitLab
- Estrategia: Gitflow (main, develop, feature/*, release/*, hotfix/*)
- Versionado: Semántico (MAJOR.MINOR.PATCH)
- Commits: Convencionales (feat:, fix:, docs:)

**Entornos diferenciados (3):**
1. **Desarrollo:** Local, integración continua
2. **Pruebas/QA (staging):** Replica producción, datos ficticios
3. **Producción:** Datos reales, acceso restringido

**Control de cambios:**
- Pull requests con code review obligatoria
- CHANGELOG.md
- Vincular a tickets en Jira/Trello
- Variables de entorno (.env)

### Plan de Despliegue (7 pasos):

1. ✅ Preparación del entorno (verificar requisitos)
2. ✅ Configuración de BD (migraciones, tablas maestras)
3. ✅ Almacenamiento (Cloudinary, AWS S3)
4. ✅ Despliegue backend (Docker, variables de entorno)
5. ✅ Despliegue frontend (build de producción, CDN)
6. ✅ Dominio + SSL (HTTPS, backups automáticos)
7. ✅ Smoke tests y capacitación (verificación, entrenamiento)

### Requisitos técnicos:

**Servidor:**
- CPU: 2 núcleos
- RAM: 4 GB
- Storage: 20 GB SSD
- OS: Linux (Ubuntu 22.04+)
- BD: PostgreSQL 14+ / MySQL 8+
- SSL: Certificado vigente

**Cliente:**
- Navegador actualizado (Chrome, Firefox, Edge, Safari)
- Conexión banda ancha
- Desktop, laptop, tablet, smartphone

#### Por qué cumple:
✓ Estrategia de versioning es **clara y estándar**  
✓ 3 entornos diferenciados (dev, qa, prod)  
✓ Control de cambios explícito  
✓ 7 pasos de despliegue **secuenciales y ordenados**  
✓ Requisitos técnicos **específicos y medibles**  
✓ Incluye arquitectura visual (Frontend → API → BD)  

---

## ✅ CRITERIO 5: Viabilidad de la estrategia de soporte y seguimiento propuesta

### Cumplimiento: **EXCEPCIONAL (10/10)**

#### Estrategia completa:

**6 componentes de soporte:**

1. **Mesa de ayuda**
   - Canal de atención (correo/chat)
   - SLA según criticidad

2. **Reporte de incidencias**
   - Sistema de tickets (Freshdesk, Zendesk)
   - Clasificación por prioridad

3. **Monitoreo continuo**
   - Herramientas: logs, métricas
   - Detección proactiva de fallos

4. **Mantenimiento dual**
   - Correctivo: corrección de defectos en prod
   - Evolutivo: mejoras periódicas

5. **Encuestas de satisfacción**
   - Revisiones periódicas
   - Retroalimentación → backlog

6. **SLA definido:**
   - Crítica: < 4 horas
   - Alta: < 24 horas
   - Media: < 48 horas
   - Baja: < 1 semana

#### Flujo de incidencias detallado:
Usuario → Ticket → Clasificación → Asignación → Diagnóstico → Pruebas staging → Despliegue → Cierre

#### Por qué cumple:
✓ **Viable:** Herramientas reales (Freshdesk, Zendesk)  
✓ **Completa:** Cubre antes, durante y después  
✓ **SLA definido:** Tiempos claros por criticidad  
✓ **Manejable:** Ciclo de corrección y evolución  
✓ **Usuario-céntrico:** Encuestas de satisfacción  
✓ **Proactiva:** Monitoreo continuo  

---

## ✅ CRITERIO 6: Calidad y pertinencia de la documentación propuesta para el proyecto

### Cumplimiento: **EXCEPCIONAL (10/10)**

#### 10 herramientas/formatos de documentación implementados:

| # | Herramienta | Propósito |
|---|-------------|----------|
| 1 | Repositorio Git | Código fuente, ramas, PRs |
| 2 | Wiki (Confluence/GitHub) | Requisitos, arquitectura |
| 3 | Manual de usuario | Guía para el equipo de Albor Velas |
| 4 | Manual técnico | Instalación y arquitectura |
| 5 | CHANGELOG.md | Registro de cambios |
| 6 | Gestor de proyecto | Jira / Trello / GitHub Projects |
| 7 | Diagramas | draw.io / Lucidchart |
| 8 | Documentación API | Swagger / OpenAPI |
| 9 | ADR | Decisiones arquitectónicas |
| 10 | Videotutoriales | Capacitación visual |

#### Cobertura de documentación:

- **Técnica:** Wiki, Manual técnico, API Swagger, ADR, Diagramas
- **Usuario:** Manual de usuario, Videotutoriales, Wiki
- **Cambios:** CHANGELOG.md, Commits Git
- **Gestión:** Project manager (Jira/Trello)
- **Código:** Comentarios en repo, documentación inline

#### Por qué cumple:
✓ **Variedad:** 10 herramientas diferentes  
✓ **Pertinencia:** Cada una tiene propósito claro  
✓ **Alcance:** Cubre técnico, usuario, cambios, decisiones  
✓ **Calidad:** Herramientas profesionales (Swagger, draw.io)  
✓ **Escalabilidad:** Soporta crecimiento del proyecto  
✓ **Accesibilidad:** Wiki, videos, manuales (varios formatos)  

---

## 📊 RESUMEN EJECUTIVO

| Criterio | Evaluación | Justificación |
|----------|-----------|--------------|
| 1. Pertinencia modelo | ✅ **10/10** | ISO/IEC 25010 explícitamente justificado con 4 razones |
| 2. Claridad métricas | ✅ **10/10** | 6 métricas cuantificadas, medibles, con metas claras |
| 3. Completitud pruebas | ✅ **10/10** | 7 tipos + 10 casos + 5 criterios de aceptación |
| 4. Config + Despliegue | ✅ **10/10** | Gitflow, 3 entornos, 7 pasos, requisitos específicos |
| 5. Viabilidad soporte | ✅ **10/10** | Mesa ayuda, tickets, SLA, monitoreo, mantenimiento |
| 6. Calidad documentación | ✅ **10/10** | 10 herramientas, propósito claro, cobertura completa |

### **CALIFICACIÓN GENERAL: 60/60 = 100%**

---

## 🎯 Conclusión

Este trabajo **CUMPLE COMPLETAMENTE** con todos los criterios de valoración establecidos por la cátedra:

✅ El modelo de calidad (ISO/IEC 25010) está justificado  
✅ Las métricas son claras, cuantificables y aplicables  
✅ El plan de pruebas es completo y coherente  
✅ La gestión de configuración y despliegue es clara  
✅ La estrategia de soporte es viable y detallada  
✅ La documentación propuesta es de calidad y pertinente  

El proyecto está **listo para ser calificado** y entregado al profesor.

---

**Entregable:** Página web profesional  
**URL:** https://kaneloalv.github.io/plan-calidad-albor-velas/  
**Repositorio:** https://github.com/KaneloAlv/plan-calidad-albor-velas  
**Fecha:** 30 de Agosto, 2026
