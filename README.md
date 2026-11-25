# Proceso civil: demandas, contestaciones, audiencia previa y vista

> Plugin de Claude Code `formularios-proceso-civil` · **186 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para el núcleo del pleito civil: demandas y contestaciones en el juicio ordinario y el verbal, reconvención, excepciones procesales, declinatoria, audiencia previa, vista y conclusiones. La prueba y los escritos de trámite tienen sus propios plugins.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 186 está al final):

- **Demandas, peticiones y solicitudes iniciales** (18). Por ejemplo: Demanda de juicio ordinario por intromisión ilegítima en el derecho al honor; Demanda de juicio ordinario para reivindicar un título nobiliario; Demanda de juicio verbal para rectificar hechos difundidos en un medio de comunicación.
- **Contestaciones, oposiciones y alegaciones** (28). Por ejemplo: Alegaciones frente a la solicitud de complemento de una resolución procesal; Contestación a la demanda alegando litispendencia internacional (artículo 29 Bruselas I bis); Oposición a la acumulación de procesos ante el mismo tribunal.
- **Estatutos, actas, certificaciones y escrituras** (5). Por ejemplo: Acta de audiencia al Ministerio Fiscal y a las partes sobre la falta de jurisdicción por inmunidad; Acta de otorgamiento de poder apud acta (artículo 23.3 LEC); Escritura de poder de miseria.
- **Comunicaciones, requerimientos y cartas** (22). Por ejemplo: Solicitud del demandado de suspender el plazo para contestar y reconvenir; Solicitud ex parte de continuar el proceso sin el demandado (artículo 22.2 Reglamento 2020-1784); Solicitud ex parte de declinatoria por sumisión a tribunales extranjeros (DIPr autónomo).
- **Escritos de trámite y otros** (113). Por ejemplo: Escrito de ampliación objetiva de la demanda; Incidente de nulidad de actuaciones por defecto de forma; Impugnación de la resolución que deniega la justicia gratuita, con reconocimiento excepcional.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Contestación a la demanda de juicio ordinario con reconvención»
   - «Demanda de juicio verbal en reclamación de cantidad»
   - «Declinatoria por falta de competencia territorial»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-proceso-civil:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-proceso-civil:escrito-ampliacion-objetiva-demanda-civ-0860`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 11.404 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-proceso-civil@formularios-proceso-civil`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-proceso-civil
/plugin install formularios-proceso-civil@formularios-proceso-civil
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-proceso-civil`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-proceso-civil/releases/latest/download/formularios-proceso-civil.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (186)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0860 | Escrito de ampliación objetiva de la demanda | `escrito-ampliacion-objetiva-demanda-civ-0860` |
| CIV-0862 | Demanda de juicio ordinario por intromisión ilegítima en el derecho al honor | `demanda-juicio-ordinario-intromision-ilegitima-derecho-civ-0862` |
| CIV-0863 | Demanda de juicio ordinario para reivindicar un título nobiliario | `demanda-juicio-ordinario-reivindicar-titulo-nobiliario-civ-0863` |
| CIV-0864 | Demanda de juicio verbal para rectificar hechos difundidos en un medio de comunicación | `demanda-juicio-verbal-rectificar-hechos-difundidos-civ-0864` |
| CIV-0865 | Demanda de juicio verbal para reivindicar la devolución de un bien mueble (ordenador personal) | `demanda-juicio-verbal-reivindicar-devolucion-bien-civ-0865` |
| CIV-0868 | Incidente de nulidad de actuaciones por defecto de forma | `incidente-nulidad-actuaciones-defecto-forma-civ-0868` |
| CIV-0872 | Alegaciones frente a la solicitud de complemento de una resolución procesal | `alegaciones-frente-solicitud-complemento-resolucion-civ-0872` |
| CIV-0875 | Demanda de juicio verbal para reclamar los gastos del sepelio | `demanda-juicio-verbal-reclamar-gastos-sepelio-civ-0875` |
| CIV-0876 | Impugnación de la resolución que deniega la justicia gratuita, con reconocimiento excepcional | `impugnacion-resolucion-deniega-justicia-gratuita-civ-0876` |
| CIV-0877 | Solicitud del demandado de suspender el plazo para contestar y reconvenir | `solicitud-demandado-suspender-plazo-contestar-civ-0877` |
| CIV-0878 | Solicitud ex parte de continuar el proceso sin el demandado (artículo 22.2 Reglamento 2020-1784) | `solicitud-ex-parte-continuar-proceso-sin-demandado-civ-0878` |
| CIV-0879 | Escrito proponiendo la declinatoria por falta de jurisdicción debida a inmunidad de jurisdicción | `escrito-proponiendo-declinatoria-falta-jurisdiccion-civ-0879` |
| CIV-0880 | Solicitud ex parte de declinatoria por sumisión a tribunales extranjeros (DIPr autónomo) | `solicitud-ex-parte-declinatoria-sumision-tribunales-civ-0880` |
| CIV-0881 | Solicitud ex parte de declinatoria por falta de competencia internacional (Bruselas I refundido) | `solicitud-ex-parte-declinatoria-falta-competencia-civ-0881` |
| CIV-0882 | Contestación a la demanda alegando litispendencia internacional (artículo 29 Bruselas I bis) | `contestacion-demanda-alegando-litispendencia-civ-0882` |
| CIV-0883 | Acta de audiencia al Ministerio Fiscal y a las partes sobre la falta de jurisdicción por inmunidad | `acta-audiencia-ministerio-fiscal-partes-sobre-falta-civ-0883` |
| CIV-0885 | Declaración jurada para obtener la habilitación ante el Tribunal Eclesiástico | `declaracion-jurada-obtener-habilitacion-ante-tribunal-civ-0885` |
| CIV-0886 | Acta de otorgamiento de poder apud acta (artículo 23.3 LEC) | `acta-otorgamiento-poder-apud-acta-articulo-23-3-lec-civ-0886` |
| CIV-0890 | Escrito del demandante indicando el tribunal de remisión de los autos ante varios fueros electivos | `escrito-demandante-indicando-tribunal-remision-autos-civ-0890` |
| CIV-0897 | Escrito del demandado pidiendo abogado y procurador de oficio | `escrito-demandado-pidiendo-abogado-procurador-oficio-civ-0897` |
| CIV-0901 | Otrosí de demanda pidiendo que el procurador practique los actos de comunicación | `otrosi-demanda-pidiendo-procurador-practique-actos-civ-0901` |
| CIV-0904 | Oposición a la acumulación de procesos ante el mismo tribunal | `oposicion-acumulacion-procesos-ante-mismo-tribunal-civ-0904` |
| CIV-0905 | Oposición a la acumulación de procesos que se tramitan ante tribunales distintos | `oposicion-acumulacion-procesos-tramitan-ante-civ-0905` |
| CIV-0907 | Escrito que aporta una resolución dictada o notificada después del trámite de conclusiones | `escrito-aporta-resolucion-dictada-notificada-despues-civ-0907` |
| CIV-0911 | Escritura de poder de miseria | `escritura-poder-miseria-civ-0911` |
| CIV-0913 | Minuta del procurador con derechos, gastos y suplidos | `minuta-procurador-derechos-gastos-suplidos-civ-0913` |
| CIV-0914 | Escrito del demandado que comparece y formula reconvención en juicio verbal | `escrito-demandado-comparece-formula-reconvencion-civ-0914` |
| CIV-0915 | Solicitud del demandado en juicio verbal de intervención de tercero y contestación a esa solicitud | `solicitud-demandado-juicio-verbal-intervencion-tercero-civ-0915` |
| CIV-0916 | Escrito del demandado que opone compensación por relaciones comerciales con el actor en verbal | `escrito-demandado-opone-compensacion-relaciones-civ-0916` |
| CIV-0920 | Declinatoria por falta de competencia territorial propuesta por el demandado en juicio verbal | `declinatoria-falta-competencia-territorial-propuesta-civ-0920` |
| CIV-0921 | Declinatoria del demandado en juicio verbal por falta de competencia territorial del tribunal | `declinatoria-demandado-juicio-verbal-falta-competencia-civ-0921` |
| CIV-0923 | Demanda de juicio verbal de rectificación de hechos con domicilios para notificaciones | `demanda-juicio-verbal-rectificacion-hechos-domicilios-civ-0923` |
| CIV-0926 | Escrito de contestación a la ampliación de hechos | `escrito-contestacion-ampliacion-hechos-civ-0926` |
| CIV-0927 | Cuestión incidental de previo pronunciamiento por falta de capacidad del demandante | `cuestion-incidental-previo-pronunciamiento-falta-civ-0927` |
| CIV-0928 | Contestación a la cuestión incidental de previo pronunciamiento por falta de capacidad del actor | `contestacion-cuestion-incidental-previo-civ-0928` |
| CIV-0936 | Proposición de reproducción de palabra, sonido e imagen con medio instrumental | `proposicion-reproduccion-palabra-sonido-e-imagen-medio-civ-0936` |
| CIV-0940 | Escrito de ampliación de hechos nuevos posteriores a la audiencia previa | `escrito-ampliacion-hechos-nuevos-posteriores-audiencia-civ-0940` |
| CIV-0946 | Conclusiones orales de la parte en el juicio ordinario | `conclusiones-orales-parte-juicio-ordinario-civ-0946` |
| CIV-0947 | Petición oral de diligencias finales durante el trámite de conclusiones | `peticion-oral-diligencias-finales-durante-tramite-civ-0947` |
| CIV-0948 | Contestación a la demanda de juicio ordinario con oposición por disconformidad en los hechos | `contestacion-demanda-juicio-ordinario-oposicion-civ-0948` |
| CIV-0949 | Contestación a la demanda ordinaria conforme en los hechos y opuesta en los fundamentos de derecho | `contestacion-demanda-ordinaria-conforme-hechos-opuesta-civ-0949` |
| CIV-0950 | Demanda de juicio ordinario de tutela del derecho fundamental al secreto de las comunicaciones | `demanda-juicio-ordinario-tutela-derecho-fundamental-civ-0950` |
| CIV-0951 | Con reconvención contra el demandante (contestación) | `reconvencion-contra-demandante-contestacion-civ-0951` |
| CIV-0953 | Impugnación del informe elaborado por detective privado | `impugnacion-informe-elaborado-detective-privado-civ-0953` |
| CIV-0955 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone defectos de capacidad | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0955` |
| CIV-0956 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone defectos de representación | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0956` |
| CIV-0957 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone litispendencia | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0957` |
| CIV-0958 | Hechos y fundamentos de la contestación ordinaria que se opone a la acumulación de acciones | `hechos-fundamentos-contestacion-ordinaria-opone-civ-0958` |
| CIV-0959 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone defectos de la demanda | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0959` |
| CIV-0960 | Hechos y fundamentos de la contestación ordinaria que opone falta de litisconsorcio necesario | `hechos-fundamentos-contestacion-ordinaria-opone-falta-civ-0960` |
| CIV-0961 | Petición del demandado en la audiencia previa de que el juez revise de oficio su competencia | `peticion-demandado-audiencia-previa-juez-revise-oficio-civ-0961` |
| CIV-0962 | Intervención del actor que integra voluntariamente la litis en la audiencia previa, y resolución | `intervencion-actor-integra-voluntariamente-litis-civ-0962` |
| CIV-0963 | Audiencia previa sobre inadecuación de procedimiento por la cuantía y paso a juicio verbal | `audiencia-previa-sobre-inadecuacion-procedimiento-civ-0963` |
| CIV-0964 | Oposición del demandante a la excepción de litispendencia o cosa juzgada, con resolución y protesta | `oposicion-demandante-excepcion-litispendencia-cosa-civ-0964` |
| CIV-0965 | Planteamiento por el actor de la falta de representación del demandado en la audiencia previa | `planteamiento-actor-falta-representacion-demandado-civ-0965` |
| CIV-0966 | Hechos y fundamentos de la contestación ordinaria que opone inadecuación de procedimiento | `hechos-fundamentos-contestacion-ordinaria-opone-civ-0966` |
| CIV-0967 | Oposición del demandante a la excepción de falta de litisconsorcio pasivo necesario | `oposicion-demandante-excepcion-falta-litisconsorcio-civ-0967` |
| CIV-0968 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone cosa juzgada | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0968` |
| CIV-0969 | Alegación en la audiencia previa de falta de capacidad del actor por carecer de personalidad | `alegacion-audiencia-previa-falta-capacidad-actor-civ-0969` |
| CIV-0970 | Alegaciones complementarias del demandante en la audiencia previa, oposición y resolución | `alegaciones-complementarias-demandante-audiencia-civ-0970` |
| CIV-0973 | Intervención del demandante que añade una petición en la audiencia previa, con oposición y protesta | `intervencion-demandante-anade-peticion-audiencia-civ-0973` |
| CIV-0975 | Intervención en la audiencia previa sobre inadecuación de procedimiento por razón de la materia | `intervencion-audiencia-previa-sobre-inadecuacion-civ-0975` |
| CIV-0977 | Alegación del demandante de un hecho de nueva noticia en la audiencia previa, y oposición | `alegacion-demandante-hecho-nueva-noticia-audiencia-civ-0977` |
| CIV-0978 | Intervención en la audiencia previa sobre defectos de la demanda y aclaraciones | `intervencion-audiencia-previa-sobre-defectos-demanda-civ-0978` |
| CIV-0982 | Otrosí de la demanda de persona jurídica exenta que no aporta justificante de la tasa judicial | `otrosi-demanda-persona-juridica-exenta-no-aporta-civ-0982` |
| CIV-0984 | Otrosí de la demanda que fija la cuantía en la pretensión de condena a entregar un inmueble | `otrosi-demanda-fija-cuantia-pretension-condena-civ-0984` |
| CIV-0985 | Contestación a la reconvención formulada por quien no es demandante, oponiendo falta de legitimación | `contestacion-reconvencion-formulada-quien-no-es-civ-0985` |
| CIV-0986 | Contestación del demandante a la reconvención oponiendo excepciones procesales | `contestacion-demandante-reconvencion-oponiendo-civ-0986` |
| CIV-0987 | Contestación del demandante a la reconvención oponiendo excepciones de fondo | `contestacion-demandante-reconvencion-oponiendo-civ-0987` |
| CIV-0988 | Otrosí de la demanda que fija la cuantía en una reclamación de cantidad dineraria | `otrosi-demanda-fija-cuantia-reclamacion-cantidad-civ-0988` |
| CIV-0989 | Comparecencia ante el tribunal competente tras estimarse la declinatoria, sin conocerlo aún | `comparecencia-ante-tribunal-competente-tras-estimarse-civ-0989` |
| CIV-0990 | Declinatoria por corresponder el asunto a los tribunales de otro país | `declinatoria-corresponder-asunto-tribunales-otro-pais-civ-0990` |
| CIV-0991 | Contestación del demandante a la declinatoria aportando documentos | `contestacion-demandante-declinatoria-aportando-civ-0991` |
| CIV-0992 | Demanda con acumulación de acciones | `demanda-acumulacion-acciones-civ-0992` |
| CIV-0993 | Declinatoria por falta de competencia territorial alegando la nulidad de la sumisión expresa | `declinatoria-falta-competencia-territorial-alegando-civ-0993` |
| CIV-0995 | Comparecencia ante el tribunal competente tras estimarse la declinatoria, ya conocido | `comparecencia-ante-tribunal-competente-tras-estimarse-civ-0995` |
| CIV-0996 | Solicitud del demandante de justicia gratuita ante la comisión de asistencia jurídica gratuita | `solicitud-demandante-justicia-gratuita-ante-comision-civ-0996` |
| CIV-1002 | Demanda general de juicio verbal por razón de la cuantía | `demanda-general-juicio-verbal-razon-cuantia-civ-1002` |
| CIV-1003 | Escrito que subsana defectos de la demanda en la determinación de la cuantía | `escrito-subsana-defectos-demanda-determinacion-cuantia-civ-1003` |
| CIV-1006 | Encabezamiento de demanda con abogado y procurador del turno de oficio en nombre de persona física | `encabezamiento-demanda-abogado-procurador-turno-oficio-civ-1006` |
| CIV-1007 | Demanda de declaración de error judicial (art. 293 LOPJ) | `demanda-declaracion-error-judicial-art-293-lopj-civ-1007` |
| CIV-1009 | Notificación y traslado de demanda de juicio ordinario según el Convenio de La Haya de 1965 | `notificacion-traslado-demanda-juicio-ordinario-segun-civ-1009` |
| CIV-1010 | Solicitud de sucesión procesal por fallecimiento del demandante | `solicitud-sucesion-procesal-fallecimiento-demandante-civ-1010` |
| CIV-1011 | Solicitud de notificación personal de la sentencia al demandado condenado en rebeldía (art. 497 LEC) | `solicitud-notificacion-personal-sentencia-demandado-civ-1011` |
| CIV-1013 | Escrito del demandado de oposición al desistimiento (art. 20.3 LEC) | `escrito-demandado-oposicion-desistimiento-art-20-3-lec-civ-1013` |
| CIV-1016 | Impugnación del reparto de la demanda con solicitud de nulidad y remisión al órgano competente | `impugnacion-reparto-demanda-solicitud-nulidad-remision-civ-1016` |
| CIV-1019 | Demanda de juicio ordinario con acumulación subjetiva de acciones por daños de circulación | `demanda-juicio-ordinario-acumulacion-subjetiva-civ-1019` |
| CIV-1020 | Demanda de juicio verbal de desahucio por falta de pago con acumulación de reclamación de cantidades | `demanda-juicio-verbal-desahucio-falta-pago-acumulacion-civ-1020` |
| CIV-1021 | Demanda de juicio ordinario que acumula reclamación de cantidad y de daños y perjuicios | `demanda-juicio-ordinario-acumula-reclamacion-cantidad-civ-1021` |
| CIV-1023 | Solicitud del demandado de que se comunique el proceso a los sucesores del demandante fallecido | `solicitud-demandado-comunique-proceso-sucesores-civ-1023` |
| CIV-1024 | Comunicación de repudiación de herencia por parientes del demandado contra la sucesión procesal | `comunicacion-repudiacion-herencia-parientes-demandado-civ-1024` |
| CIV-1025 | Solicitud del actor de que se comunique el juicio a los sucesores del demandado fallecido | `solicitud-actor-comunique-juicio-sucesores-demandado-civ-1025` |
| CIV-1026 | Oposición del demandado al desistimiento por incomparecencia de los sucesores del actor fallecido | `oposicion-demandado-desistimiento-incomparecencia-civ-1026` |
| CIV-1028 | Oposición de los coejecutados a que el deudor solidario suceda como ejecutante en el proceso | `oposicion-coejecutados-deudor-solidario-suceda-como-civ-1028` |
| CIV-1029 | Otrosí de la contestación que pide llamar a un tercero al juicio ordinario | `otrosi-contestacion-pide-llamar-tercero-juicio-civ-1029` |
| CIV-1030 | Solicitud de llamada a tercero con suspensión del plazo para contestar la demanda | `solicitud-llamada-tercero-suspension-plazo-contestar-civ-1030` |
| CIV-1031 | Escrito del demandante que identifica a un tercero para notificarle la pendencia del juicio verbal | `escrito-demandante-identifica-tercero-notificarle-civ-1031` |
| CIV-1032 | Escrito del actor que manifiesta desconocer a los herederos del demandado fallecido y su paradero | `escrito-actor-manifiesta-desconocer-herederos-civ-1032` |
| CIV-1033 | Otrosí del demandante que pide llamar a un tercero sin la condición de demandado | `otrosi-demandante-pide-llamar-tercero-sin-condicion-civ-1033` |
| CIV-1035 | Solicitud de intervención adhesiva de tercero a favor del demandado en juicio ordinario | `solicitud-intervencion-adhesiva-tercero-favor-civ-1035` |
| CIV-1042 | Demanda de juicio ordinario con acumulación de pretensiones incompatibles | `demanda-juicio-ordinario-acumulacion-pretensiones-civ-1042` |
| CIV-1046 | Oposición a la causa de recusación del LAJ propuesta por la parte contraria | `oposicion-causa-recusacion-laj-propuesta-parte-civ-1046` |
| CIV-1050 | Adhesión a la recusación del LAJ propuesta por la parte contraria | `adhesion-recusacion-laj-propuesta-parte-contraria-civ-1050` |
| CIV-1051 | Adhesión a la causa de recusación propuesta por la contraparte contra el juez | `adhesion-causa-recusacion-propuesta-contraparte-contra-civ-1051` |
| CIV-1053 | Solicitud del demandado con justicia gratuita de abogado y procurador de oficio en desahucio verbal | `solicitud-demandado-justicia-gratuita-abogado-civ-1053` |
| CIV-1059 | Comunicación del demandado de que comparecerá en juicio verbal con procurador y abogado | `comunicacion-demandado-comparecera-juicio-verbal-civ-1059` |
| CIV-1062 | Otrosí de la demanda de juicio verbal que anuncia el uso de abogado y procurador no preceptivos | `otrosi-demanda-juicio-verbal-anuncia-uso-abogado-civ-1062` |
| CIV-1063 | Procurador de su renuncia a la representación del poderdante (comunicación) | `procurador-renuncia-representacion-poderdante-civ-1063` |
| CIV-1066 | Manifestación del demandante de satisfacción extraprocesal del derecho de reparación civil | `manifestacion-demandante-satisfaccion-extraprocesal-civ-1066` |
| CIV-1067 | Solicitud del demandante de terminar el proceso por satisfacción extraprocesal (art. 22 LEC) | `solicitud-demandante-terminar-proceso-satisfaccion-civ-1067` |
| CIV-1068 | Personación y allanamiento total del demandado en juicio ordinario | `personacion-allanamiento-total-demandado-juicio-civ-1068` |
| CIV-1069 | Solicitud del demandado de terminar el proceso por satisfacción extraprocesal de las pretensiones | `solicitud-demandado-terminar-proceso-satisfaccion-civ-1069` |
| CIV-1070 | Solicitud del actor de que se dicte auto de allanamiento parcial pedido por el demandado | `solicitud-actor-dicte-auto-allanamiento-parcial-pedido-civ-1070` |
| CIV-1071 | Personación y allanamiento total del demandado en juicio verbal | `personacion-allanamiento-total-demandado-juicio-verbal-civ-1071` |
| CIV-1072 | Desistimiento del actor sin traslado al demandado aún no emplazado | `desistimiento-actor-sin-traslado-demandado-aun-no-civ-1072` |
| CIV-1075 | Oposición del demandado al desistimiento con petición de costas, antes de contestar a la demanda | `oposicion-demandado-desistimiento-peticion-costas-civ-1075` |
| CIV-1076 | Desistimiento del actor tras la contestación con traslado al demandado y petición de no pagar costas | `desistimiento-actor-tras-contestacion-traslado-civ-1076` |
| CIV-1077 | Desistimiento del actor con traslado al demandado ya emplazado o citado | `desistimiento-actor-traslado-demandado-ya-emplazado-civ-1077` |
| CIV-1079 | Acta de apoderamiento apud acta a procurador antes de presentar la demanda | `acta-apoderamiento-apud-acta-procurador-antes-civ-1079` |
| CIV-1080 | Encabezamiento de demanda con procurador apoderado apud acta en comparecencia | `encabezamiento-demanda-procurador-apoderado-apud-acta-civ-1080` |
| CIV-1081 | Encabezamiento de demanda con procurador en nombre del tutor de un menor | `encabezamiento-demanda-procurador-nombre-tutor-menor-civ-1081` |
| CIV-1082 | Otrosí de demanda que pide emplazar al demandado domiciliado en el extranjero (Convenio de La Haya) | `otrosi-demanda-pide-emplazar-demandado-domiciliado-civ-1082` |
| CIV-1083 | Otrosí de la demanda que pide una medida urgente antes del reparto | `otrosi-demanda-pide-medida-urgente-antes-reparto-civ-1083` |
| CIV-1084 | Vista en segunda instancia con personación de procurador habilitado (solicitud) | `vista-segunda-instancia-personacion-procurador-civ-1084` |
| CIV-1085 | Solicitud de nuevo señalamiento de vista por imposibilidad de asistir el representante de la actora | `solicitud-nuevo-senalamiento-vista-imposibilidad-civ-1085` |
| CIV-1086 | Solicitud de suspensión de la vista señalada por acuerdo de las partes (art. 188.1.3 LEC) | `solicitud-suspension-vista-senalada-acuerdo-partes-art-civ-1086` |
| CIV-1087 | Escrito del actor que desconoce otro domicilio del demandado en el monitorio y pide oficios | `escrito-actor-desconoce-otro-domicilio-demandado-civ-1087` |
| CIV-1089 | Escrito anunciando que se usará una lengua cooficial en la vista oral | `escrito-anunciando-usara-lengua-cooficial-vista-oral-civ-1089` |
| CIV-1090 | Escrito pidiendo copia de las grabaciones originales de la vista | `escrito-pidiendo-copia-grabaciones-originales-vista-civ-1090` |
| CIV-1092 | Escrito pidiendo suspender la vista por coincidencia de señalamientos del letrado | `escrito-pidiendo-suspender-vista-coincidencia-civ-1092` |
| CIV-1101 | Escrito aportando un documento posterior a la demanda, a la contestación o a la audiencia previa | `escrito-aportando-documento-posterior-demanda-civ-1101` |
| CIV-1102 | Escrito de allanamiento total del demandado en juicio ordinario | `escrito-allanamiento-total-demandado-juicio-ordinario-civ-1102` |
| CIV-1103 | Escrito de declinatoria territorial ante el tribunal del domicilio del demandado (juicio verbal) | `escrito-declinatoria-territorial-ante-tribunal-civ-1103` |
| CIV-1104 | Escrito del actor que dirige la demanda contra los litisconsortes señalados por el demandado | `escrito-actor-dirige-demanda-contra-litisconsortes-civ-1104` |
| CIV-1105 | Demanda del procurador contra su poderdante para reclamar provisión de fondos | `demanda-procurador-contra-poderdante-reclamar-civ-1105` |
| CIV-1107 | Escrito del actor pidiendo contestar a la alegación de nulidad del negocio hecha por el demandado | `escrito-actor-pidiendo-contestar-alegacion-nulidad-civ-1107` |
| CIV-1112 | Escrito del demandante que se opone a la nulidad de actuaciones por copia inexacta | `escrito-demandante-opone-nulidad-actuaciones-copia-civ-1112` |
| CIV-1114 | Contestación a la demanda con oposición a la acumulación de acciones hecha en la ampliación | `contestacion-demanda-oposicion-acumulacion-acciones-civ-1114` |
| CIV-1116 | Escrito de ampliación de hechos de la demanda por cambio de liquidador, con documentos | `escrito-ampliacion-hechos-demanda-cambio-liquidador-civ-1116` |
| CIV-1119 | Escrito de ampliación subjetiva de la demanda | `escrito-ampliacion-subjetiva-demanda-civ-1119` |
| CIV-1120 | Escrito general de contestación a la demanda y oposición | `escrito-general-contestacion-demanda-oposicion-civ-1120` |
| CIV-1121 | Demanda genérica de juicio ordinario | `demanda-generica-juicio-ordinario-civ-1121` |
| CIV-1123 | Escrito aportando sentencia o resolución de fecha no anterior a las conclusiones (art. 271.2 LEC) | `escrito-aportando-sentencia-resolucion-fecha-no-civ-1123` |
| CIV-1126 | Alegaciones de la contraparte sobre una sentencia aportada tras las conclusiones (art. 271.2 LEC) | `alegaciones-contraparte-sobre-sentencia-aportada-tras-civ-1126` |
| CIV-1127 | Escrito aportando documento anterior a la demanda o contestación del que no se tenía conocimiento | `escrito-aportando-documento-anterior-demanda-civ-1127` |
| CIV-1133 | Contestación a la demanda con oposición a la acumulación de acciones planteada en la propia demanda | `contestacion-demanda-oposicion-acumulacion-acciones-civ-1133` |
| CIV-1134 | Escrito general del demandante que contesta a la reconvención | `escrito-general-demandante-contesta-reconvencion-civ-1134` |
| CIV-1135 | Escrito general de contestación a la demanda con reconvención | `escrito-general-contestacion-demanda-reconvencion-civ-1135` |
| CIV-1137 | Contestación a la demanda alegando compensación de deudas en una compraventa de mercancías | `contestacion-demanda-alegando-compensacion-deudas-civ-1137` |
| CIV-1138 | Escrito de un sujeto no demandante que contesta a la reconvención | `escrito-sujeto-no-demandante-contesta-reconvencion-civ-1138` |
| CIV-1139 | Escrito de contestación a la demanda que se allana parcialmente a las pretensiones del actor | `escrito-contestacion-demanda-allana-parcialmente-civ-1139` |
| CIV-1143 | Escrito pidiendo que el juicio se celebre en dos meses desde la audiencia previa (art. 429.3 LEC) | `escrito-pidiendo-juicio-celebre-dos-meses-desde-civ-1143` |
| CIV-2689 | Demanda de jura de cuentas del procurador contra su poderdante | `demanda-jura-cuentas-procurador-contra-poderdante-civ-2689` |
| CIV-2695 | Declinatoria del Abogado del Estado por falta de competencia territorial | `declinatoria-abogado-estado-falta-competencia-civ-2695` |
| CIV-2698 | Escrito del demandado que pide suspender el verbal por prejudicialidad administrativo-laboral | `escrito-demandado-pide-suspender-verbal-civ-2698` |
| CIV-2700 | Declinatoria por falta de jurisdicción civil a favor del orden contencioso-administrativo | `declinatoria-falta-jurisdiccion-civil-favor-orden-civ-2700` |
| CIV-2703 | Escrito de alegaciones contra la declinatoria por falta de competencia territorial | `escrito-alegaciones-contra-declinatoria-falta-civ-2703` |
| CIV-2704 | Escrito que contesta a la declinatoria de competencia internacional en juicio ordinario | `escrito-contesta-declinatoria-competencia-civ-2704` |
| CIV-2705 | Declinatoria por falta de competencia territorial planteada en juicio ordinario | `declinatoria-falta-competencia-territorial-planteada-civ-2705` |
| CIV-2709 | Contestación del demandante a la reconvención en proceso de separación, nulidad o divorcio | `contestacion-demandante-reconvencion-proceso-civ-2709` |
| CIV-2711 | Escrito del demandante que admite la falta de competencia territorial del tribunal | `escrito-demandante-admite-falta-competencia-civ-2711` |
| CIV-2714 | Personación de los herederos del demandante fallecido en el juicio de reclamación de paternidad | `personacion-herederos-demandante-fallecido-juicio-civ-2714` |
| CIV-2716 | Escrito del demandante que pide seguir el juicio de paternidad contra los herederos del demandado | `escrito-demandante-pide-seguir-juicio-paternidad-civ-2716` |
| CIV-2717 | Escrito de parte que pide suspender la vista y fijar un nuevo señalamiento | `escrito-parte-pide-suspender-vista-fijar-nuevo-civ-2717` |
| CIV-2725 | Escrito del demandado que pide oír a una persona allegada en el proceso de medidas de apoyo | `escrito-demandado-pide-oir-persona-allegada-proceso-civ-2725` |
| CIV-2730 | Escrito del demandante que elige el tribunal competente tras declararse la incompetencia territorial | `escrito-demandante-elige-tribunal-competente-tras-civ-2730` |
| CIV-2731 | Petición de nuevo señalamiento de la vista por enfermedad del abogado | `peticion-nuevo-senalamiento-vista-enfermedad-abogado-civ-2731` |
| CIV-2732 | Petición de nuevo señalamiento de la vista por coincidir con otro señalamiento del abogado | `peticion-nuevo-senalamiento-vista-coincidir-otro-civ-2732` |
| CIV-2733 | Escrito del demandante que defiende la competencia territorial del tribunal | `escrito-demandante-defiende-competencia-territorial-civ-2733` |
| CIV-2734 | Escrito del demandante que subsana la falta de certificación del matrimonio antes de la admisión | `escrito-demandante-subsana-falta-certificacion-civ-2734` |
| CIV-2735 | Escrito de personación del demandado en un juicio verbal civil | `escrito-personacion-demandado-juicio-verbal-civil-civ-2735` |
| CIV-2736 | Petición del actor para ampliar la demanda a nuevos demandados antes de la contestación | `peticion-actor-ampliar-demanda-nuevos-demandados-antes-civ-2736` |
| CIV-2737 | Escrito de desistimiento sin costas frente a un codemandado que lo acepta | `escrito-desistimiento-sin-costas-frente-codemandado-lo-civ-2737` |
| CIV-2738 | Petición del demandado para acumular dos juicios ordinarios por el mismo accidente de tráfico | `peticion-demandado-acumular-dos-juicios-ordinarios-civ-2738` |
| CIV-2740 | Declinatoria de jurisdicción en juicio verbal a favor del orden contencioso-administrativo | `declinatoria-jurisdiccion-juicio-verbal-favor-orden-civ-2740` |
| CIV-2741 | Declinatoria de jurisdicción en juicio ordinario a favor del orden contencioso-administrativo | `declinatoria-jurisdiccion-juicio-ordinario-favor-orden-civ-2741` |
| CIV-2748 | Cuenta del procurador fallecido presentada por sus herederos contra el poderdante que no pagó | `cuenta-procurador-fallecido-presentada-herederos-civ-2748` |
| CIV-2749 | Escritura que revoca un poder para pleitos otorgado anteriormente | `escritura-revoca-poder-pleitos-otorgado-anteriormente-civ-2749` |
| CIV-2755 | Escrito de declinatoria por falta de competencia | `escrito-declinatoria-falta-competencia-civ-2755` |
| CIV-2764 | Contestación a la demanda con reconvención en un pleito de tráfico | `contestacion-demanda-reconvencion-pleito-trafico-civ-2764` |
| CIV-2765 | Escrito general de contestación a la demanda con posibles excepciones procesales | `escrito-general-contestacion-demanda-posibles-civ-2765` |
| CIV-2766 | Escrito del perjudicado ya indemnizado que renuncia a las acciones ejercitadas en la demanda | `escrito-perjudicado-ya-indemnizado-renuncia-acciones-civ-2766` |
| CIV-2768 | Demanda civil con petición de emplazamiento del demandado que reside en el extranjero | `demanda-civil-peticion-emplazamiento-demandado-reside-civ-2768` |
| CIV-2769 | Oposición a la declinatoria por falta de jurisdicción basada en la inmunidad de jurisdicción | `oposicion-declinatoria-falta-jurisdiccion-basada-civ-2769` |
| CIV-2770 | Contestación a la demanda que plantea la excepción de conexidad del Reglamento Bruselas I bis | `contestacion-demanda-plantea-excepcion-conexidad-civ-2770` |
| CIV-2771 | Escrito que pide el emplazamiento por edictos del demandado de domicilio desconocido | `escrito-pide-emplazamiento-edictos-demandado-domicilio-civ-2771` |

## Privacidad

Ver `PRIVACY.md`.
