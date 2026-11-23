# Atlas del Madrid Profundo — actualización de inventario

## Archivos
- `index.html`: aplicación actualizada con filtro de cronología aproximada (columna Q), ficha de 35 atributos y edición.
- `yacimientos.geojson`: inventario combinado de 505 registros anteriores y los nuevos con coordenadas. **Es la opción recomendada para publicar en GitHub Pages**.
- `yacimientos_nuevos.geojson`: solo los nuevos registros, para usar «Importar GeoJSON» sin reemplazar el inventario.
- `excluidos.txt`: filas no importadas por falta de coordenadas utilizables.
- `campos_excel.json`: listado de las 35 columnas originales.

## Publicar para todos los navegadores
1. Haz copia de seguridad del GeoJSON publicado y exporta cualquier edición local pendiente.
2. En el repositorio GitHub `gismadrid/Atlas-Madrid-Profundo`, sube `index.html` y `yacimientos.geojson` a la raíz, sustituyendo los actuales.
3. Confirma el commit en `main` y espera a que Pages publique.
4. Abre el Atlas y recarga con Ctrl+F5.

## Solo importar los nuevos
En el Atlas abre «Yacimientos» → «Importar GeoJSON» → selecciona `yacimientos_nuevos.geojson`. Para hacerlos permanentes, exporta el inventario completo y publícalo como `yacimientos.geojson`.

## Cronología
El filtro se basa en la columna Q «Crono aprox.», no en la clasificación cultural. Los valores negativos representan años anteriores al presente, según la convención de tu Excel. Los registros sin valor siguen visibles por defecto, incluso con un filtro activo, salvo que desmarques «Incluir yacimientos sin cronología informada».

## Coordenadas
Se admiten DMS (grados/minutos/segundos), latitud/longitud decimal con prefijo «Baena» y formatos UTM como `Point (X Y)` o `X: ...; Y: ...`. Para las UTM se ha supuesto ETRS89 huso 30, pendiente de confirmación. Los registros «Pendiente» o vacíos no se han importado.

## Edición
Selecciona el yacimiento y pulsa «Editar». Despliega «Campos completos del inventario Excel» para modificar los 35 campos, incluida «Crono aprox.». Guarda, exporta GeoJSON y reemplaza el archivo publicado para compartir los cambios. Los 505 registros anteriores muestran los mismos 35 campos como «—» hasta que se documenten.

## Atención
La importación por ID no identifica automáticamente posibles duplicados de nombre entre el inventario anterior y el personal. Revisa coincidencias antes de fusionar registros. GitHub Pages no guarda automáticamente las modificaciones locales.
