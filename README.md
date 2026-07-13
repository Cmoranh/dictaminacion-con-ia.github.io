# Dictaminación con IA — Dashboard de Dictámenes Jurídicos

Panel de análisis y monitoreo de dictámenes jurídicos (Bancrea). Aplicación 100% del
lado del cliente: filtros múltiples, KPIs, gráficas (Chart.js) y tabla con búsqueda,
ordenamiento y detalle en modal. Permite cargar un CSV propio (botón "Cargar CSV" o
arrastrando el archivo sobre la página) y trae datos de ejemplo por defecto.

## Uso

- **En línea (GitHub Pages):** https://cmoranh.github.io/dictaminacion-con-ia.github.io/
- **Local:** abre `index.html` en el navegador, o sirve la carpeta:

  ```bash
  python3 -m http.server 8080
  # luego visita http://localhost:8080
  ```

## Datos

El dashboard espera un CSV con estas columnas (acepta alias y normaliza acentos/fechas):

`Caso`, `Ref Base`, `Fecha de Inicio`, `Fecha de Última Modificación`, `Nombre`, `RFC`,
`Proceso 72`, `Proceso 226`, `Proceso 222`, `Coordinador`, `Abogado`, `Ejecutivo`,
`Tipo Dictamen`, `Modo (Crear o Actualizar)`, `Estatus`, `Tipo Gestión`, `Pasó por IA`,
`Obs.`, `Comentarios Abogado`.

Los datos cargados se procesan solo en el navegador; no se envían a ningún servidor.

## Dependencias externas (CDN)

- [Chart.js 4.4.1](https://www.chartjs.org/) + plugin datalabels
- Google Fonts: Syne y DM Mono
