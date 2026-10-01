# Revisión de documentos de IT — Arranque

**Para:** Gerente de IT, JST Power Equipment Nogales
**Contenido:** orden de trabajo propuesto, preguntas que bloquean, decisiones transversales, puntos donde el brief no cuadra con los documentos y hallazgos preliminares.

Todavía no se reescribe ningún documento. El brief pide levantar las preguntas primero, y varias de ellas cambian el contenido de más de un formato.

---

## 1. Orden propuesto

| # | Documento | Por qué en este lugar | Depende de |
|---|---|---|---|
| 1 | **NO-FIT-003** + texto para NO-PIT-001 | Fija las reglas de las que cuelgan los demás: quién solicita el equipo, la excepción de USB, la revisión periódica y la regla de equipo compartido. Si esto cambia después, hay que retocar 002, 005 y 009. | P3, P6 |
| 2 | **NO-FIT-002** | Es el acta de entrega. Define la estructura de inventario que reutilizan la baja (005) y el setup (009). Aquí se resuelve F2-03 y el equipo compartido (6.1). | Estructura aprobada en el punto 3 de este documento |
| 3 | **NO-FIT-005** | Toma la estructura del 002 y la usa en la devolución. Es el formato más completo, así que el trabajo es acotado. | 002, P7, P8 |
| 4 | **NO-FIT-001** | Lleva la decisión de SAP, la ruta MOD (6.2) y el flujo digital. Lo pongo después de 002 porque el catálogo de hardware de 001 tiene que usar las mismas categorías que el acta. | P1, P2, P4, P9, P10, decisión SAP |
| 5 | **NO-FIT-007** | Es el más independiente, pero 009 y 006 lo referencian. | P5, P6, P11 |
| 6 | **NO-FIT-009** | Integra 001 (vocabulario SAP), 007 (software, sin DriverEasy) y 002 (entrega). Tiene que ir al final de esa cadena. | 001, 007 |
| 7 | **NO-FIT-006** | Las decisiones ya están tomadas (semestral, firmas, quitar IPX y unidad óptica). Lo dejo al último porque el renglón "software contra lista aprobada" depende de 007, y porque propongo que este mismo checklist sirva como revisión periódica (ver 3.3). | 007, P6 |

**Alternativa:** si quieres ir calentando mientras contestas las preguntas, NO-FIT-006 es el único que puedo cerrar casi completo sin respuestas. Solo quedaría pendiente la referencia al inventario.

---

## 2. Preguntas

### Las del brief (sección 7)

| # | Pregunta | Bloquea |
|---|---|---|
| P1 | ¿Cuál es la revisión vigente de NO-FQA-002? *(Nota: las versiones en Markdown que recibí no citan NO-FQA-002 en ninguna parte; supongo que la cita está en el encabezado original, que se perdió en la conversión.)* | Todos (solo la referencia) |
| P2 | ¿Existe la instancia de pruebas de SAP para la capacitación "dentro de 15 días"? | 001 |
| P3 | ¿Quién es el dueño del trámite de solicitud de equipo: RH o el jefe inmediato? *(Ver 4.2: hay una tercera versión.)* | 003, 001, PIT-001 |
| P4 | ¿Qué equipo de piso existe realmente? (lectores de código de barras, tablets industriales, impresoras de etiquetas, radios, otros) | 001, 002, 005 |
| P5 | ¿Cuál es la lista real de software en uso? | 007, 009 |
| P6 | ¿Hay un inventario de activos existente? ¿En qué herramienta (Excel, Lansweeper, la consola de LEK, otra) y qué columnas tiene? | **Casi todos.** Es la pieza clave: versiones, licencias, programa de mantenimiento, excepciones de USB y equipo compartido viven ahí según el principio 4.2. Si no existe, el diseño tiene que decir quién lo crea, aunque no sea un documento controlado. |

### Preguntas nuevas

| # | Pregunta | Bloquea | Por qué |
|---|---|---|---|
| P7 | ¿Quién crea y da de baja los usuarios de **videovigilancia**? NO-PIT-002 §5.1 dice "IT / EH&S". | 005, 001 | Si EH&S también crea usuarios, la baja en 005 tiene que incluir a EH&S. Y si en 005 damos de baja ese acceso, el alta también debería quedar registrada en 001. Hoy no hay ningún renglón para eso. |
| P8 | ¿Quién administra los **controles de acceso físico** (gafete, tarjeta, puertas): IT, RH o Seguridad Patrimonial? | 005 | El brief pide agregarlos a la baja. Necesito saber quién ejecuta y quién firma ese renglón. |
| P9 | Hay **tres VPN** (FortiClient → Nogales, SonicWall → Florida, EasyConnect → China). ¿Quién administra cada cuenta? | 005, 009 | La baja actual solo contempla la de China. NO-FIT-009 dice que FortiClient "se pide a Alestra" y EasyConnect "a XU" (una persona, igual que en 005). |
| P10 | ¿Existen de verdad los niveles de Internet "Std Restrictions / Exec Level" y las clases de llamada del teléfono (local / larga distancia / internacional)? | 001 | Si el filtrado lo administra el ISP y no hay perfiles, el formato ofrece algo que IT no puede otorgar. |
| P11 | **MySQL** y **WAMP Server** en la lista aprobada: ¿para qué se usan y en qué equipos? | 007 | Son software de servidor y de desarrollo. Si sostienen una aplicación interna, tienen dueño y van en otra sección. Si ya no se usan, salen. No los voy a quitar sin confirmarlo. |
| P12 | ¿Qué idioma llevan 001, 005, 006, 007 y 009? El brief solo ordena español para 002 (y 003 ya está en español). | Todos | Mi recomendación: todo en español, porque los formatos del sistema de calidad los llena y los audita gente de aquí. Pero es decisión tuya. |
| P13 | ¿Cuáles son los **puestos oficiales** de las dos personas de IT? Hoy aparecen "Gerente de IT", "Administrador de IT", "IT Manager" y "local site administrator". | Todos | Para escribir por puesto (principio 4.3) necesito los nombres de puesto correctos. |
| P14 | ¿El sistema de calidad tiene una regla general de **retención de registros**? NO-PIT-001 Rev D dice en su historial *"se eliminó la tabla de tiempo de retención"*. | 001 (F1-03), 005 (F5-04) | El brief pide definir por cuánto tiempo se guarda el correo de autorización. Hoy no hay un número de referencia y no voy a inventar uno. |

---

## 3. Decisiones transversales que conviene tomar ya

Estas cruzan varios documentos. Prefiero que las veas antes de entregar el primero.

### 3.1 Estructura 002 / 003 / 005 (F2-03). Propuesta

| Formato | Qué es | Cuándo se firma | Quién firma |
|---|---|---|---|
| **NO-FIT-003** | Acuse de lectura y aceptación de la política de uso (las reglas pasan a NO-PIT-001) | **Una vez por usuario**, en el alta, y de nuevo solo si cambia la política | Usuario |
| **NO-FIT-002** | Acta de entrega y recepción: lista de equipo, estado a la entrega, cláusulas de responsabilidad. Lleva una **columna de devolución** del mismo equipo. | **En cada entrega** de equipo, y otra vez cuando se devuelve | Usuario + IT |
| **NO-FIT-005** | Baja o cambio de accesos. **No vuelve a capturar el equipo**: anota el folio o la fecha del 002 y confirma que la devolución quedó registrada ahí. | En la baja | RH + IT |

**Por qué no fusionar 003 dentro de 002:** tienen ciclos distintos. El acuse de política lo firma **todo usuario de recursos de IT**, incluidos los operadores que solo usan una estación compartida con cuenta genérica y que nunca reciben equipo propio. El acta de entrega solo la firma quien recibe equipo, y puede firmarla varias veces. Separados, nadie firma dos cosas parecidas el mismo día por la misma razón. Esto confirma F3-02 en lugar de contradecirlo.

### 3.2 Evidencia digital (001) frente a firma en papel (002 y 003). Opciones, sin resolver

- **A. Convivencia por tipo de documento.** 001 es digital (correo del jefe, guardado como `.msg` o PDF). 002 y 003 siguen en papel firmado, escaneado y guardado. Es simple y no cambia nada para planta. Lo malo: hay dos carpetas y dos criterios.
- **B. Todo digital con firma en tableta o PDF.** Es más ordenado, pero exige herramienta y la validación de RH de que una firma electrónica simple sirve para una cláusula de responsabilidad económica (ver 5.2).
- **Mi recomendación:** A en esta revisión, con **una sola estructura de carpetas y una sola nomenclatura** para los tres tipos de evidencia. Así cambiar a B después no obliga a reescribir los formatos.

### 3.3 Revisión periódica (F3-03) sin crear un proceso nuevo

La propuesta es usar el **mantenimiento preventivo semestral (NO-FIT-006) como la revisión**. En cada mantenimiento el técnico ya tiene el equipo enfrente. Se agregan 3 o 4 renglones:

- el Asset ID, el usuario o área y la ubicación coinciden con el inventario;
- el software instalado coincide con NO-FIT-007;
- las excepciones vigentes (USB, software) siguen justificadas;
- el estado contra el acta 002.

**Evidencia:** el propio 006 firmado. **Frecuencia:** la misma del mantenimiento. **Carga extra:** unos minutos por equipo. No hace falta un programa de auditoría aparte para dos personas.

### 3.4 Excepciones (USB, versión de software no soportada): usar lo que ya existe

NO-PIT-001 §5.1 ya define un formato de desviación, **NO-FME-046**, con justificación y aprobación. Propongo que las excepciones de USB y de software se tramiten con ese formato, que IT las anote en el inventario y que se revisen en el mantenimiento semestral. Así no se crea ningún documento nuevo. Lo detallo en NO-FIT-003.

---

## 4. Donde el brief no cuadra con los documentos

1. **F1-03: "el procedimiento exige firmas autógrafas en los formatos hermanos".** NO-PIT-001 no dice "autógrafas". §5.4 solo dice que 001, 002 y 003 estén "llenados y autorizados". La contradicción real no es papel contra digital: **ningún documento dice qué cuenta como evidencia de autorización**. El ajuste de fondo es el mismo, pero la redacción en PIT-001 debe definir la evidencia, no corregir algo que hoy no dice.
2. **Dueño del trámite (F3-03 / P3): no son dos versiones, son tres.** NO-FIT-003 dice RH. NO-PIT-001 §5.3 (Generales) dice jefe inmediato. NO-PIT-001 §5.3 (Controles lógicos) dice "administrador correspondiente" para altas y "propietario de la empresa correspondiente" para cambios. Además, NO-FIT-003 dice que el equipo se pide **con el NO-FIT-001**: el catálogo de hardware de 001 *es* la solicitud de equipo.
3. **NO-PIT-001 §5.4 tiene una dependencia circular.** Pide que IT verifique que el 002 esté firmado *antes de establecer el acceso*. Pero el 002 se firma al entregar el equipo, y el equipo se entrega después del setup (009), que es donde se crea la cuenta de AD. La secuencia correcta sería: 001 autorizado → crear accesos y preparar equipo (009) → 003 firmado → entregar con 002. Va en efectos colaterales.
4. **F1-04 SAP: el formato ya tiene una ruta por rol.** La sección 2c pide la descripción de la función y un usuario existente para modelar. Lo grueso es la casilla de módulos (2d), que además mezcla cosas que no son módulos ("Security", "Reporting"). Esto inclina la decisión hacia la opción (b), fortaleciendo 2c en lugar de crear un formato. El análisis completo va en 001.
5. **Patches (F9-01 / F6):** NO-PIT-001 dice que los parches se aplican "siguiendo el formato de mantenimiento preventivo NO-FIT-006". Hay dos problemas: (a) leído literalmente, el parcheo sería semestral; (b) **NO-FIT-006 no tiene ningún renglón de Windows Update**. El checklist debe *verificar* que el parcheo automático está al día, y PIT-001 debe decir que el parcheo es continuo.

---

## 5. Hallazgos preliminares (el detalle va en cada documento)

### 5.1 Principio 4.3 (por puesto): casos que el brief no listó

- **NO-FIT-009 item 10:** "EasyConnect (the account is requested from XU)". Es la misma persona del correo en 005 (F5-05). Se cambia por el puesto.
- **NO-FIT-007 columna "Approved By: Luis S."** en todos los renglones. Por las fechas del historial de PIT-001, parece ser alguien que ya no está a cargo. Se propone registrar "puesto + iniciales".

### 5.2 Principio 4.1 (documentos públicos)

- **NO-FIT-009 item 13** expone el nombre del dominio interno de AD, y el **item 12** describe cómo se crea la cuenta de administrador local. Se deja el *qué* ("crear cuenta de dominio según NO-FIT-001", "configurar cuenta de administración local según el registro técnico de IT") y se quita el *cómo*.

### 5.3 NO-FIT-002: la cláusula de responsabilidad económica

- Dice "financial **remuneration**", que significa pagarle *al* empleado; es lo contrario de lo que quiere decir. También responsabiliza al "Employee's **Department**", que no puede pagar nada.
- Más importante: en México los descuentos al salario por pérdidas o averías están limitados por la LFT (art. 110), con topes y condiciones. **Recomiendo que RH o el área legal validen la redacción en español antes de emitirla.** Yo la traduzco y la dejo marcada para validación; no la voy a dar por buena legalmente.

### 5.4 NO-FIT-007: la regla nueva deja equipos fuera de cumplimiento desde el primer día

Al escribir "versión soportada por el fabricante", algunos renglones actuales dejan de cumplir en cuanto se emite el documento. Por ejemplo, **Adobe Acrobat XI** (sin soporte desde 2017) y **SolidWorks 2013**, si esas son las versiones instaladas. Hace falta un plan: actualizar, o abrir una desviación con NO-FME-046. En el software de máquina (WinCC V7.0, JFD-2000) se espera que la versión no esté soportada, y por eso esa sección necesita su propia regla.

### 5.5 Catálogos obsoletos

**Air Card** (módem celular USB) aparece en 002 y 005. Propongo quitarlo, salvo que P4 diga lo contrario.

### 5.6 NO-FIT-001

- Tiene texto basura en el formato vigente: **"Last Name: sdf"**.
- El usuario a clonar se pide **dos veces**: "User is replacing / same function as" en la sección 1 y "Existing User ID to Model" en 2c. Propongo conservar el de la sección 1, como pide el brief, y quitar el de 2c.
- **Contratista / temporal con "Estimated End Date":** el dato se pide pero nada lo usa. Propongo un renglón en "Uso de IT": *fecha de expiración configurada en la cuenta*. Es un control barato y con evidencia (el atributo queda en AD), y evita cuentas temporales que nunca se cierran.
- El vocabulario "Responsibilities / Process Leader / local site administrator" viene de una plantilla de Oracle EBS corporativa. "Process Leader" no es un puesto en JST.

### 5.7 NO-FIT-003

- El acuse firmado dice *"una copia de mi **estado de cuenta** será periódicamente revisado"*. Viene copiado de una política de celulares y aquí no tiene sentido.
- La introducción limita la política a "equipo de cómputo móvil (Laptop)", pero las reglas aplican a todo el equipo.

### 5.8 NO-FIT-005

- Dice que **RH recoge el equipo**. Si IT no recibe el equipo, nadie lo compara contra el estado registrado en la entrega (F2-04). Propongo que RH recoja, pero que IT firme la recepción en la columna de devolución del 002.
- **Microsoft 365:** la secuencia "quitar licencia" + "mantener el reenvío 2 semanas" puede chocar. Quitarle la licencia al buzón lo deja en periodo de gracia. Lo común es convertirlo a buzón compartido. Hay que verificarlo contra cómo lo hace hoy LEK; lo planteo como pregunta en 005, no como cambio.
- La VPN aparece bajo "Remove user from ERP".

### 5.9 NO-FIT-006

- Las columnas "Repair" y "Repaired" son ambiguas.
- No hay campo de notas (mismo problema que F9-03).
- El renglón "Cables unplugged and re-plugged" no aporta y genera fallas.
- "Monitor login script" y "Proxy settings": ¿existen hoy un script de inicio de sesión y un proxy? Si no existen, se quitan.

### 5.10 NO-FIT-009

- Mezcla **tareas del equipo** (software, impresoras) con **tareas de la cuenta** (crear el usuario de AD, permisos en el file server). Si un usuario existente recibe una PC nueva, el checklist le pide crear otra vez su cuenta. Propongo dos bloques: el de cuenta se marca N/A cuando ya existe un 001 procesado.
- **Equipo reasignado:** no hay un paso para limpiar el perfil o los datos del usuario anterior. Conecta con F5-04.

---

## 6. Qué necesito para arrancar

1. Respuestas a **P3 y P6** como mínimo, para empezar NO-FIT-003.
2. Tu visto bueno o tus ajustes a la **estructura 3.1** y a la **idea 3.3** (mantenimiento = revisión periódica).
3. Confirmar el **orden** de la sección 1, o la alternativa de empezar con 006.

Las demás preguntas pueden llegar mientras avanzo, porque bloquean documentos posteriores.

---

## 7. Respuestas recibidas

| # | Respuesta | Efecto |
|---|---|---|
| P3 | El dueño del trámite es el **jefe inmediato**. | Se aplica en NO-FIT-003, en el texto para NO-PIT-001 y después en 001. |
| P6 | El inventario es **AssetTiger**. | Es el registro vivo de los principios 4.2 y 3.3. Falta confirmar qué módulos y campos se usan (ver NO-FIT-003, D6). |
| 5.3 | Al Gerente tampoco le convence la cláusula de cobro. | Se rediseña en NO-FIT-002. |
| 3.4 | NO-FME-046 es desconocido para IT. | Se deja de lado. Las excepciones se tramitan con NO-FIT-001 tipo MOD (ver NO-FIT-003). |
| D1 (003) | El acuse lo firman **todos**, incluidos los operadores de piso. | Aplicado en 003 y PIT-001. |
| D5 (003) | No se prohíbe conectar el celular a la PC. **Se prohíbe conectarlo a la red** sin autorización. | Aplicado. |
| 6.1 | En las estaciones compartidas firman **todos los que las comparten**. Por excepción se pueden asignar al gerente del área. | Aplicado en PIT-001 (sección H). El formato se resuelve en 002. |
| MOD | Al Gerente no le convence usar el 001 completo para un cambio. | Se plantea en 003 como D7. Se diseña en 001. |
| D2–D4, D8 (003) | Lleva resumen. Revisión semestral. No hay políticas corporativas. El equipo compartido se asigna al gerente por acuerdo con el Gerente de IT. | Aplicado. NO-FIT-003 queda cerrado, salvo D7. |
| D7 | El Gerente quiere ver alternativas; se inclina por un formato aparte. | `02-D7-alternativas-cambio-accesos.md` |
| D7 | **Alternativa B: NO-FIT-010 Solicitud de cambio de accesos.** 001 solo altas. 005 solo bajas (salida, despido, incapacidad, suspensión). Cambios de rol por 010. | Aplicado en 003 y PIT-001. Afecta F5-03 (el cambio de puesto sale del 005). |
| D9–D12, P4 (002) | Sin cobro. Sin denuncia. Sin celulares. Firma en papel. Equipo: tablet, laptop, desktop, docking y monitor. Sin rutas en los documentos. | Aplicado. NO-FIT-002 queda cerrado. Choca con F1-04 (catálogo del 001). |
| D13–D17, P7–P9, P15 (005) | Plazos sin "aviso tardío". Sin incapacidad. H: 90 días. Buzón compartido (personas que indique el jefe; por omisión, el jefe). China fuera; SAP vía SAP Administration. Videovigilancia la crean varias áreas. Sin gafetes (huella + sites). FortiClient vía ISP. | Aplicado. Queda D18 (vida del buzón compartido frente a 2 semanas de AD), P9b y P16. |
| P9b, P16, D18 (005) | SonicWall obsoleto. EasyConnect se pide al China IT team. Todas las eliminaciones a 30 días (H: sigue en 90). | NO-FIT-005 cerrado. Efecto: quitar SonicWall de NO-FIT-007 y de la definición de "Acceso remoto" en NO-PIT-001. |
| P2, FIORI, SAP | Hay ambiente de pruebas. FIORI es cuenta aparte; basta con marcarla. El Gerente quiere un buen formato de SAP llenado por el jefe en el alta, con copia de permisos. SAP Administration como puesto. | NO-FIT-001 con Anexo SAP y NO-FIT-010 propuestos. Abiertas D19–D26. |
