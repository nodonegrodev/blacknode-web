# AGENTS.md — BlakNode v2.0 (reglas del proyecto)

> Leídas por cualquier agente que trabaje en esta carpeta. **Mandan sobre tu criterio.** Si algo de este archivo entra en conflicto con el Brandbook, gana el Brandbook y avisás.

## 1. Qué es esto
Landing de una sola página de **BlakNode** (con K), agencia de software, diseño y proyectos, Chile. Público: dueños y gerentes de PyME chilenas, que llegan desde el celular por WhatsApp. **Objetivo único de la página: que escriban por WhatsApp.**

## 2. Marca (Brandbook V1.0 — no negociable)
- **Colores:** `--negro:#0C0B0B` · `--naranja:#F14E20` · `--blanco:#FFFFFF` · apoyos `--grafito:#1C1A19` (tarjetas) · `--humo:#2E2B29` (líneas) · `--piedra:#8C8782` (texto secundario) · `--hueso:#F5F2ED` (papel) · `--brasa:#FF7A4D` (hover) · `--ascua:#B8350F`.
- **Proporción: negro 55 % · blanco 30 % · naranja 15 %.** El naranja **solo** en acciones, estado activo y datos clave.
- **Tipografía, tres voces que nunca se mezclan:** Barlow Condensed 800 en MAYÚSCULAS para titulares (interlineado 0,9) · Inter 400/500/600/700 para cuerpo (16/24 mínimo) · JetBrains Mono para etiquetas, números y URL (12 px, `letter-spacing:.14em`).
- **Firma:** corte de **14°** en bloques grandes y cabeceras · **sombra dura** plana de 12 px, sin desenfoque · patrón NODOS muy tenue, nunca bajo párrafos largos.
- **Logotipo:** `logo-blaknode-inverso.svg` (versión para fondos oscuros) y `favicon.svg`. **No deformar, no rotar, no sombrear, no recolorear.** Mínimo digital: 64 px de alto el logotipo, 24 px el isotipo.
- **Voz:** tú, frases de ≤ 20 palabras, verbos de acción (construimos, diseñamos, entregamos, escuchamos). Cercano y audaz, nunca vendehúmo.
- **Prohibidas:** soluciones integrales · sinergia · disruptivo · líder del mercado · experto en todo · paquete cerrado · best-in-class · llave en mano · transformación digital.

## 3. Restricciones técnicas
| Regla | Motivo |
|---|---|
| Un solo `index.html`, CSS y JS en línea | hosting cPanel compartido: solo estático |
| **Cero librerías** (sin GSAP, Lenis, ScrollTrigger, React, jQuery) y **cero CDN** | presupuesto y latencia del origen |
| **Cero rastreadores** (sin GA, Meta Pixel, Tag Manager) | contradice el pilar de soberanía de datos |
| Fuentes self-hosted en esta carpeta, con `preload` y `font-display: swap` | 3 archivos, ~99 KB |
| Video con `preload="none"`, cargado **después** del primer pintado, con `poster` | el video pesa 461 KB y no puede tocar el LCP |
| Cero degradados, cero `backdrop-filter` | el brandbook pide contraste plano |
| Deploy: git → cPanel Git → Update from Remote → **Deploy HEAD Commit**. **Nadie edita `public_html` a mano.** | regla de la casa |

## 4. Contenido: lo que está prohibido inventar
- **Titular aprobado del hero:** `DISEÑAMOS SOFTWARE, QUE LA HERRAMIENTA SE ADAPTE A TU NEGOCIO.` **El copy es territorio del Capitán: ningún texto se reescribe en una pasada de maquetación.** Si proponés uno mejor, lo escribís aparte en el reporte.
- **Clientes, casos, testimonios, logos de terceros, portafolio.** No existen todavía.
- **Cifras de resultados** («+300 %», «duplicaron», «92 % de reducción»).
- **Garantías técnicas no cumplidas**: sin frecuencias de respaldo concretas, sin «24/7», sin «activo en línea».
- **Títulos que no corresponden** y nombres de empresas reales (los talonarios y fichas de utilería van con campos vacíos: `CLIENTE: ————`).
- **Amenazas**: ni multas, ni UTM, ni fiscalización. La normativa se menciona como oficio, nunca como susto.
- Si necesitás un dato que no está en este archivo ni en el brief: **preguntás**. No lo rellenás.

## 5. Pisos de calidad (se miden, no se opinan)
- Cuerpo de lectura **≥ 16 px / 24 px**; etiquetas Mono ≥ 11 px; **ninguna línea de texto bajo 45 ni sobre 75 caracteres**; párrafos **≤ 3 líneas**.
- **Un elemento dominante por pantalla.** Ninguna sección con más de ~30 % de su viewport en negro sin función.
- Ninguna sección con la misma silueta que la vecina: alternar lleno / lista indexada / riel con filas / escenario multimedia / paneles enfrentados / cierre tipográfico.
- Contraste **AA** mínimo (4.5:1 cuerpo, 3:1 grande). Área tocable **≥ 48 px**. `prefers-reduced-motion` respetado y **los controles siguen funcionando** sin animación.
- Responsive verificado en **390 px**: sin desbordes horizontales, sin bloques vacíos, sin elementos cortados.

## 6. Reporte obligatorio al cerrar cualquier tarea
1. Capturas en **1280 px y 390 px** de cada sección tocada.
2. Peticiones y KB totales del primer pintado (presupuesto: **< 150 KB**, ≤ 5 peticiones).
3. **LCP y CLS medidos** con `PerformanceObserver`, pegando el número y el comando. **Sin medición no está terminado.**
4. Tamaño calculado de cada texto de lectura y caracteres por línea.
5. Checklist de marca (§2) y de prohibiciones (§4).

## 7. Cómo trabajás
- Un archivo, una entrega, cambios chicos y verificables. No instales dependencias ni agregues paso de build.
- **No toques nada fuera de esta carpeta.** No borres ni renombrés los `.woff2`, el logo, los videos ni la `og:image`.
- Si una instrucción del pedido contradice este archivo, **avisás antes de hacerla**.
- Antes de dar por hecho que algo «queda bien», miralo: a pantalla completa, en 390 px y con el movimiento desactivado.

## 8. Skills de diseño disponibles en `./.agents/skills/`
`design-taste` (anti-slop: patrones prohibidos y pre-flight) · `frontend-design` (dirección de arte, tipografía, plan antes de código) · `taste-design-review` (auditoría con severidad P0-P3) · `copywriting` · `impeccable`.
**Leelas antes de maquetar una sección nueva.** Después de cambiar una sección, pasala por el pre-flight de `design-taste`.
