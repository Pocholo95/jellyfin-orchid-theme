# 🌸 Orchid — tema para Jellyfin

Tema moderno y limpio para Jellyfin Web con acentos en degradado **morado → rosa**, superficies con efecto vidrio (glassmorphism), esquinas redondeadas y animaciones suaves.

Probado en **Jellyfin 12.1**.

## Paleta

| Token | Color | Uso |
|---|---|---|
| `--orchid-purple` | `#a855f7` | Acento principal |
| `--orchid-pink` | `#ec4899` | Acento secundario / hover |
| `--orchid-accent` | `#c084fc` | Enlaces y etiquetas |
| `--orchid-bg` | `#0d0a14` | Fondo |
| `--orchid-surface-solid` | `#1a1426` | Tarjetas, diálogos, inputs |

## Instalación

**Dashboard → General → Custom CSS code**

### Opción A: importar desde GitHub

Pega esta línea y guarda:

```css
@import url("https://cdn.jsdelivr.net/gh/Pocholo95/jellyfin-orchid-theme@v1.1.2/theme.css");
```

Para actualizar, cambia `v1.1.2` por la última versión de [Releases/Tags](https://github.com/Pocholo95/jellyfin-orchid-theme/tags).

> Evita `@main`: los navegadores guardan ese archivo en caché hasta 7 días, así que los cambios tardarían en verse en cada dispositivo.

### Opción B: pegar el CSS completo

Copia todo el contenido de [`theme.css`](theme.css), pégalo en el campo y guarda.

Después recarga el navegador con **Ctrl + F5**.

## Personalización

Puedes cambiar los colores sin tocar el tema. Añade esto **después** del `@import`:

```css
:root {
  --orchid-purple: #8b5cf6;
  --orchid-pink: #f472b6;
  --orchid-radius: 8px;
}
```

Todas las variables están al principio de `theme.css`, en la sección **Tokens**.

## Qué cambia

- Cabecera translúcida con desenfoque
- Pestañas tipo "pill" con degradado activo
- Tarjetas redondeadas que se elevan con un brillo al pasar el ratón
- Botones principales (Reproducir, Guardar…) con degradado y glow
- Barras de progreso, sliders del reproductor, checkboxes y switches con los colores del tema
- Diálogos, menús y toasts con el estilo del tema
- Hover uniforme en menús y listas: tinte suave + barra rosa a la izquierda
- Avatares redondos en el reparto y en el login
- Pantalla de login con tarjeta de vidrio
- Respeta `prefers-reduced-motion`

## Limitaciones

Jellyfin 12 no carga el *Custom CSS* en las páginas de administración (Dashboard, Metadata Manager…), para que un CSS roto nunca bloquee el panel. Esas páginas mantienen el tema oscuro por defecto.

## Licencia

MIT
