# cierto — prototipo de plataforma de sorteos (demo para revisión)

Sitio estático (un solo `index.html`, sin dependencias ni servidor). Todo es ficticio:
sin pagos reales, sin premios, y los datos se guardan solo en el navegador de quien lo prueba.

## Qué muestra
- **Varios sorteos en curso a la vez** (SUV, moto, smartphone + notebook, dinero) y un sorteo anterior ya finalizado.
  Cada uno tiene su propio stock, precio, meta mínima, fecha y verificación.
- Portada con sorteo destacado, listado con orden (más próximos, menor precio, más vendidos) y etiquetas
  ("Últimos tickets", "Sorteo asegurado", "Agotado", "Finalizado").
- Compra: packs con descuento, números al azar o elegidos, reserva de 10 minutos, pago simulado.
- Ticket con comprobante SHA-256, recuperación por RUT o correo (de todos los sorteos).
- **Verificador de sorteo** por sorteo: recalcula el resultado en el navegador (funciona de verdad).
- **Panel interno** (menú "Modo demo"): resumen de todos los sorteos, **crear un sorteo nuevo** (aparece al instante
  en el sitio público), consola de sorteo (al sortear, el sorteo pasa a "Finalizado"), soporte y auditoría.
- **Revisión legal**: flujo propuesto y preguntas para el abogado (imprimible en PDF).

## Ticket y correo
- Cada número se muestra como un ticket con fondo, la ilustración del premio, número grande, línea de corte y código.
- En la pantalla de confirmación, "Ver correo enviado" muestra el correo de confirmación (compatible con Outlook).
  Desde ahí se puede **copiar el correo** (para pegarlo en un mensaje nuevo) o **descargar un .eml** (en Outlook se abre como borrador).
- Este prototipo **no envía correos reales**: es un sitio estático. El envío real (por ejemplo con Amazon SES) va en la fase de backend.

## Consejos para la demostración
- Menú "Modo demo" → "Reiniciar datos de demo" deja todo como al inicio (borra compras, sorteos creados y sorteos ejecutados).
- Para ver el ciclo completo: compra un ticket, entra al panel, crea un sorteo, sortéalo y comprueba el resultado en "Verificar sorteo".

## Publicar en GitHub Pages
1. Crea un repositorio nuevo en GitHub (si es público, cualquiera con el enlace lo verá).
2. Sube `index.html` y este `README.md` a la rama `main`.
3. En el repositorio: Settings → Pages → Source: "Deploy from a branch" → rama `main`, carpeta `/ (root)`.
4. En un par de minutos queda en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

Para probarlo localmente basta con abrir `index.html` en el navegador.
