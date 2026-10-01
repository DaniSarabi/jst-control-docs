# D7 · ¿Cómo se piden los cambios de accesos?

**Para:** Gerente de IT
**Tema:** 6.2 del brief, "todo cambio de accesos pasa por un documento". Aquí también entra la excepción de USB.

---

## 1. Qué tiene que resolver cualquier opción

| Necesidad | Por qué |
|---|---|
| El gerente **no tiene que saber qué permisos tiene hoy** el usuario. | No lo sabe, ni tiene por qué. Solo pide qué agregar o quitar y por qué. |
| **IT registra el "antes" y el "después".** | IT es quien ve los permisos en los sistemas. Sin el "antes", no se puede reconstruir por qué alguien tiene lo que tiene. |
| El cambio queda en el **expediente del usuario**. | De ahí sale el historial (ya está en NO-PIT-001). |
| Sirve para: agregar acceso, quitar acceso, cambio de puesto y excepción temporal (USB, etc.). | Que sea una sola ruta para todo cambio. |
| Llenarlo toma **menos de 5 minutos**. | Si es más pesado que mandar un correo informal, la gente va a seguir mandando correos informales. |

---

## 2. Algo que encontré al revisarlo: el 001 hoy tiene tres tipos

El NO-FIT-001 actual tiene los tipos **NEW, MOD y DEL**. Pero las bajas ya tienen su propio formato, el **NO-FIT-005**, y el NO-PIT-001 dice que la revocación se hace con el 005. Entonces hoy **hay dos caminos para dar de baja a un usuario**, y el DEL del 001 nadie lo usa (o no debería).

Si sacamos también el MOD, el ciclo de vida queda con **un documento por etapa**:

| Etapa | Documento |
|---|---|
| Alta | NO-FIT-001 (solo altas) |
| **Cambio** | **Solicitud de cambio de accesos** (según la alternativa que elijas) |
| Baja | NO-FIT-005 |

Este hallazgo es lo que me hizo cambiar de recomendación (ver sección 5).

---

## 3. Las alternativas

### Alternativa A · Hoja de cambio dentro del NO-FIT-001

El 001 lleva una página aparte, "Cambio de accesos". Para un cambio, el gerente llena solo esa página.

- ✅ No se agrega ningún código al sistema de calidad.
- ❌ El gerente abre "el formato de alta" para pedir un cambio. Va a ver todo el formato y se va a confundir, o lo va a llenar completo, que es justo lo que no quieres.
- ❌ El 001 crece. Ya trae la parte de hardware, aplicaciones y SAP, y le estaríamos agregando otra página.
- ❌ Cuando se revise el 001 por un tema de altas (por ejemplo, SAP), también se revisa la hoja de cambios, aunque no haya cambiado nada en ella.

### Alternativa B · Formato aparte: "Solicitud de cambio de accesos"

Una sola página, con código propio (ver sección 6).

- ✅ Es claro: el nombre del formato dice para qué sirve.
- ✅ Corto: se llena en minutos.
- ✅ Ciclo de vida limpio: alta (001), cambio (este), baja (005).
- ✅ El 001 se simplifica: solo altas. Se le quitan los tipos MOD y DEL.
- ❌ Agrega un código al sistema. Se compensa, porque el 001 pierde dos tipos que hoy confunden.

### Alternativa C · Sin formato: correo con plantilla fija

El jefe manda un correo a IT con un asunto y unos campos fijos. IT archiva el correo en el expediente y anota el "antes / después" en una hoja de registro.

- ✅ Es lo más ligero para el gerente.
- ✅ Encaja con el flujo digital que ya se definió para el 001 (la autorización es el correo del jefe).
- ❌ Los correos se desordenan rápido: falta un campo, el asunto cambia, alguien responde en otro hilo.
- ❌ El "antes / después" de IT queda separado de la solicitud, en otra hoja.
- ❌ En una auditoría ISO, "un correo con plantilla" es más difícil de defender como registro controlado que un formato con código.

---

## 4. Cómo se vería (contenido de las alternativas A y B)

El contenido es **el mismo** en A y B. Lo único que cambia es si lleva código propio o es una página del 001.

**SOLICITUD DE CAMBIO DE ACCESOS**

**1. Usuario**

| Nombre: | | Número de empleado: | |
|---|---|---|---|
| Puesto actual: | | Departamento: | |
| Planta: | ☐ Planta 1 ☐ Planta 2 | Jefe inmediato: | |

**2. Tipo de cambio** (marca uno)

☐ Agregar acceso ☐ Retirar acceso ☐ Cambio de puesto ☐ Excepción temporal (USB, otro)

*Si es cambio de puesto:*

| Puesto nuevo: | | Fecha efectiva: | |
|---|---|---|---|
| Persona con funciones equivalentes en el puesto nuevo (para copiar sus accesos): | | | |
| ¿Requiere cambio de equipo? | ☐ No ☐ Sí → se hace con NO-FIT-002 | | |

**3. Qué se pide**

| Sistema o recurso | Agregar / Quitar | ¿Qué necesita hacer el usuario? (en palabras simples) | ¿Temporal? Hasta: |
|---|---|---|---|
| | | | |
| | | | |
| | | | |

**4. Justificación**

*¿Por qué se necesita el cambio?*

**5. Autorización del jefe inmediato**

☐ Autorizado por correo. Fecha del correo: ________ *(o firma, según se decida en NO-FIT-001)*

**6. Uso exclusivo de IT**

| | |
|---|---|
| Accesos que tenía antes (solo los relacionados con el cambio): | |
| Accesos otorgados o retirados: | |
| Lo negado y por qué: | |
| Accesos del puesto anterior retirados (si fue cambio de puesto): | ☐ Sí ☐ N/A |
| Ejecutó (nombre, puesto de IT): | |
| Fecha de recepción de la solicitud: | |
| Fecha de ejecución: | |
| ☐ Guardado en el expediente del usuario ☐ Inventario actualizado (si hubo equipo o USB) | |

> **Pendiente:** si un cambio toca **SAP**, la sección 3 tiene que usar el mismo vocabulario que se decida para el alta de SAP en NO-FIT-001. Esta hoja se ajusta cuando se resuelva el 001.

---

## 5. Lo que yo haría

**Alternativa B, formato aparte.**

Antes te recomendé A por el principio de no inflar el sistema. Cambié de opinión por dos razones:

1. **El contenido es igual en A y B**, así que la diferencia es solo de presentación. En presentación, B gana: un gerente que quiere quitarle un permiso a alguien no debería abrir "el formato de alta".
2. **El DEL del 001 duplica al 005.** Con B, el 001 se simplifica a solo altas, y el ciclo de vida queda con un documento por etapa. El sistema queda con el mismo número de trámites, pero cada uno con su formato y sin traslapes. Esto no infla el sistema; lo ordena.

La C la descarto: para dos personas de IT parece la más ligera, pero termina costando más cuando hay que encontrar algo en una auditoría.

---

## 6. Si eliges B, lo que hay que tocar

1. **Código nuevo.** Los números 004 (videovigilancia, citado en NO-PIT-002) y 008 ya están ocupados o no los conozco. **¿Qué número sigue libre en la serie NO-FIT?** No voy a asignarlo yo.
2. **NO-FIT-001:** quitar los tipos MOD y DEL. Queda solo para altas.
3. **NO-FIT-005 (choca con el brief):** el F5-03 pide que el 005 contemple el **cambio de puesto** como tipo de baja. Con B, el cambio de puesto se pide en la solicitud de cambio, porque implica quitar **y** agregar accesos. El 005 se quedaría para: salida ordenada, despido, incapacidad prolongada y suspensión. **Hay que decidir esto antes de llegar al 005.**
4. **NO-PIT-001:** en "Controles lógicos", los cambios de roles se documentan con la solicitud de cambio, no con el UAR (NO-FIT-001). Lo mismo para la excepción de USB en la sección 5.5 F.
5. **NO-PIT-001 §6 Documentación:** agregar el formato nuevo.

Esto sería **el único documento nuevo** de esta revisión. Si lo apruebas, lo hago completo (con bitácora) cuando lleguemos al 001, porque se diseñan juntos.
