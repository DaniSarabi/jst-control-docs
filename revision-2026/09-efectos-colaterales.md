# Efectos colaterales y estado del paquete

**Para:** Gerente de IT
**Contenido:** el punto 6 del brief, la lista de cambios que obligan a tocar los procedimientos o que chocan con algo fuera de alcance, consolidada de los siete documentos trabajados.

---

## 1. Estado del paquete

| Documento | Archivo | Estado |
|---|---|---|
| NO-FIT-003 · Acuse de la Política de Uso de Equipo y Recursos de IT | `01-NO-FIT-003.md` | Cerrado |
| Texto para NO-PIT-001 (sección 5.5 nueva) | `01b-texto-para-NO-PIT-001.md` | Cerrado |
| NO-FIT-002 · Acta de Entrega y Devolución de Equipo de IT | `03-NO-FIT-002.md` | Cerrado |
| NO-FIT-005 · Baja de Usuario | `04-NO-FIT-005.md` | Cerrado |
| NO-FIT-001 · Solicitud de Alta de Usuario (con Anexo SAP) | `05-NO-FIT-001.md` | Cerrado |
| NO-FIT-010 · Solicitud de Cambio de Accesos (**nuevo**) | `06-NO-FIT-010.md` | Cerrado |
| NO-FIT-009 · Configuración Inicial de Equipo | `07-NO-FIT-009.md` | Cerrado |
| NO-FIT-006 · Lista de Verificación de Mantenimiento Preventivo | `08-NO-FIT-006.md` | Cerrado |
| NO-FIT-007 · Lista de Software Aprobado | — | **Fuera de esta vuelta** (decisión del Gerente de IT) |

---

## 2. Cambios que hay que hacer en NO-PIT-001

Además de incorporar la sección 5.5 completa (`01b-texto-para-NO-PIT-001.md`):

| # | Sección | Cambio | Viene de |
|---|---|---|---|
| 1 | 4 Definiciones, "Acceso remoto" | Quitar **Dell SonicWall**. Ya no se usa. | 005 |
| 2 | 5.3 Generales | La UAR (NO-FIT-001) la hace el **gerente del área**, no el jefe inmediato. | D27 |
| 3 | 5.3 Generales | *"IT dará mantenimiento preventivo a los equipos de cómputo **cada seis meses** utilizando NO-FIT-006."* | 006 |
| 4 | 5.3 Medios de almacenamiento | Agregar: *"Solo se usan medios de la Compañía entregados por IT conforme a 5.5 F."* | 003 |
| 5 | 5.3 Actualizaciones y Parches | Cambiar *"siguiendo NO-FIT-006"* por *"Los equipos se actualizan de forma automática con Windows Update. En el mantenimiento semestral (NO-FIT-006) se verifica que las actualizaciones estén al día."* | 006 |
| 6 | 5.3 Controles lógicos, requisitos de cuentas | Altas con NO-FIT-001 y cambios con **NO-FIT-010**, autorizados por el gerente del área. NO-FIT-001 aplica a usuarios con **cuenta nominal**. Los operadores de estaciones compartidas firman NO-FIT-003 y la lista del acta NO-FIT-002. | D7, D27, 001-H6 |
| 7 | 5.3 Controles lógicos, roles | Los cambios de roles se documentan con **NO-FIT-010**, ya no con la UAR. | D7 |
| 8 | 5.3 Controles lógicos, datos del usuario dado de baja | El responsable de los datos es el **jefe inmediato** durante **90 días** (unidad H:). El buzón pasa a buzón compartido con acceso para quien indique el jefe, durante **30 días**. | 005 |
| 9 | 5.3 Controles lógicos, baja | Agregar los **plazos de aviso de RH**: 1 día hábil antes en salida ordenada, antes de la notificación en despido, y el primer día en suspensión. | 005 |
| 10 | 5.4 | Corregir la dependencia circular. Para crear accesos se necesita el **NO-FIT-001**; para entregar equipo, el **NO-FIT-003** firmado; al entregar, se firma el **NO-FIT-002**. | Arranque 4.3 |
| 11 | 6 Documentación | Actualizar los nombres de 001, 002, 003, 005, 006 y 009. Agregar **NO-FIT-010 Solicitud de Cambio de Accesos**. | Todos |
| 12 | 5.1 | Cita **NO-FME-046 Formato de desviación**, que IT no conoce. Que Calidad confirme si existe. Si no existe, quitar la cita. Las excepciones de IT ya no lo usan (van por NO-FIT-010). | Arranque 3.4 |
| 13 | Varias | "Administrador de IT" y "Administrador correspondiente" se cambian por el **puesto oficial** (pendiente P13). | Principio 4.3 |

---

## 3. Lo que queda abierto por haber saltado NO-FIT-007

1. **NO-FIT-009 instala software que el 007 no lista:** WinRAR, PDF XChange, Snagit, LightCast y el cliente Lek. Hoy el setup contradice la regla de "solo software aprobado".
2. **El 007 sigue listando SonicWall**, que ya no se usa. También hay que confirmar que DriverEasy no esté en la lista.
3. **NO-FIT-006, renglón 16** (software contra lista aprobada) se marca N/A hasta que se actualice el 007.
4. **NO-PIT-001 5.5 E** remite a un "registro de solicitud de software en NO-FIT-007" que todavía no existe. Mientras tanto, la solicitud de software que no está en la lista se hace con **NO-FIT-010**.
5. El brief tenía pendientes en el 007 que no se tocaron: quitar versiones, separar el software de producción del de oficina, licenciamiento, periodicidad de revisión, y la regla "versión soportada por el fabricante" (con el riesgo de que Acrobat XI y SolidWorks 2013 queden fuera de cumplimiento).

---

## 4. Dependencias fuera de alcance

| Tema | Qué depende de él |
|---|---|
| **Bloqueo técnico de USB (GPO)** | Mientras no exista, la prohibición de USB (5.5 F) se cumple solo por disciplina. |
| **Borrado seguro del disco** | NO-FIT-005 solo registra el destino del disco; no dice cómo se borra. |
| **Buzón de correo de IT** | No existe. Las solicitudes de 001 y 010 llegan a una persona, y si esa persona falta, se atoran. Riesgo aceptado (D24). |

---

## 5. A quién hay que avisar

| Quién | Qué cambia para ellos |
|---|---|
| **RH** | Plazos de aviso de baja. Recoger el equipo y entregarlo a IT para que IT lo revise. La sección 4 del acta NO-FIT-002 (responsabilidades, sin cobro) conviene que la lean antes de emitirla. |
| **Gerentes de área** | Ahora **ellos** envían y autorizan NO-FIT-001 y NO-FIT-010 por correo, incluidas las laptops (ya no las autoriza el Gerente de Planta). |
| **Supervisores de área** | Recaban la firma de cada usuario nuevo en el acta del equipo compartido y la entregan a IT. |
| **LEK** | Confirmar que el buzón compartido se conserva los 30 días con la cuenta de AD deshabilitada. |
| **Todo el personal** | Firma el nuevo acuse NO-FIT-003, incluidos los operadores de estaciones compartidas. |

---

## 6. Requisitos del inventario de activos

Sin nombrar la herramienta, el inventario tiene que guardar por cada equipo:
- Asset ID, número de serie, tipo, marca y modelo.
- A quién o a qué área está asignado (*check-out*) y su ubicación.
- Fecha de compra y vencimiento de la garantía.
- Fecha del próximo mantenimiento preventivo.
- Las USB de la empresa entregadas por excepción, asignadas al usuario.

---

## 7. Preguntas del arranque que nunca se contestaron

| # | Pregunta | Efecto si no se contesta |
|---|---|---|
| P1 | Revisión vigente de la plantilla NO-FQA-002 (Rev A o Rev B). | Lo resuelves al pasar los documentos a la plantilla. |
| P12 | Idioma. | Todo el paquete quedó en español. Como no hubo objeción, lo doy por aceptado. |
| P13 | Puestos oficiales de las dos personas de IT. | Los documentos dicen "Gerente de IT" y "personal de IT". Si el puesto oficial es otro, hay que ajustarlo. |
