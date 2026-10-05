# SAKUBA V2 — GitHub Pages

Versión estática de SAKUBA preparada para publicarse directamente en **GitHub Pages**.

## Estructura

```text
SAKUBA_V2_GitHubPages/
├── index.html
├── README.md
├── .nojekyll
├── css/
│   └── styles.css
├── js/
│   └── app.js
└── assets/
    ├── covers/
    └── images/
        └── favicon.svg
```

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub.
2. Sube **todo el contenido de esta carpeta** al repositorio.
3. En el repositorio entra a **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Elige la rama `main` y la carpeta `/ (root)`.
6. Guarda y espera a que GitHub Pages publique el sitio.

## Importante

Esta versión no utiliza Flask, Python, PHP ni una base de datos de servidor. Todo funciona en el navegador.

Los favoritos, historial y tamaño de fuente se guardan mediante `localStorage`, por lo que son datos locales del navegador de cada lector.

## Añadir una portada

En `js/app.js`, cada obra tiene:

```js
portada: "",
```

Puedes usar una imagen del propio repositorio, por ejemplo:

```js
portada: "assets/covers/mi-portada.jpg",
```

o una URL directa de una imagen.

## Añadir obras y capítulos

El catálogo está dentro de `js/app.js`, en `CATALOGO_NOVELAS`.

Cada obra contiene:

- `id`
- `portada`
- `titulo`
- `autor`
- `status`
- `estrellas`
- `generos`
- `sinopsis`
- `capitulos`

Los capítulos contienen:

- `numero`
- `titulo`
- `contenido`

## Nota sobre publicación

GitHub Pages sirve archivos estáticos. Por eso esta V2 está pensada para que el contenido editorial se administre desde archivos del repositorio, no desde un panel conectado a una base de datos.

