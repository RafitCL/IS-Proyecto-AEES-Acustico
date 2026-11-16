# ESPECIFICACIÓN DE REQUERIMIENTOS DE SOFTWARE (ISO/IEC/IEEE 29148)

## 1. Requerimientos Funcionales (RF)
| ID | Módulo | Requerimiento | Prioridad | Criterio de verificación |
| :--- | :--- | :--- | :--- | :--- |
| RF-01 | M1 | Listar los equipos del catálogo con categoría, descripción, precio y fotos. | Must | El catálogo muestra el 100% de equipos activos en BD. |
| RF-02 | M1 | Mostrar la disponibilidad de cada equipo para un rango de fechas. | Must | Con 2 reservas que cubren el stock, el sistema muestra 0 disponibles. |
| RF-03 | M1 | Impedir que un equipo sea reservado en fechas superpuestas por encima del stock. | Must | Prueba de concurrencia: solo se acepta una reserva si queda 1 equipo. |
| RF-06 | M2 | Generar una cotización con detalle, subtotal y días de alquiler. | Must | La cotización coincide con el cálculo manual en pruebas. |
| RF-12 | M2 | Calcular el adelanto exigido según el porcentaje configurado. | Must | Con 30% sobre S/ 1000, el adelanto mostrado es S/ 300. |
| RF-13 | M2 | Generar un QR de pago Yape/Plin por el monto del adelanto. | Must | El QR contiene el monto y el identificador de reserva correctos. |
| RF-14 | M2 | Registrar el pago del adelanto y cambiar la reserva a "confirmada". | Must | Tras registrar pago, el estado cambia y se guarda la fecha. |
| RF-24 | M3 | Permitir el CRUD de equipos, paquetes y precios en el panel. | Must | Las 4 operaciones se ejecutan y reflejan en el catálogo. |
| RF-25 | M3 | Permitir gestionar reservas (consultar, confirmar, cancelar). | Must | Cada cambio de estado queda registrado con usuario y fecha. |
| RF-28 | M3 | Aplicar control de acceso basado en roles (RBAC). | Must | Un operador recibe error 403 al intentar acceder a configuración. |
| RF-16 | M4 | Autenticar clientes con Google (Gmail) y verificar celular. | Should | Usuario con Gmail válido accede al área de fidelización. |
| RF-19 | M5 | Asistente IA que recomienda equipos según el tipo de evento. | Should | La recomendación incluye ítems existentes en catálogo. |

## 2. Requerimientos No Funcionales (RNF - ISO 25010)
| ID | Categoría | Requerimiento | Métrica / Umbral |
| :--- | :--- | :--- | :--- |
| RNF-01 | Eficiencia | El catálogo debe cargar rápido en red móvil. | p95 ≤ 2.5s en 3G; ≤ 1s en laboratorio. |
| RNF-05 | Seguridad | Mitigar riesgos del OWASP Top 10. | 0 hallazgos críticos en revisión ZAP; validación en 100% de formularios. |
| RNF-07 | Legal | Tratamiento de datos según Ley N° 29733. | Consentimiento registrado; datos de demo anonimizados. |
| RNF-09 | Usabilidad | El flujo de cotización debe ser intuitivo. | ≥ 80% de usuarios completa el flujo sin ayuda. |
| RNF-12 | Mantenibilidad | Código con estándares de calidad. | ESLint sin errores; cobertura de pruebas ≥ 70%. |
