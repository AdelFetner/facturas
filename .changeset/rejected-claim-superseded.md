---
"facturas": patch
---

Una idempotencyKey rechazada ya no recupera el CAE de la venta que tomó su número cuando el store tiene `withLock`: la siguiente clave la marca como reemplazada. Sin `withLock` el problema persiste y se corrige aparte