# ushuaiasoporte-web — Ushuaia Soporte Técnico (`ushuaiasoporte.com`)

Repositorio oficial del sitio web, el Manual de Estilo Digital y las maquetas interactivas de **Ushuaia Soporte Técnico (USP)** — Ushuaia, Tierra del Fuego, Argentina (`54°48′S 68°18′W`).

> Separado intencionalmente del repositorio operativo interno `USP-GLOBAL` para mantener cero mezcla con datos privados de clientes, facturación o credenciales.

---

## Estructura del repositorio

```text
ushuaiasoporte-web/
├── index.html                           # Sitio oficial principal — Aurora Austral (Single-Scroll Cinematográfico)
├── favicon.svg                          # Isotipo oficial vectorial (Faro Les Éclaireurs + RJ45)
├── studio/index.html                    # Hub histórico de comparativa de los 3 pilotos
├── assets/
│   ├── usp-logo-cyan.svg                # Vector oficial exacto (#00AEEF) extraído de PDF Illustrator
│   ├── usp-logo-white.svg               # Versión negativa blanca
│   ├── usp-logo-dark.svg                # Versión monocroma grafito (#1A1E29)
│   ├── usp-logo-seal.svg                # Sello circular con fondo blanco (estilo Tarjeta Opción 2)
│   ├── usp-logo-layered.svg             # SVG semántico en 5 capas animables (ring/faro/beacon/rj45-L/rj45-R)
│   ├── usp-logo-currentcolor.svg        # SVG adaptable a CSS currentColor
│   └── usp-logo-official.png            # Master raster oficial 1080×1080
├── manual-de-estilo/
│   ├── index.html                       # Manual de Estilo Digital interactivo (exportable a PDF A4)
│   └── MANUAL_DE_ESTILO.md              # Guía canónica Markdown (DESIGN.md)
├── piloto-1-faro-telemetry/index.html   # Archivo de referencia — Piloto 01
├── piloto-2-meridiano-54/index.html     # Archivo de referencia — Piloto 02
├── piloto-3-aurora-austral/index.html   # Archivo de referencia — Piloto 03 base
├── .github/workflows/deploy.yml         # CI/CD automático hacia GitHub Pages en cada push a main
└── _headers                             # Cabeceras de seguridad listas para Cloudflare Pages
```

---

## Arquitectura de Hosting Elegida ($0/mes, Comercial, Sin Bloqueos)

| Plataforma | Costo | Uso comercial permitido | Actualización desde GitHub | Notas clave |
| :--- | :---: | :---: | :---: | :--- |
| **GitHub Pages (Activo ahora)** | **$0/mes** | Sí | Automática vía `.github/workflows/deploy.yml` | SSL automático, CDN global Fastly, cero cuentas extra. Ideal para previsualización inmediata y producción estática. |
| **Cloudflare Pages (Opcional recomendado para producción)** | **$0/mes** | Sí (sin límite de ancho de banda) | Automática en cada `git push` + previews por rama | Nodos en Buenos Aires / Sudamérica, SSL automático, `_headers` ya incluido, sinergia directa si se migra DNS a Cloudflare. |
| *Vercel Hobby (descartado)* | $0/mes | **No** (ToS prohíbe uso comercial en plan gratuito; Pro cuesta USD 20/mes) | Automática | No conviene para el sitio comercial de una empresa. |
| *Supabase Free (no requerido)* | $0/mes | Sí (con pausa automática tras 7 días sin actividad) | N/A (es backend DB/Auth) | Solo tendría sentido en una fase futura si se agrega portal de clientes/tickets; para el sitio web aporta latencia sin beneficio. |

---

## Cómo actualizar el sitio desde GitHub

Cualquier cambio en este repositorio se publica automáticamente en ~20 segundos:

```bash
git add .
git commit -m "feat(web): actualizar contenido o diseño"
git push origin main
```

---

## Cómo promover el piloto ganador a producción (`ushuaiasoporte.com`)

1. Una vez elegido el piloto definitivo (`piloto-1-faro-telemetry`, `piloto-2-meridiano-54` o `piloto-3-aurora-austral`), se promueve su `index.html` a la raíz del repositorio (ajustando las rutas relativas de `../assets/` a `./assets/`).
2. En **Squarespace DNS** (`ushuaiasoporte.com`) — o en **Cloudflare DNS** si se conecta Cloudflare Pages:
   - **Opción GitHub Pages (manteniendo Squarespace DNS):**
     - `A` `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
     - `CNAME` `www` → `rafael202603.github.io`
     - Agregar archivo `CNAME` en la raíz con `ushuaiasoporte.com` y activar *Enforce HTTPS*.
   - **Opción Cloudflare Pages:**
     - Conectar este repo desde Cloudflare Dashboard → *Workers & Pages → Create → Pages → Connect to Git* (sin comando de build, directorio de salida `/`), y asignar el dominio personalizado `ushuaiasoporte.com`.
