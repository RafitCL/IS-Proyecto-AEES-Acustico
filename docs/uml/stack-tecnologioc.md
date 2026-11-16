# PERTINENCIA TECNOLÓGICA Y LIMITACIONES (AG-C112)

## 1. Stack Seleccionado
| Capa | Tecnología | Justificación |
| :--- | :--- | :--- |
| Backend | Node.js + Express | Ecosistema unificado en JavaScript; ideal para aplicaciones I/O intensivas como reservas en tiempo real. |
| Base de Datos | PostgreSQL | Integridad referencial estricta necesaria para evitar sobreventa de equipos y manejar transacciones de pagos de forma segura. |
| Frontend | React | Creación de interfaces de usuario dinámicas (SPA) para el catálogo y el panel administrativo. |

## 2. Reconocimiento de Limitaciones (Criterio de Rúbrica)
*   **Escalabilidad:** Node.js opera en un solo hilo (single-thread). Si el tráfico de usuarios concurrentes en temporada alta (ej. fiestas patrias o fin de año) supera la capacidad de un solo núcleo, el servidor se bloqueará. *Mitigación:* Se implementará un balanceador de carga o clústeres de Node.js en el despliegue final.
*   **Mantenibilidad:** Al usar JavaScript (lenguaje de tipado dinámico), el riesgo de errores en tiempo de ejecución (como sumar un string a un número en el cálculo de precios) es alto. *Mitigación:* Se aplicará ESLint y se considerará la migración a TypeScript para la versión 2.0.
*   **Rendimiento:** Las consultas complejas de disponibilidad (verificar fechas cruzadas) en PostgreSQL pueden volverse lentas si la tabla de reservas crece demasiado. *Mitigación:* Se crearán índices compuestos en las columnas de fecha de inicio y fin.
