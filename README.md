# Galería de Imágenes Animada

Una galería de imágenes en columnas que se despliega con animaciones sincronizadas con el scroll, usando **solo CSS moderno**.

## Características

- Animación de entrada para cada imagen al aparecer en la vista
- Encabezado sticky que cambia de estilo al desplazarse
- Sin JavaScript, todo con CSS y `animation-timeline`

## Cómo funciona

La implementación utiliza animaciones CSS sincronizadas con el scroll:

1. Las **imágenes** se animan con `@keyframes reveal` y `animation-timeline: view()`
2. El **header sticky** se anima con `@keyframes enhance-header` y `animation-timeline: scroll(root)`

## Animaciones utilizadas

```css
/* Animación de imágenes */
animation: reveal linear both;
animation-timeline: view();

/* Animación del header */
animation: enhance-header linear both;
animation-timeline: scroll(root);
```

## Compatibilidad con Navegadores

Esta función requiere soporte para animaciones CSS scroll-timeline. Actualmente compatible con:

- Chrome (y navegadores basados en Chromium) con características experimentales habilitadas
- Firefox con flags habilitados

## Uso

¡Simplemente incluye el CSS en tu proyecto y agrega los elementos HTML de la galeria! No se necesita configuración de JavaScript.
