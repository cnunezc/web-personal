# César Núñez Cuevas

Sitio: [cesar-nunez-web-personal.vercel.app](https://cesar-nunez-web-personal.vercel.app/)

Sitio personal estático hecho con Astro. Páginas: inicio, experiencia y contacto.

```bash
npm install
npm run build
```

La salida queda en `dist/`. Vista previa: `npm run preview`.

## Publicaciones de LinkedIn

La portada muestra hasta tres publicaciones en «Lo último en LinkedIn». Salen del arreglo `linkedinPosts` en `src/data/linkedin.ts`, en ese orden. Cada valor es el URN de la publicación y se incrusta con un iframe a `https://www.linkedin.com/embed/feed/update/<urn>`.

Para agregar una publicación:

1. Abre la publicación en LinkedIn.
2. Copia el URN que aparece en la URL, después de `/feed/update/`. Tiene la forma `urn:li:activity:1234567890123456789` o `urn:li:share:1234567890123456789`.
3. Añádelo al arreglo:

```ts
export const linkedinPosts: string[] = [
  "urn:li:activity:1234567890123456789",
];
```

Si el arreglo está vacío, esa sección muestra solo el enlace «Ver mis publicaciones en LinkedIn».
