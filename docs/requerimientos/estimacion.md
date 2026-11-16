# ESTIMACIÓN DE ESFUERZO Y TAMAÑO (AG-C071)

La estimación se realizó mediante la técnica de *Planning Poker* (juicio de expertos) sobre las historias de usuario, contrastada con un conteo rápido de Puntos de Caso de Uso (UCP).

| Módulo | Casos de Uso Principales | Complejidad | Story Points (SP) | Horas Estimadas |
| :--- | :--- | :--- | :--- | :--- |
| M1. Catálogo y disponibilidad | Consultar catálogo, verificar disponibilidad, filtrar | Alta (lógica de solapamiento de fechas) | 21 | 60 |
| M2. Cotizador y reservas | Cotizar, convertir a reserva, generar QR, registrar pago | Alta | 34 | 100 |
| M3. Panel administrativo | CRUD equipos/paquetes, gestionar reservas, RBAC | Alta | 34 | 100 |
| M4. Auth y fidelización | Login Gmail, verificar celular, puntos | Media | 13 | 40 |
| M5. Asistente IA | Configurar evento, recomendar equipos | Alta (integración API externa) | 21 | 60 |
| Transversal | Seguridad, pruebas, CI/CD, documentación | Alta | 30 | 90 |
| **TOTAL** | | | **153 SP** | **450 h** |

**Nota de viabilidad:** Con 4 integrantes y una dedicación estimada de ~10 horas semanales por integrante durante las 18 semanas efectivas del ciclo, se dispone de un total de ~720 horas. Por lo tanto, el alcance propuesto (MVP + Should) es técnicamente viable y realista.
