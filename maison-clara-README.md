# MAISON CLARA — Tienda de Hogar & Decoración

Demo visual de la tienda **MAISON CLARA** desplegada en GitHub Pages.  
La versión de venta real está en Shopify con Spocket como proveedor de dropshipping.

🌐 **Demo en vivo:** `https://TUNOMBRE.github.io/maison-clara/`  
🛍️ **Tienda Shopify:** `https://TUTIENDA.myshopify.com`

---

## ¿Qué es este repositorio?

Esta página sirve como **landing de marca y catálogo visual** para MAISON CLARA. Es la cara pública del proyecto antes de redirigir a la tienda oficial en Shopify donde se procesan los pedidos reales.

Usos principales:
- Portfolio / demo de la tienda para inversores o colaboradores
- Landing page de marca para campañas de ads (URL más limpia que myshopify.com)
- Página de presentación para redes sociales e influencers

---

## Estructura del proyecto

```
maison-clara/
├── index.html              # Tienda completa (una sola página)
├── README.md               # Este archivo
└── .github/
    └── workflows/
        └── deploy.yml      # Auto-deploy a GitHub Pages en cada push
```

---

## Cómo publicarlo en 5 minutos

### Paso 1 — Crear el repositorio en GitHub

1. Ve a [github.com/new](https://github.com/new)
2. Nombre del repo: `maison-clara`
3. Visibilidad: **Public** (necesario para GitHub Pages gratuito)
4. NO marques "Add a README file" (ya lo tienes aquí)
5. Haz clic en **Create repository**

### Paso 2 — Subir los archivos

Desde tu terminal (con [Git](https://git-scm.com/) instalado):

```bash
# Clona el repo vacío que acabas de crear
git clone https://github.com/TUNOMBRE/maison-clara.git
cd maison-clara

# Copia los archivos de este proyecto dentro de la carpeta
# (index.html, README.md y la carpeta .github/)

# Sube todo a GitHub
git add .
git commit -m "🚀 Lanzamiento inicial MAISON CLARA"
git push origin main
```

### Paso 3 — Activar GitHub Pages

1. Ve a tu repo en GitHub → **Settings** → **Pages**
2. En **Source**, selecciona **GitHub Actions**
3. El workflow `.github/workflows/deploy.yml` se ejecutará automáticamente
4. En 1–2 minutos tu tienda estará en: `https://TUNOMBRE.github.io/maison-clara/`

### Paso 4 — Personalizar los enlaces a Shopify

Abre `index.html` y reemplaza las dos apariciones de `TUTIENDA.myshopify.com` con la URL real de tu tienda Shopify. También reemplaza `TUNOMBRE` con tu usuario de GitHub en los meta tags OG y la URL canónica.

```bash
# En macOS/Linux, reemplaza de golpe con sed:
sed -i 's/TUTIENDA.myshopify.com/nombrereal.myshopify.com/g' index.html
sed -i 's/TUNOMBRE/tunombredeusuario/g' index.html

git add index.html
git commit -m "✏️ Actualizar enlaces a Shopify"
git push origin main
```

---

## Dominio personalizado (opcional)

Si tienes el dominio `maisonclara.es`, puedes apuntarlo a GitHub Pages:

1. En tu proveedor de dominios, añade estos registros DNS:

```
Tipo    Nombre    Valor
A       @         185.199.108.153
A       @         185.199.109.153
A       @         185.199.110.153
A       @         185.199.111.153
CNAME   www       TUNOMBRE.github.io
```

2. En GitHub → Settings → Pages → **Custom domain**: escribe `maisonclara.es`
3. Marca **Enforce HTTPS**
4. La propagación puede tardar hasta 24h, pero suele ser mucho menos

---

## Productos incluidos en la demo

| Producto | Precio | Margen estimado |
|---|---|---|
| Tira LED RGB Ambiente | 34,90 € | ~65% 🔥 |
| Espejo LED Retroiluminado | 79,90 € | ~55% 🔥 |
| Vinilos Geométricos Adhesivos | 24,90 € | ~60% 🔥 |
| Set Velas Soja Aromáticas x4 | 38,90 € | ~70% |
| Humidificador Aromaterapia | 49,90 € | ~52% |
| Organizador Modular Bambú | 44,90 € | ~54% |
| Lámpara Colgante Ratán | 64,90 € | ~50% |
| Jarrón Artesanal Barro | 76,90 € | ~52% |

Proveedor: [Spocket](https://www.spocket.co) — almacenes EU, envío 3–7 días.

---

## Stack técnico

- HTML5 + CSS3 puro (sin frameworks)
- Google Fonts: Cormorant Garamond + Inter
- Imágenes: [Unsplash](https://unsplash.com) (sustituir por fotos propias)
- Despliegue: GitHub Actions → GitHub Pages (gratuito)

---

## Licencia

Este código es de uso personal para el proyecto MAISON CLARA.  
Las imágenes de Unsplash tienen licencia propia — no usar con fines comerciales sin sustituirlas por imágenes propias o con licencia comercial.
