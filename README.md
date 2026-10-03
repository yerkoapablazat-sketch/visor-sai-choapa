# Visor SAI Choapa

Visor geoespacial de la calidad de aguas superficiales, aguas subterráneas y sedimentos fluviales del **Programa de Seguimiento Ambiental Integral (SAI)** en la cuenca del río Choapa, Región de Coquimbo, Chile (2011–2026).

**Ver el visor:** `https://<usuario>.github.io/visor-sai-choapa/` *(se activa al publicar con GitHub Pages)*

## Qué muestra

- Mapa de las estaciones de monitoreo sobre la red hidrográfica de la cuenca.
- Valor de cada parámetro por campaña, comparado con:
  - **NCh 1333** (requisitos de calidad del agua para riego) y **NCh 409** (agua potable), para aguas;
  - **Guía de Ontario** para calidad de sedimentos acuáticos, para sedimentos.
- Serie histórica por estación, perfil de cordillera a mar y **huella de calidad** (estaciones × campañas).
- Contexto territorial: subcuencas BNA y relieve sombreado.
- Los valores bajo el límite de detección se muestran como tales (`< LD`), nunca como cero.

## Aviso

Versión de consulta. Los datos provienen de la base del programa y están sujetos a revisión; no reemplazan los informes técnicos oficiales de cada campaña.

## Fuentes

| Dato | Fuente |
|---|---|
| Resultados de aguas y sedimentos | Base de datos del Programa SAI (campañas 2011–2026) |
| Red hidrográfica | Dirección General de Aguas (DGA) |
| Localidades de referencia | © colaboradores de OpenStreetMap (ODbL) |
| Subcuencas | DGA, Clasificación de cuencas hidrográficas de Chile (BNA) |
| Relieve | Copernicus GLO-30 DEM (ESA / Agencia Espacial Europea) |
| Coordenadas de estaciones | Programa SAI (UTM 19S, EPSG:32719) |

## Cómo se actualiza

El visor es un solo archivo (`index.html`) sin servidor. Se genera con los scripts de la plataforma (`Plataforma_Geoespacial/scripts`, pasos 01 → 02 → 02b → 03) a partir de la base de cada campaña. Para publicar una nueva versión: reemplazar `index.html`, hacer commit y push.

## Tecnología

HTML, CSS y JavaScript sin compilación; mapa con [Leaflet](https://leafletjs.com/) 1.9.4 (BSD-2) cargado desde cdnjs; tipografía IBM Plex (Google Fonts, OFL).
