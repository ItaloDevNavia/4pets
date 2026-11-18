# 4Pets: rediseño de comercial4pets.cl (demo)

Tienda de mascotas en Ciudad de Los Valles, Pudahuel. Es una propuesta de rediseño de su tienda Jumpseller en un sitio estático (`index.html` + `productos.js`), sin build y listo para Vercel.

## Qué cambia frente a la web actual
- **Identidad:** la web actual usa verde y café, colores que no aparecen en su logo. Esta usa los colores del propio logo:
  - Naranja de "Pets".
  - Turquesa del borde.
  - Rosado de la lengua del beagle.
  - Crema de sus banners.

  La tipografía es redondeada (Fredoka), a juego con el logo de caricatura, y hay huellas, burbujas que se mueven y botones "de goma".
- **Portada:** el video de YouTube con carga negra se reemplaza por un mensaje claro ("Lo mejor para tu mejor amigo") y sus propias mascotas recortadas de los banners.
- **Menú:** el menú negro tenía unas 60 subcategorías, muchas vacías (juguetes, peces, ropa…). Ahora hay:
  - "¿Para quién compras?" con 4 tarjetas que muestran cuántos productos hay.
  - Chips de categoría que solo apuntan a lo que existe.
- **Buscador de alimento en 3 toques:** especie → edad → tamaño. Muestra solo lo que le sirve, ordenado por **precio por kilo** y marcando el más conveniente.
- **Búsqueda instantánea:** con fotos y precio, navegable con teclado, y "pregúntanos por WhatsApp" si no hay resultados.
- **Catálogo:**
  - Filtros combinables (mascota, tipo, marca) con contador.
  - Orden por precio o por precio por kilo.
  - Etiquetas de oferta y de línea veterinaria.
  - Ficha rápida con enlace al producto en la tienda actual.
- **Carro:**
  - Se queda guardado al recargar.
  - Barra de progreso hacia el **envío gratis sobre $50.000**.
  - Pedido armado por **WhatsApp**.
- **Móvil:** barra inferior (Inicio, Alimento, Buscar, Carro), filtros en hoja deslizable y botones grandes.

## Datos
**Reales** (comercial4pets.cl, leído el 17‑11‑2026):
- Los 59 productos con nombre, marca, precio, precio anterior, "desde", foto y enlace.
- Logo, banners y fotos de mascotas.
- Envío gratis sobre $50.000 y los medios de pago (Webpay, Mercado Pago, Khipu, transferencia).
- Dirección: Av. del Canal #20000, Ciudad de Los Valles, Pudahuel.
- Atención de lunes a domingo, 10:00 a 19:00.
- WhatsApp +56 9 3496 6535 y correo comercial4pets@gmail.com.
- La reseña de Catalina Pezo.
- Los textos "Tu tienda de mascotas de confianza…" y "¡Los protege hoy, los cuida siempre!".
- La lista de marcas del menú. Las que no tienen productos en la web aparecen en gris.

**Calculado o asignado por la demo:**
- El precio por kilo sale del peso que dice el nombre.
- La especie, la edad y el tamaño de cada alimento salen de su categoría en la tienda y de su nombre.
- La especie de los fármacos sale del nombre (`productos.js`).

**A decidir con el cliente:**
- **Pago:** el pedido sale por WhatsApp. Para cobrar en línea hay que conectar este diseño a Jumpseller, como tema o con su API, o seguir enlazando a la tienda actual (la ficha ya lo hace).
- **Stock:** la demo no lo maneja.
- **Catálogo:** se actualiza volviendo a leer la tienda y regenerando `productos.js`.

## Ver en local
```
python -m http.server 5201 -d 4pets
```
