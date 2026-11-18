# Dosis en radiología pediátrica

Página web estática para consultar, desde el móvil (vía QR), la dosis efectiva media estimada de las exploraciones pediátricas más frecuentes, con sus recomendaciones de «no hacer» y los NRD europeos de referencia.

## Contenido

- `index.html`: el buscador (exploración + edad → dosis, equivalencia BERT, «no hacer», NRD RP 185).
- `comparativa.html` e `img/`: gráficos comparativos con series europeas.

## Publicar en GitHub Pages

1. Cree un repositorio público (por ejemplo, `rx-pediatria`).
2. **Add file → Upload files**: suba `index.html`, `comparativa.html`, `README.md` y la carpeta `img`.
3. **Settings → Pages** → *Deploy from a branch* → rama `main`, carpeta `/ (root)` → **Save**.
4. En uno o dos minutos estará en `https://<usuario>.github.io/rx-pediatria/`.

## Editar los datos

Todo está en el bloque `DATOS` al principio del script de `index.html`:

- `EXPLORACIONES`: dosis efectiva media (mSv) por grupo de edad (`dosis`) o valor pediátrico único (`unica`), qué recomendaciones de «no hacer» mostrar (`nh`) y qué tabla de NRD (`nrd`).
- `NO_HACER`: texto resumido y fuente de cada recomendación.
- `NRD`: tablas de la RP 185.
- `FONDO_NATURAL`: referencia para BERT (3,0 mSv/año, UNSCEAR 2024).
- `REVISION`: fecha que aparece al pie.

Al guardar los cambios (**Commit changes**), la página se actualiza sola en uno o dos minutos. La dirección no cambia, así que el QR sigue siendo válido.

## Enlaces directos para QR

`?e=<exploración>&r=<grupo de edad>`, ambos empezando en 0. Por ejemplo, `?e=7&r=1` abre TC de cráneo, 1–5 años.

## Fuentes

- Documento de base con datos DOPOES (tablas 1–3) y su revisión técnica (BERT con 3,0 mSv/año).
- SERAM. Recomendaciones de «no hacer», 2014; Ministerio de Sanidad, Compromiso por la Calidad (SERAM y AEP).
- Comisión Europea. Radiation Protection 185, tablas 10.2a–b.
