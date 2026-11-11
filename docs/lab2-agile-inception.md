# Laboratorio 2: Agile Inception del sistema de residuos

**Proyecto:** EcoRuta Cusco: sistema de gestión de recolección de residuos sólidos
**Autora:** Gisel Dayana Farfan Gomez
**Curso:** Ingeniería de Software I

---

## 1. Lista de stakeholders

| Stakeholder | Rol en el sistema | Intereses / expectativas | Influencia | Interés |
|---|---|---|---|---|
| **Municipalidad** (Gerencia de Medio Ambiente / Limpieza Pública) | Cliente y patrocinador. Planifica rutas, horarios y supervisa el servicio | Reducir costos operativos, mejorar la cobertura, tener datos para tomar decisiones y cumplir la normativa ambiental | Alta | Alto |
| **Ciudadanos** | Usuarios finales. Consultan horarios, reciben alertas y reportan incidencias | Saber cuándo pasa el camión, que no se acumule basura en las calles y poder reportar problemas fácilmente | Media | Alto |
| **Operadores de camiones** (choferes y ayudantes) | Usuarios operativos. Siguen las rutas asignadas y registran el avance | Tener rutas claras, una app sencilla y menos reclamos de vecinos | Baja | Medio |
| Supervisores de limpieza pública | Monitorean las rutas en tiempo real y atienden incidencias | Visibilidad de la flota y capacidad de reasignar rutas | Media | Alto |
| Área de TI municipal | Despliega y mantiene el sistema | Que el sistema sea fácil de mantener y seguro | Media | Medio |
| Recicladores formalizados / asociaciones | Recogen residuos reciclables segregados | Acceso a puntos y horarios de reciclaje | Baja | Medio |
| Ministerio del Ambiente / ente fiscalizador | Regulador | Cumplimiento de la Ley de Gestión Integral de Residuos Sólidos (D.L. 1278) | Alta | Bajo |

**Prioridad de gestión:**
- **Gestionar de cerca:** Municipalidad y supervisores.
- **Mantener informados:** ciudadanos, operadores y recicladores.
- **Mantener satisfecho:** ente regulador.

---

## 2. Documento de visión

### 2.1 Visión (plantilla del laboratorio)

- **Para:** la Municipalidad de Cusco y los vecinos del distrito
- **El sistema:** EcoRuta Cusco, una plataforma web y móvil de gestión de recolección de residuos
- **Que permite:** planificar y monitorear en tiempo real las rutas de los camiones recolectores, informar a los ciudadanos los horarios de recojo y recibir reportes de acumulación de basura
- **A diferencia de:** la gestión actual basada en horarios fijos, comunicación informal y sin seguimiento de la flota, que provoca recojos perdidos y puntos críticos de basura

### 2.2 Visión extendida (formato Geoffrey Moore)

> **Para** la municipalidad y los ciudadanos del distrito,
> **que necesitan** un servicio de recolección de residuos puntual, predecible y transparente,
> **EcoRuta Cusco es** una plataforma web y móvil de gestión de recolección
> **que** permite planificar rutas, seguir los camiones por GPS, notificar a los vecinos y atender reportes ciudadanos.
> **A diferencia de** la gestión manual actual sin información en tiempo real,
> **nuestro producto** conecta a la municipalidad, los operadores y los ciudadanos en un solo sistema basado en datos.

### 2.3 Objetivos del proyecto

1. Reducir los recojos no realizados o fuera de horario.
2. Informar a los ciudadanos con anticipación sobre el paso del camión.
3. Dar a la municipalidad visibilidad en tiempo real de la flota.
4. Canalizar los reportes ciudadanos de puntos críticos de basura y medir su tiempo de atención.
5. Generar reportes para tomar decisiones sobre rutas y recursos.

### 2.4 Alcance inicial (MVP)

| Incluye ✅ | No incluye ❌ (por ahora) |
|---|---|
| Registro de rutas, zonas y horarios | Optimización automática de rutas con IA |
| Seguimiento GPS de camiones desde una app del operador | Sensores de llenado en contenedores (IoT) |
| Consulta de horarios por dirección/zona para ciudadanos | Pagos de arbitrios en línea |
| Notificaciones de "el camión se acerca" | Gestión de personal y planillas |
| Reporte ciudadano de basura acumulada (foto + ubicación) | Integración con otros municipios |
| Panel de monitoreo y reportes básicos para la municipalidad | Gestión de residuos industriales u hospitalarios |

---

## 3. Lean Canvas

| Bloque | Contenido |
|---|---|
| **1. Problema** | • Los vecinos no saben a qué hora pasa el camión y sacan la basura a destiempo<br>• Se forman puntos críticos de basura en calles y esquinas<br>• La municipalidad no sabe en tiempo real dónde están los camiones ni si cumplieron la ruta<br>• Los reclamos ciudadanos se pierden o no se les da seguimiento |
| *Alternativas existentes* | Horarios fijos comunicados por volantes o redes sociales, el silbato o la campana del camión, reclamos por teléfono o en mesa de partes y control de rutas en hojas de papel |
| **2. Segmentos de clientes / Usuarios** | • **Cliente:** Municipalidad (gerencia de limpieza pública)<br>• **Usuarios:** ciudadanos, operadores de camiones y supervisores<br>• **Early adopters:** juntas vecinales de zonas con más puntos críticos |
| **3. Propuesta de valor única** | "Que la basura se recoja a tiempo: el ciudadano sabe cuándo pasa el camión y la municipalidad sabe si pasó." |
| *Concepto de alto nivel* | "Como un seguimiento de delivery, pero para el camión de la basura" |
| **4. Solución** | • App del operador con ruta asignada y envío de ubicación GPS<br>• App/web ciudadana con horarios, alertas y reportes con foto<br>• Panel municipal de monitoreo de flota, incidencias e indicadores |
| **5. Canales** | Página web y redes sociales de la municipalidad, juntas vecinales, campañas de educación ambiental y códigos QR en contenedores y recibos de arbitrios |
| **6. Fuentes de ingreso** | Presupuesto municipal (proyecto de inversión), posible licencia anual del software para otros municipios y fondos o programas ambientales |
| **7. Estructura de costos** | Desarrollo y mantenimiento, hosting en la nube, servicio de mapas/GPS, dispositivos móviles para operadores, capacitación y soporte |
| **8. Métricas clave** | • % de rutas completadas a tiempo<br>• N.º de usuarios ciudadanos activos<br>• N.º de puntos críticos reportados vs. atendidos<br>• Tiempo promedio de atención de reportes<br>• Reducción de reclamos |
| **9. Ventaja diferencial** | Adaptado a la realidad local (calles estrechas, zonas sin numeración, conectividad limitada), información en tiempo real y participación ciudadana integrada |

---

## 4. Riesgos iniciales

Escala: **A** = alta, **M** = media, **B** = baja.

| ID | Riesgo | Categoría | Prob. | Impacto | Mitigación |
|---|---|---|---|---|---|
| R1 | Baja adopción del sistema por parte de los ciudadanos | Negocio | A | A | Campañas con juntas vecinales, interfaz simple y canal alternativo por WhatsApp/SMS |
| R2 | Fallas o pérdida de señal GPS en los camiones | Técnico | M | A | Guardar ubicaciones sin conexión y sincronizarlas después; mostrar la "última ubicación conocida" |
| R3 | Resistencia de los operadores a usar la app | Organizacional | M | A | Involucrarlos en el diseño, capacitación práctica y una app con pocos pasos |
| R4 | Conectividad móvil limitada en algunas zonas | Técnico | A | M | Modo offline y bajo consumo de datos |
| R5 | Cambio de gestión municipal o recorte de presupuesto | Político / financiero | M | A | Entregas incrementales con valor visible temprano y documentación de resultados |
| R6 | Direcciones y zonas mal registradas | Datos | M | M | Levantamiento inicial de rutas con el equipo de campo y validación en mapa |
| R7 | Reportes ciudadanos falsos o mal usados | Operativo | M | B | Exigir foto y ubicación, moderación y límite de reportes por usuario |
| R8 | Exposición de datos personales de los ciudadanos | Legal / seguridad | B | A | Cumplir la Ley de Protección de Datos Personales (Ley 29733), recolectar los datos mínimos y cifrarlos |
| R9 | Falta de dispositivos móviles para los operadores | Recursos | M | M | Incluirlos en el presupuesto inicial o usar dispositivos compartidos por camión |

---

## 5. Reflexión

> *Nota: el enunciado del laboratorio pregunta sobre Git.*

**¿Por qué Git es crítico en proyectos colaborativos?**
Porque permite que varias personas trabajen sobre el mismo código al mismo tiempo sin sobrescribirse. Cada cambio queda registrado con su autor, fecha y motivo. Con las ramas, cada integrante puede desarrollar una funcionalidad de forma aislada y luego integrarla mediante *merge* o *pull request*, lo que facilita la revisión. Además, junto con GitHub, sirve como respaldo remoto y fuente única de verdad del proyecto.

**¿Qué problemas evita?**
- Pérdida de código por sobrescritura o por fallas del equipo
- Confusión de versiones del tipo "final_v2_ahora_si.zip"
- Conflictos no detectados entre cambios de distintos integrantes
- No poder volver a una versión que sí funcionaba
- No saber quién hizo un cambio ni por qué

Además, en este proyecto también versionamos los artefactos del Agile Inception (visión, canvas y riesgos), así que la evolución del alcance queda trazada junto con el código.

---

## 6. Trabajo extra

### 6.1 Refinamiento del Lean Canvas
- Se completaron los **9 bloques**, no solo los 4 solicitados.
- Se separó **cliente** (quien paga: la municipalidad) de **usuarios** (ciudadanos y operadores).
- Se definieron **early adopters** para validar el MVP en una zona piloto.
- Se agregaron **métricas medibles** para evaluar el éxito del piloto.

### 6.2 Soluciones similares

| Solución | Qué ofrece | Qué tomamos como idea | Diferencia con EcoRuta |
|---|---|---|---|
| **RUBICONSmartCity** (EE. UU.; desde agosto de 2024 pertenece a Routeware) | Software para flotas municipales de recolección: seguimiento GPS de vehículos, avance de rutas en tiempo real, verificación digital del servicio y portal web para supervisores. Usado en ciudades como Atlanta y Denver | Panel de flota y confirmación del servicio por parada | Requiere hardware dedicado en cada camión (tablet, dispositivo telemático y cámara); no está orientado al ciudadano |
| **Sensoneo** (Eslovaquia) | Sensores ultrasónicos de nivel de llenado en contenedores y software de optimización de rutas. Caso emblemático: Bratislava, con sensores en unos 1 750 contenedores y equipos en 92 camiones | Planificar las rutas según datos reales (fase futura) | Requiere infraestructura IoT, fuera del alcance del MVP |
| **Recycle Coach** (EE. UU. y Canadá) | App web y móvil gratuita para vecinos: calendario de recojo por dirección, recordatorios (push, SMS o correo), avisos de cambios de horario, buscador de "¿dónde va cada residuo?" y reporte de recojos no realizados | Consulta de horarios por dirección y alertas configurables | Trabaja con horarios fijos y no muestra la ubicación real del camión |
| **SeeClickFix 311 CRM** (EE. UU.; producto de CivicPlus) | Plataforma web y móvil para que los vecinos reporten problemas urbanos y sigan su atención; asigna los reportes según ubicación y categoría y detecta duplicados | Reporte ciudadano con ubicación, asignación automática y seguimiento del estado | Es genérica para cualquier servicio municipal y no se especializa en residuos |

*Fuentes: Waste360, Business Wire y Routeware (Rubicon); sensoneo.com y Recycling Magazine (Sensoneo); páginas municipales de Leduc, Frederick County y Westchester County (Recycle Coach); civicplus.com (SeeClickFix). Consultadas en octubre de 2026.*

**Conclusión:** ninguna solución integra en un solo producto de bajo costo el seguimiento de la flota, la información a vecinos y los reportes ciudadanos adaptados al contexto local. Ese es el espacio que busca cubrir EcoRuta Cusco.

---

## 7. Herramientas sugeridas

| Herramienta | Uso |
|---|---|
| **Miro** | Lean Canvas visual y mapa de stakeholders (poder/interés) |
| **Notion** | Documento de visión y registro de riesgos |
| **Trello** | Backlog inicial del MVP (columnas: Por hacer / En progreso / Hecho) |
| **Git + GitHub** | Versionado de este documento y del código |
