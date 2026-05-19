# DigiDocu La Portada

PWA para llenar e imprimir recetarios hospitalarios oficiales del Hospital Municipal La Portada.

## Funciones principales

- Recetario ambulatorio.
- Recetario internado.
- Recetario UTI / UCIN.
- Buscador de medicamentos desde `data/medicamentos.json`.
- Buscador de diagnosticos y autollenado CIE-10 desde `data/cartera_servicios.json`.
- Lista de servicios/especialidades.
- Vista previa imprimible.
- Instalacion como PWA en navegador compatible.

## Publicacion en GitHub Pages

Este proyecto puede publicarse como sitio estatico. Los archivos necesarios son:

```text
index.html
app.js
styles.css
manifest.webmanifest
sw.js
icons/
data/
README.md
```

No es necesario publicar los PDF de prueba, plantillas extraidas ni scripts locales.

## Uso

Abre la app publicada desde GitHub Pages, llena el formulario, revisa la vista previa y usa `Imprimir` o `Generar PDF`.

## Datos

Los datos cargados actualmente son:

- `data/medicamentos.json`
- `data/cartera_servicios.json`

No deben agregarse datos personales de pacientes al repositorio.

## Publicación sugerida

Repositorio nuevo: `digidocu`

URL esperada en GitHub Pages:

```text
https://marceoviedo1980.github.io/digidocu/
```

Cambios hechos para evitar conflictos con otras PWAs:

- `manifest.webmanifest` usa `id: /digidocu/`.
- `start_url` y `scope` quedaron relativos.
- `sw.js` usa caché propio con prefijo `digidocu-`.
- El service worker ya no borra cachés de otras apps del mismo dominio GitHub Pages.
- Versionado actualizado a `digidocu-20260519-01`.
