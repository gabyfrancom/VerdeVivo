# 🌿 VerdeVivo

**App de cuidado de plantas (PWA)** — funciona en Android, iPhone y navegador de escritorio. Controla el estado de tus plantas: riego, poda, necesidades de sol y ubicación, con fotos, alertas y datos meteorológicos de tu zona.

## ✨ Funciones

- **Estado de cada planta** — semáforo automático: ✅ Bien / ⚠️ Atención / 🚨 Urgente según los días transcurridos desde el último riego y poda.
- **Registro de riegos** — botón "💧 Regada" que guarda la fecha y hora del móvil y lleva un historial por planta.
- **Alertas del próximo riego** — banner en pantalla y notificación del navegador cuando toca regar (verifica cada minuto según la fecha/hora del dispositivo).
- **Clima en tiempo real** — temperatura ambiente, humedad relativa y presión atmosférica de tu ubicación exacta, vía [Open-Meteo](https://open-meteo.com/) (gratis, sin API key) y la geolocalización del móvil.
- **Fotos** — sube fotos de tus plantas (se comprimen automáticamente) o usa las imágenes de ejemplo.
- **Ubicaciones y sol** — asigna cada planta a una ubicación (salón, balcón, jardín...) y su necesidad de sol: sombra, sol parcial o sol pleno.
- **Modo oscuro** — claro/oscuro con detección automática de la preferencia del sistema.
- **Instalable** — al ser PWA se instala como app nativa desde el navegador, funciona offline y guarda todos los datos en el dispositivo (localStorage).

## 📱 Instalación en el móvil

1. Sube estos archivos a GitHub y activa **GitHub Pages** (Settings → Pages → rama `main`).
2. Abre la URL en el navegador del móvil.
3. **Android (Chrome):** menú ⋮ → *"Añadir a pantalla de inicio"*.
4. **iPhone (Safari):** botón Compartir → *"Añadir a pantalla de inicio"*.

> ⚠️ **Nota sobre las alertas:** las notificaciones web funcionan con la app abierta o instalada como PWA. Para que lleguen con la app cerrada se requeriría un servidor de push (fuera del alcance de una app 100 % estática y gratuita). La app también muestra el aviso en pantalla cada vez que la abres.

## 🛠️ Tecnologías

- HTML + CSS + JavaScript puro (sin frameworks ni dependencias).
- [Open-Meteo API](https://open-meteo.com/) para datos meteorológicos.
- Geolocation API, Notification API, Canvas (compresión de fotos), Service Worker + Manifest (PWA).

## 📁 Estructura

```
├── index.html        # App completa (HTML + CSS + JS)
├── manifest.json     # Manifiesto PWA
├── sw.js             # Service Worker (offline)
├── icons/            # Íconos de la app
│   ├── icon-192.png
│   └── icon-512.png
└── img/              # Fotos de ejemplo
    ├── monstera.jpg
    ├── cactus.jpg
    └── helecho.jpg
```

## 🚀 Uso

1. Pulsa **➕ Añadir planta** y completa nombre, ubicación, sol, frecuencia de riego y poda.
2. Sube una foto si quieres (opcional).
3. Cuando riegues, pulsa **💧 Regada** — la app calcula solo cuándo toca el próximo riego.
4. Activa la ubicación para ver temperatura, humedad y presión de tu zona.
5. Pulsa **🔔 Activar alertas** para recibir notificaciones cuando una planta necesite agua.

---

Hecho con 💚 para que ninguna planta vuelva a morirse de sed.
