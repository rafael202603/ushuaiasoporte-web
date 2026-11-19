# MANUAL DE ESTILO — USHUAIA SOPORTE TÉCNICO (`USP`)

> Documento canónico de identidad visual, tipográfica, cromática y verbal.  
> Uso: Referencia normativa (`DESIGN.md`) para diseñadores, desarrolladores y agentes de IA.  
> Dominio oficial: `ushuaiasoporte.com` · Coordenadas: `54°48′S 68°18′W`

---

## 01. Esencia de Marca y Verdad Corporativa

Todo artefacto digital o impreso emitido en nombre de **Ushuaia Soporte Técnico** debe regirse por la verdad operativa verificable. Cero fabricación, cero relleno comercial y cero adornos superfluos.

| Atributo | Especificación Verificada |
| :--- | :--- |
| **Nombre comercial** | Ushuaia Soporte Técnico |
| **Sigla operativa** | `USP` (monograma histórico en archivos fuente: `UST`) |
| **Dominio web** | `ushuaiasoporte.com` |
| **Fundador y CEO** | Rafael Pinto (bilingüe ES/EN; trayectoria previa en hotelería Lennox/Albatros y análisis/implementación en Delver Agencia Marítima) |
| **Inicio de operaciones** | `2014` — Ushuaia, Tierra del Fuego, Argentina (`54°48′S 68°18′W`) |
| **Cobertura geográfica** | Atención presencial en Ushuaia; soporte remoto en toda la Patagonia y Argentina (incluyendo operación multisede en Ushuaia y El Calafate) |
| **Teléfono / WhatsApp** | `+54 9 2901 519191` (`https://wa.me/5492901519191`) |
| **Correos corporativos** | `rafael@ushuaiasoporte.com`, `soporte@ushuaiasoporte.com`, `contacto@ushuaiasoporte.com` (y `juan@ushuaiasoporte.com` en operaciones) |
| **Taglines oficiales (vectores)** | `"Provisión, Diseño y Armado de Redes CORPORATIVAS"` · `"Servicios Informáticos"` |

### Mandato de Identidad (Directriz del Fundador)

- **Sobriedad:** estética arquitectónica, precisa y sin estridencias visuales.
- **Nitidez:** geometría limpia, contrastes medidos y jerarquía inequívoca.
- **Claridad en la información:** cada dato técnico, contacto o alcance de servicio se presenta de forma directa y escaneable.
- **Homogeneidad tipográfica:** máximo **2 familias** en todo el sistema (una *sans-serif* geométrica sobria + una monoespaciada técnica para datos duros, protocolos, métricas y contacto).
- **Cero relleno de marketing:** sin hipérboles vacías ni promesas genéricas.
- **Cero emojis decorativos:** nunca utilizar emojis en interfaces, documentación corporativa, firmas ni piezas de comunicación.

---

## 02. Isotipo, Anatomía y Reglas de Uso

El isotipo oficial proviene directamente de los archivos vectoriales maestros (`LOGO SOPORTE USHUAIA RAFA PINTO.pdf/.ai`). **Nunca debe redibujarse a mano**; siempre se utilizan los activos SVG oficiales alojados en `web-pilots/assets/`.

### Simbología y Estructura (`viewBox="0 0 360 360"`)

El emblema es un **sello circular** compuesto por cinco capas semánticas verificables en `usp-logo-layered.svg`:

1. **Anillo exterior (`usp-ring`):** perímetro circular entre `r = 153.72` y `r = 169.22` centrado en `(180, 180)`, que contiene e integra el sistema.
2. **Faro Les Éclaireurs (`usp-faro`):** silueta central del faro emblemático del Canal Beagle (`x ≈ 179.5`, `y: 54.01 → 300.00`), símbolo de guía continua y estabilidad operativa en el Fin del Mundo.
3. **Baliza (`usp-beacon`):** núcleo luminoso en la cúspide del faro (`cx: 179.51`, `cy: 49.96`, `r: 8.10`), punto focal de monitoreo y disponibilidad.
4. **Conector RJ45 Izquierdo (`usp-rj-left`):** ficha Ethernet orientada hacia el faro (`x: 20.26 → 145.85`, `y: 144.95 → 214.95`).
5. **Conector RJ45 Derecho (`usp-rj-right`):** ficha Ethernet simétrica (`x: 213.61 → 339.20`, `y: 145.18 → 215.18`). Ambos conectores representan la conectividad física y de red de misión crítica.

### Variantes Oficiales en `web-pilots/assets/`

| Archivo | Color / Relleno | Uso Recomendado |
| :--- | :--- | :--- |
| `usp-logo-cyan.svg` | `#00AEEF` (Cian Beagle) | Uso principal sobre fondos claros (`#FFFFFF`, `#F4F7FA`) u oscuros profundos (`#070A10`, `#252936`). |
| `usp-logo-white.svg` | `#FFFFFF` (Blanco Glaciar) | Aplicación monocromática negativa sobre superficies Cian Beagle (`#00AEEF`), Grafito Austral o fotografía oscura controlada. |
| `usp-logo-dark.svg` | `#1A1E29` (Tinta oscura) | Impresión monocromática en negro/tinta profunda o documentación técnica en blanco y negro. |
| `usp-logo-seal.svg` | Disco `#FFFFFF` + trazo `#00AEEF` | Sello cerrado de alto contraste para avatares, cabeceras con textura o fondos donde se requiera contención sólida. |
| `usp-logo-layered.svg` | `currentColor` en 5 `<g>` | Uso interactivo web (CSS hover/estado en baliza o conectores) y diagramas de anatomía técnica. |

### Zona de Respeto y Tamaños Mínimos

- **Unidad modular (`x`):** equivale al espesor del anillo exterior en el espacio normalizado o a `1/8` del diámetro total del isotipo (`D`). Para mayor precisión práctica, la **zona de respeto mínima** alrededor de los 4 bordes del sello es **`0.25 × D`** (equivalente a `1x` tomando `x = 0.25D`, es decir `90px` en el `viewBox` de `360`). Ningún texto, borde de contenedor ni otro elemento gráfico puede invadir esa área.
- **Tamaño mínimo digital:** `28 px` de diámetro para isotipo simple (`usp-logo-cyan.svg` / `usp-logo-seal.svg`); `16 px` exclusivamente en `favicon` simplificado sin pérdida de reconocimiento del faro.
- **Tamaño mínimo impreso:** `12 mm` de diámetro en papelería y tarjetas personales; `10 mm` en sellos auxiliares.

### Usos Prohibidos

- Deformar proporciones (`aspect-ratio` distinto de `1:1`).
- Rotar el faro o desalinear la simetría horizontal de los conectores RJ45.
- Aplicar sombras paralelas difusas, biseles 3D o gradientes arcoíris sobre el isotipo.
- Colocar `usp-logo-cyan.svg` directamente sobre fondos azules/cian de luminancia similar sin usar la variante `white` o `seal`.
- Redibujar el trazo en lugar de referenciar los SVG oficiales.

---

## 03. Paleta Cromática y Tokens

Todos los valores cromáticos derivan de los PDFs vectoriales originales de Illustrator y los maestros PNG de marca, extendidos con tokens de interfaz oscuros y claros de contraste verificado.

### Primario y Acento

| Token CSS | Nombre | HEX | RGB | CMYK | OKLCH | Contraste / Rol |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `--usp-cyan` | **Cian Beagle** (Primario Oficial) | `#00AEEF` | `0, 174, 239` | `87, 0, 0, 0` | `71.8% 0.148 228.5°` | Acento gráfico, isotipo, bordes activos, texto/elementos sobre `#070A10` (`8.2:1` AAA) y `#252936` (`5.7:1` AA). |
| `--usp-cyan-deep` | **Cian Profundo** (Acento Accesible) | `#0074A6` | `0, 116, 166` | `92, 42, 12, 2` | `53.2% 0.116 232°` | Enlaces, etiquetas e iconos de texto sobre blanco `#FFFFFF` (`5.14:1` WCAG AA) y `#F4F7FA` (`4.82:1` AA). |

### Superficies y Tintas

| Token CSS | Nombre | HEX | RGB | CMYK | OKLCH | Rol y Contraste |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `--usp-obsidian` | **Obsidiana Antártica** | `#070A10` | `7, 10, 16` | `— (Digital)` | `14.5% 0.015 260°` | Fondo principal de interfaz web oscura de alta precisión. |
| `--usp-obsidian-elev` | **Obsidiana Elevada** | `#101521` | `16, 21, 33` | `— (Digital)` | `19.2% 0.024 261°` | Tarjetas, paneles técnicos y barras laterales en modo oscuro. |
| `--usp-graphite` | **Grafito Austral** | `#252936` | `37, 41, 54` | `87, 82, 62, 40` | `28.5% 0.022 268°` | Superficie oscura oficial de Tarjeta Vector Opción 2 y bloques institucionales. |
| `--usp-white` | **Blanco Glaciar** | `#FFFFFF` | `255, 255, 255` | `0, 0, 0, 0` | `100% 0 0°` | Superficie clara primaria, papelería e impresión A4. |
| `--usp-alabaster` | **Alabastro Mineral** | `#F4F7FA` | `244, 247, 250` | `3, 1, 1, 0` | `97.5% 0.006 248°` | Superficie secundaria clara, grilla técnica y contenedores alternos. |
| `--usp-ink` | **Tinta Polar** | `#0D131F` | `13, 19, 31` | `86, 74, 54, 72` | `18.3% 0.025 258°` | Texto principal sobre fondos claros (`18.5:1` sobre `#FFFFFF`, WCAG AAA). |
| `--usp-slate` | **Gris Técnico** | `#556278` | `85, 98, 120` | `68, 52, 34, 15` | `49.3% 0.036 259°` | Texto secundario, metadatos y subtítulos sobre `#FFFFFF` (`6.08:1` WCAG AA/AAA grande). |

### Semántica Operativa (Uso Restringido)

Solo debe utilizarse para representar **estados reales de infraestructura, enlaces o monitoreo**. Prohibido su uso como decoración de marca.

| Token CSS | Nombre | HEX | RGB | OKLCH | Uso Permitido |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `--usp-status-ok` | **Enlace** | `#10B981` | `16, 185, 129` | `69.6% 0.149 162.5°` | Servidor en línea, VPN/Tailscale activo, backup verificado. |
| `--usp-status-warn` | **Alerta** | `#F59E0B` | `245, 158, 11` | `76.9% 0.165 70.1°` | Latencia elevada, espacio en disco bajo, advertencia preventiva. |
| `--usp-status-crit` | **Crítico** | `#EF4444` | `239, 68, 68` | `63.7% 0.208 25.3°` | Caída de enlace, falla de servicio o incidente crítico. |

---

## 04. Sistema Tipográfico (Regla Estricta de 2 Familias)

La identidad exige **homogeneidad tipográfica absoluta**: un máximo de **2 familias** activas en todo proyecto.

1. **Familia 1 — Sans Geométrica Sobria (`--font-sans`):**
   - Pila CSS: `'Plus Jakarta Sans', 'Inter', system-ui, -apple-system, 'Segoe UI', sans-serif`
   - Uso: Titulares arquitectónicos, cuerpo editorial, descripciones de servicio, botones y navegación.
   - Pesos autorizados: `400` (Regular), `500` (Medium), `600` (SemiBold), `700` (Bold).

2. **Familia 2 — Monoespaciada Técnica (`--font-mono`):**
   - Pila CSS: `'JetBrains Mono', 'IBM Plex Mono', 'Consolas', 'Courier New', monospace`
   - Uso: Índices de sección (`01`..`07`), coordenadas (`54°48′S 68°18′W`), códigos HEX/CMYK/OKLCH, teléfonos, emails, nombres de protocolos (`SPF/DKIM/DMARC`, `RDP`, `VPN`, `RJ45`), métricas y estados operativos.
   - Regla obligatoria: Activar siempre `font-variant-numeric: tabular-nums` en tablas, escalas, relojes y cifras.

### Escala Tipográfica Fluida

| Token | Tamaño (`clamp`) | Familia | Peso | Interlineado | Tracking | Uso |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `--type-display` | `clamp(2.25rem, 4.5vw, 3.75rem)` | Sans | `700` | `1.06` | `-0.03em` | Portada principal y titular hero |
| `--type-h1` | `clamp(1.65rem, 2.8vw, 2.35rem)` | Sans | `700` | `1.14` | `-0.025em` | Encabezado de sección principal |
| `--type-h2` | `clamp(1.20rem, 1.8vw, 1.50rem)` | Sans | `600` | `1.25` | `-0.015em` | Subtítulos y bloques técnicos |
| `--type-body` | `clamp(0.95rem, 1.05vw, 1.05rem)` | Sans | `400` | `1.62` | `0` | Párrafos y documentación |
| `--type-mono-md` | `0.875rem` (`14px`) | Mono | `500` | `1.50` | `0.02em` | Datos de contacto, firmas y tokens |
| `--type-mono-xs` | `0.75rem` (`12px`) | Mono | `500` | `1.40` | `0.08em` | Etiquetas en mayúsculas, badges e índices |

---

## 05. Movimiento, Scroll y Accesibilidad

**Principio rector:** *Física de Precisión, no Pirotecnia.* Las transiciones reflejan instrumental técnico calibrado: respuesta inmediata, desaceleración suave y cero rebote elástico exagerado.

| Token | Valor | Uso |
| :--- | :--- | :--- |
| `--ease-usp` | `cubic-bezier(0.22, 1, 0.36, 1)` | Curva maestra de entrada/desaceleración exponencial suave |
| `--dur-fast` | `150ms` | Cambios de color en hover, copiado al portapapeles, estados de foco |
| `--dur-base` | `280ms` | Alternancia de superficies, paneles, tarjetas y overlays de retícula |
| `--dur-slow` | `520ms` | Transiciones estructurales o demostración de señal/baliza |

### Reglas de Implementación y Accesibilidad

- **Sin trampas de `opacity: 0`:** Ningún bloque de contenido en CSS estático puede inicializarse con `opacity: 0` esperando JavaScript para hacerse visible. Si se usa animación de entrada por scroll, debe ser progresiva mediante clase añadida por JS únicamente cuando el entorno soporta `IntersectionObserver` y con respaldo inmediato visible.
- **`prefers-reduced-motion: reduce`:** Obligatorio respetar la preferencia del sistema reduciendo duraciones a `0.01ms` y suprimiendo desplazamientos o pulsos continuos en la baliza del faro.
- **Foco visible:** Todo elemento interactivo mantiene un contorno nítido `:focus-visible` de `2px solid #00AEEF` (sobre oscuro) o `#0074A6` (sobre claro) con `outline-offset: 2px`.

---

## 06. Voz, Tono, Veracidad y Confidencialidad

### Los 5 Pilares Reales de Servicio

Toda comunicación comercial o técnica de `USP` se estructura sobre estos cinco pilares verificados:

1. **Soporte IT Corporativo y Hotelero:** atención presencial y remota, puestos de trabajo, recepción/front, comanderas fiscales Hasar y terminales POS.
2. **Provisión, Diseño y Armado de Redes Corporativas:** cableado estructurado, switches, routers, Wi-Fi empresarial y de huéspedes (`Ubiquiti UniFi`) y gestión de ISPs.
3. **Servidores e Infraestructura Crítica:** `Windows Server`, `SQL Server`, `Terminal Server / RDP` seguro, `Tailscale / VPN`, PMS `Arion / WinPax` y ERP `Bejerman`.
4. **Backups, Monitoreo y Continuidad Operativa:** respaldos automatizados local + nube, auditoría diaria de salud de servidores y recuperación ante incidentes.
5. **Correo Corporativo, Dominios y Cloud:** migración a `Microsoft 365` y `Google Workspace`, administración `DNS`, autenticación `SPF / DKIM / DMARC`, `cPanel` y defensa anti-phishing.

### Tono Editorial

- **Directo, técnico y sereno.** Se habla en español rioplatense profesional o inglés técnico neutro cuando se atiende en modo bilingüe (`ES/EN`).
- **Verbos concretos:** *diagnosticar, aislar, respaldar, migrar, configurar, auditar, sostener*.
- **Evitar:** *"soluciones disruptivas"*, *"transformación 360°"*, *"pasión por la tecnología"*, signos de exclamación múltiples o emojis.

### Regla de Confidencialidad Estricta

- **Prohibido publicar** en sitios web, muestras o documentación pública: direcciones IP privadas o públicas de clientes, credenciales, contraseñas, topologías internas identificables, montos de facturación o nombres de clientes sin autorización expresa.
- **Referencia pública autorizada por sectores:**
  - *"Hotelería multisede en Ushuaia y El Calafate"*
  - *"Comercio, arquitectura y estudios profesionales en Tierra del Fuego"*

---

## 07. Aplicaciones Oficiales y Checklist de Calidad

### Aplicaciones Normativas

1. **Tarjeta Personal Oscura (Opción 2 Vector):** superficie `Grafito Austral #252936`, isotipo `usp-logo-cyan.svg` o `usp-logo-white.svg`, nombre en Sans `700`, bloque de especialidad `"Provisión, Diseño y Armado de Redes CORPORATIVAS"` y pie `"Servicios Informáticos"`, datos de contacto en `JetBrains Mono` / `Consolas`.
2. **Tarjeta Personal Clara (Opción 1 Vector):** superficie `Blanco Glaciar #FFFFFF` con borde técnico sutil `#D8E0EA`, isotipo `usp-logo-cyan.svg`, acentos de contacto en `Cian Profundo #0074A6` para legibilidad AA sobre papel.
3. **Firma de Correo Corporativo:** composición monoespaciada limpia sin imágenes pesadas ni banners promocionales; incluye nombre, rol, sigla `USP`, teléfono `+54 9 2901 519191`, correo y dominio `ushuaiasoporte.com` + `54°48′S 68°18′W`.
4. **Cabecera Web Ejecutiva (`Header Lockup`):** isotipo SVG (`32px`–`40px`) + denominación tipográfica + indicador de coordenadas/estado en `Mono`, con máximo contraste en modo Obsidiana o Blanco Glaciar.

### Checklist de Verificación para Agentes y Diseñadores

- [ ] ¿Se usó únicamente el SVG oficial de `web-pilots/assets/` sin redibujar el faro ni los RJ45?
- [ ] ¿Se respetó el máximo de **2 familias tipográficas** (`Plus Jakarta Sans` + `JetBrains Mono / Consolas`)?
- [ ] ¿Los enlaces y etiquetas sobre fondo claro usan `#0074A6` (y no `#00AEEF` para texto pequeño)?
- [ ] ¿Se eliminaron por completo emojis decorativos y relleno de marketing?
- [ ] ¿Se verificó que no haya IPs, claves, precios internos ni nombres de clientes no autorizados?
- [ ] ¿Funciona el documento/prototipo en `file://` y responde correctamente a `prefers-reduced-motion` y `@media print`?
