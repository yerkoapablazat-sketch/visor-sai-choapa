# Visor SAI Choapa

Visor geoespacial de la calidad de aguas superficiales, aguas subterráneas y sedimentos fluviales del **Programa de Seguimiento Ambiental Integral (SAI)** en la cuenca del río Choapa, Región de Coquimbo, Chile (2011–2026).

**Ver el visor:** https://yerkoapablazat-sketch.github.io/visor-sai-choapa/

## Qué muestra

- **Mapa** de las estaciones de monitoreo sobre el relieve y la red hidrográfica de la cuenca, con subcuencas, estaciones fluviométricas y capas del territorio (minería, agricultura, glaciares, humedales, cuerpos de agua y áreas protegidas).
- **Valor de cada parámetro por campaña**, comparado con:
  - **NCh 1333** (riego) y **NCh 409** (agua potable), para aguas, con excepciones por estación (por ejemplo, la RCA N° 38/2004 en CHO-03);
  - **Guía de Ontario** para calidad de sedimentos acuáticos, para sedimentos.
- **Ficha de estación:** serie histórica, glosario del parámetro, tendencia, caudal del mes de muestreo, balance iónico y aptitud para riego.
- **Tendencias 2011–2026:** Kendall estacional y pendiente de Sen, también ajustadas por caudal para separar el efecto de la sequía.
- **Aptitud del agua para riego:** clasificación Riverside (conductividad y RAS).
- **Caudal y sequía:** caudal anual comparado con 1991–2020 y condición hidrológica de cada campaña.
- **Perfil de cordillera a mar** y **huella de calidad** (estaciones × campañas).
- **Descarga de datos** en CSV, por estación o por campaña.
- Los valores bajo el límite de detección se muestran como tales (`< LD`), nunca como cero.

## Aviso

Versión de consulta. Los datos provienen de la base del programa y están sujetos a revisión; no reemplazan los informes técnicos oficiales de cada campaña. Las tendencias describen cambios en el tiempo; no identifican sus causas.

## Fuentes

| Dato | Fuente |
|---|---|
| Resultados de aguas y sedimentos | Base de datos del Programa SAI (campañas 2011–2026) |
| Caudales medios mensuales | Dirección General de Aguas (DGA) |
| Red hidrográfica | Dirección General de Aguas (DGA) |
| Subcuencas | DGA, Clasificación de cuencas hidrográficas de Chile (BNA) |
| Uso de la tierra | CONAF, Catastro de los Recursos Vegetacionales y Uso de la Tierra, Región de Coquimbo (2025) |
| Relieve | Copernicus GLO-30 DEM (ESA / Agencia Espacial Europea) |
| Localidades de referencia | © colaboradores de OpenStreetMap (ODbL) |
| Coordenadas de estaciones | Programa SAI (UTM 19S, EPSG:32719) |

## Instituciones

Programa de Seguimiento Ambiental Integral (SAI) · Instituto de Investigaciones Agropecuarias (INIA), Ministerio de Agricultura · Junta de Vigilancia del Río Choapa y sus Afluentes.

## Cómo se actualiza

El visor es un solo archivo (`index.html`) sin servidor. Se genera con los scripts de la plataforma (`Plataforma_Geoespacial/scripts`, pasos 01 → 02 → 02b → 05b → 06 → 03) a partir de la base de cada campaña y de los caudales de la DGA. Para publicar una nueva versión: reemplazar `index.html`, hacer commit y push.

## Tecnología

HTML, CSS y JavaScript sin compilación; mapa con [Leaflet](https://leafletjs.com/) 1.9.4 (BSD-2) cargado desde cdnjs; tipografía IBM Plex (Google Fonts, OFL).
