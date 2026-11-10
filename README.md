# Panel de clientes · alirio.motion

Control de videos por cliente, saldo y factura en PDF. Un solo archivo (`index.html`), sin servidor.

## Uso
- **En tu PC:** abrí `index.html`. Si `data.js` está en la misma carpeta, carga tus datos solo.
- **En GitHub Pages:** la primera vez tocá *Restaurar copia* con tu `.json`, o *Importar Excel* dentro de cada cliente.
- Todo lo que edites se guarda en el navegador. Usá *Copia de seguridad (.json)* para no perderlo.
- *Generar factura* → elegís período → *Descargar PDF*.

`data.js` tiene montos y datos bancarios: está en `.gitignore` y no se sube.

## Clientes
- **Marliseth Ochoa · Our North by 8A** — estética marino / cian / oro.
- **50+1 New York** — trabajo de Times Square / MSG, estética morado / lila del logo 50+1.

Si ya habías usado la web, al abrirla separa sola los ítems de Times Square de Marliseth y los pasa a 50+1.

## Espacio y copias
- Si lo guardado pasa del 80 % de los ~5 MiB que da el navegador, o si un guardado falla por falta de espacio, aparece un aviso arriba del hub (usa `navigator.storage.estimate()` y el tamaño real de `localStorage`).
- La copia `.json` se baja siempre como archivo (Blob), así que funciona en Firefox, Safari y iPhone; no se usa `showSaveFilePicker`.
- Las tablas muestran 300 filas por vez (botón «Mostrar más»): un Excel de 5.000 filas ya no congela la página.
- La factura tiene campos opcionales «Factura E N.º» y «CAE»: si se llenan, el PDF dice que es el detalle de esa factura.
