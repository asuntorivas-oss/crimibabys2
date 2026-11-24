# BB Criminóloga · Expedientes CrimiBABYS

Sitio de venta y juego web del **Expediente 001: La última Navidad**.

## Qué hay en esta carpeta

```
bb-criminologa/
├── index.html                      ← Landing de venta (página principal)
├── assets/
│   └── dafne.jpg                   ← Foto de Dafne para la landing
└── caso/
    └── la-ultima-navidad/
        ├── index.html              ← El juego (expediente para celular)
        ├── bienvenida.mp4          ← Video de bienvenida (temporal)
        └── poster.jpg              ← Portada del video
```

Cuando esté publicado, quedará así:

- Landing: `https://tudominio.com/`
- Juego: `https://tudominio.com/caso/la-ultima-navidad/`

## Antes de subirlo: 3 cosas que debes cambiar

1. **Enlace de pago.** En `index.html`, busca `LINK_DE_PAGO` y reemplázalo por tu enlace de Hotmart o Stripe (botón "Comprar ahora").
2. **Código de acceso.** En `caso/la-ultima-navidad/index.html`, busca `const CODE='CRIMI-001';` y cambia el código si quieres. Es el que le llega al cliente por correo.
3. **Correo de compra.** En tu plataforma de pago, configura el correo automático con este texto:
   > ¡Gracias por tu compra, CrimiBABY! Abre tu expediente aquí: https://tudominio.com/caso/la-ultima-navidad/ · Tu código de acceso: CRIMI-001 · Pueden jugar hasta 6 personas con el mismo código, cada una desde su celular.

## Paso 1 · Subirlo a GitHub (sin usar la terminal)

1. Entra a github.com y crea una cuenta si no tienes.
2. Arriba a la derecha: **+ → New repository**.
3. Nombre: `bb-criminologa`. Elige **Private** (privado) — ver la nota de seguridad abajo.
4. Clic en **Create repository**.
5. En la página del repositorio: **uploading an existing file** (o **Add file → Upload files**).
6. Arrastra **todo el contenido** de esta carpeta (los archivos y las carpetas `assets` y `caso`, no la carpeta exterior).
7. Abajo, clic en **Commit changes**.

## Paso 2 · Publicarlo en internet (recomendado: Netlify, gratis)

Netlify publica gratis desde un repositorio privado de GitHub.

1. Entra a netlify.com → **Sign up with GitHub**.
2. **Add new site → Import an existing project → GitHub**.
3. Elige el repositorio `bb-criminologa`.
4. Deja vacíos "Build command" y "Publish directory" (o pon `/`). Clic en **Deploy**.
5. En un minuto tendrás una dirección tipo `https://bb-criminologa.netlify.app`.
6. Para usar un dominio propio (ej. `bbcriminologa.com`): **Domain settings → Add a domain** y sigue las instrucciones.

Cada vez que cambies un archivo en GitHub, Netlify actualiza el sitio solo.

**Alternativa: GitHub Pages.** En el repositorio: **Settings → Pages → Branch: main → Save**. Hasta donde sé, GitHub Pages gratis solo funciona con repositorios **públicos** (en privados requiere plan de pago), y en un repositorio público cualquiera puede ver el código, incluida la solución del caso. Por eso recomiendo Netlify.

## Nota de seguridad (importante)

Este sitio es estático: el código de acceso y la solución están dentro del archivo del juego. Alguien con conocimientos técnicos podría verlos con "ver código fuente". Para un primer lanzamiento está bien (la mayoría de la gente no lo hará), pero para proteger mejor el producto, el siguiente paso sería:

- Códigos únicos por compra (por ejemplo con Lemon Squeezy o una automatización con Stripe), y
- Validar el código y entregar la solución desde un servidor (por ejemplo, funciones de Netlify).

## Probarlo en tu computadora

Haz doble clic en `index.html` para ver la landing. Para el juego, abre `caso/la-ultima-navidad/index.html` y entra con el código `CRIMI-001`.

## Pendientes antes de lanzar

- Grabar el video de bienvenida definitivo de Dafne y reemplazar `bienvenida.mp4` (mismo nombre).
- Reemplazar las descripciones de las fotos del caso por fotos producidas.
- Que Dafne revise el caso completo y la edad recomendada de la landing.
- Confirmar precio final (la landing dice $199 MXN).

Todos los personajes y hechos del caso son ficticios.
