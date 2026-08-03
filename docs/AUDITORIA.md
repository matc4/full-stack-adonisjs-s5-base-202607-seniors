# Auditoría

## Parte A — Revisión del backlog de historias de usuario

| Ajuste | Motivo |
|---|---|
| Proveer un formato de ejemplo de user story más breve y solo referencial. | Hizo que cumpliera una plantilla de User Story con demasiadas secciones y, al no tomarlo como referencia sino como obligatorio, alguna información era reiterativa. |
| Proveer antiejemplos o restricciones más claras. | Al no ser explícito, muchas historias se crearon con comentarios técnicos que no corresponden a esta etapa, enfocada en definición de producto. |

## Parte B — Auditoría de documentación

Estado de la documentación del proyecto.

### Hallazgos

| Tipo de doc | Estado | Ubicación | Observación |
|---|---|---|---|
| README de proyecto | **Completo** | [README.md](../README.md) | No pude levantar el proyecto porque faltaba una librería, `@poppinss/ts-exec`. Pero se lo asigno más a una falta de doc de troubleshooting. |
| Descripción de la arquitectura general | **Parcial** | [backend/README.md](../backend/README.md) | Existe un README de backend, pero el frontend no tiene uno equivalente. |
| Documentación de la API o de los endpoints | **Parcial** | [README.md](../README.md) | Están los endpoints en el README, pero no tienen detalle exacto de cómo llamarlos y qué responden. La información está incompleta. |
| Docstrings y comentarios significativos en código (TSDoc/JSDoc) | **Parcial** | — | Están los comentarios, pero solo dicen lo obvio. No tienen ninguna aclaración sustancial que aporte algo diferente a lo que ya se puede ver a simple vista. |
| Decisiones técnicas registradas | **Nulo** | — | El README aclara que es un asunto pendiente. |
| Guía operacional | **Nulo** | — | No hay instrucciones de despliegue ni de troubleshooting. De hecho tuve algunos problemas para levantar el proyecto y no tuve guía para solucionarlo. |
| Convenciones de código del proyecto | **Parcial** | [CLAUDE.md](../CLAUDE.md) | Tiene convenciones generales importantes, pero falla en dar otras convenciones que son de relevancia, como por ejemplo cómo nombrar los artefactos. |
| Especificación OpenSpec y su trazabilidad con el código | **Parcial** | — | El endpoint `health` no tiene spec, y un endpoint `/users/active` está especificado pero no tiene implementación. |

### Top 3 carencias que más duelen

1. Que no exista un archivo de troubleshooting: impide levantar el proyecto.
2. Que no exista un README del frontend.
3. Que no exista un documento de arquitectura general del proyecto.

### Top 3 cosas que ya están bien

1. El README general del proyecto.
2. El README del backend.
3. OpenSpec de las funcionalidades.

## Exploración de formatos de documentación

- **Diagrama C4** — Permite manejar distintos niveles de detalle de la arquitectura, pudiendo elegir simpleza o más complejidad según el análisis que se requiera hacer.
- **ADR** — Es importante al explicar por qué se tomaron ciertas decisiones de arquitectura en el ciclo de vida de un proyecto. Con el tiempo pueden volver a plantearse las mismas interrogantes y perderse los justificativos que llevaron a la arquitectura actual.
- **OpenAPI** — Aporta detalles estructurados de cómo consumir un API, al ser estructurado puede utilizarse de manera muy fiable para que Devs o Agentes construyan una integración contra dicha API
