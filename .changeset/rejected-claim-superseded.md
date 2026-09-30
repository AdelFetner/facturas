---
"facturas": patch
---

Una idempotencyKey rechazada ya no recupera el CAE de otra venta que tomó su número. El rechazo queda guardado en la reserva, así que el reintento y `recover()` informan un conflicto si aparece un comprobante en ese número, con o sin `withLock`. Si el número sigue libre, el reintento lo vuelve a enviar. Actualizá todos los procesos que comparten un store: las versiones anteriores ignoran el rechazo guardado.
