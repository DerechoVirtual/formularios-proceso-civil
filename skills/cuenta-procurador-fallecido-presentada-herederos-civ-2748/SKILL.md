---
name: cuenta-procurador-fallecido-presentada-herederos-civ-2748
description: "Cuenta del procurador fallecido presentada por sus herederos contra el poderdante que no pagó. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Cuenta del procurador fallecido presentada por sus herederos contra el poderdante que no pagó

> Formulario **CIV-2748** del plugin **Proceso civil: demandas, contestaciones, audiencia previa y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 25-11-2026.

## Qué es

Escrito de los herederos del que fuera procurador en un procedimiento civil (ordinario, verbal o especial), acreditado su condición mediante declaración de herederos y presentando cuenta detallada y justificada de las cantidades debidas y no satisfechas al causante.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Cuenta del procurador fallecido presentada por sus herederos contra el poderdante que no pagó» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Cuenta del procurador fallecido presentada por sus herederos contra el poderdante que no pagó” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:cuenta-procurador-fallecido-presentada-herederos-civ-2748`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, audiencia previa y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DESCRIBIR
- [ ] SEDE

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El art. 34 de la LEC regula el que había venido siendo denominado en la práctica forense procedimiento de "jura de cuentas". Así, el Procurador que pretenda reclamar de su poderdante moroso las cantidades que éste le adeude por sus derechos y gastos que hubiere suplido, presentará cuenta detallada y justificada, asegurando (no es ya necesario el solemne juramento) que le son debidas y no han sido satisfechas. El Letrado de la Administración de Justicia, una vez presentada la cuenta, requerirá acto seguido al deudor moroso para que pague la suma debida con las costas, en el plazo de diez días, con expreso apercibimiento de apremio. En ese mismo plazo, podrá el poderdante impugnar la cuenta. La vigente LEC ha venido a introducir la posibilidad de una audiencia previa al poderdante a fin de que el mismo pueda aducir lo que a su derecho convenga, antes de proceder al correspondiente apremio al deudor moroso. Esta modificación introducida en la vigente LEC, con respecto a su antecedente legislativo, sin duda no es ajena a la doctrina establecida por el Tribunal Constitucional en el sentido de que ya en el procedimiento de jura de cuentas previsto en la legislación anterior, el requerimiento de pago al deudor había de llevarse a cabo de forma que no impidiera a éste formular las alegaciones pertinentes. En este sentido, por ejemplo, STC 12/1997 de 27 de enero de 1997.

Así pues, si en el plazo señalado de diez días, el poderdante no paga ni impugna la cuenta, se procederá a despachar ejecución por la cantidad contenida en aquélla más las costas previsibles del incidente. Por el contrario, si el poderdante impugna la cuenta, --y ha de entenderse, naturalmente, que dispone no sólo de la posibilidad de impugnar partidas concretas, sino también, incluso de forma esencial, de la de aducir un posible pago o plus petición--, el Letrado de la Administración de Justicia resolverá por decreto, examinando la cuenta y las actuaciones procesales, pero sin recibir el incidente a prueba, en el plazo de diez días y, para el caso de que estime alguna cantidad como debida, se procederá a la vía de apremio si no se satisficiere en el plazo de cinco días a contar de la notificación de este auto. Este decreto y el auto que resuelva el recurso de revisión no prejuzgarán, ni siquiera parcialmente, la sentencia que pudiera recaer en juicio declarativo posterior, sin que el decreto (en su caso, el auto) dictado en este procedimiento especial goce de los efectos de la cosa juzgada en ningún sentido, pudiendo ser, incluso, en el procedimiento posterior revisados los pronunciamientos que se contengan en el mismo.

Por otro lado, y como consecuencia de una enmienda aprobada en la Cámara Alta, se estableció que el mismo derecho que los Procuradores tendrán sus herederos, respecto de los derechos de esta naturaleza en que les sucedieren, despejando con ello cualquier duda al respecto.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
