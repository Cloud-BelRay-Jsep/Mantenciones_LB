# Despliegue MM SAG — Octubre 2026

## 1. Subir a GitHub Pages (carpeta nueva dentro del repo de Confluencia)
1. En el repo, crear la carpeta `sag/` y subir: `index.html`, `Panel_OT.html`, `Acreditaciones.html`, `registro.html`, `logo-belray.png`.
2. La URL quedará: `https://<usuario>.github.io/<repo>/sag/`
   - Panel general: `.../sag/index.html`
   - Panel OT: `.../sag/Panel_OT.html`
   - Acreditaciones: `.../sag/Acreditaciones.html`
   - Registro NFC: `.../sag/registro.html`

## 2. Autorizar el teléfono receptor (una vez por teléfono, sin incógnito)
`https://<usuario>.github.io/<repo>/sag/registro.html?setup=belray-sag-2026-q7m4`
Quitar autorización: `.../sag/registro.html?reset=1`
(La llave y el nombre de almacenamiento son distintos a los de Confluencia: un teléfono autorizado allá NO queda autorizado aquí.)

## 3. URL a grabar en cada llavero (sin tildes, `+` en vez de espacio)
- Entrada: `https://<usuario>.github.io/<repo>/sag/registro.html?nombre=Juan&apellido=Perez&tipo=entrada`
- Salida:  `https://<usuario>.github.io/<repo>/sag/registro.html?nombre=Juan&apellido=Perez&tipo=salida`

## 4. Apps Script del Sheet
- Proyecto del Sheet: pegar `ReporteTurno_v3.gs` + `IndexadorDocumentos.gs` (un solo `onOpen`, ya viene en v3). Recargar el Sheet → menú Bel-Ray.
- Web App NFC: `RegistroNFC_v3.gs` ya desplegado (EXEC_URL ya configurada).
