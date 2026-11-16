# ACTA DE CONSTITUCIÓN DEL PROYECTO (PROJECT CHARTER)

## 1. Información general
* **Nombre del proyecto:** Sistema de Información Web para la Gestión de Alquiler de Equipos Audiovisuales — AeeS Acústico
* **Asignatura:** Ingeniería de Software (SIS021) — Semestre 2026-II
* **Organización beneficiaria:** AeeS Acústico (MYPE, Urb. Larapa Grande, San Jerónimo, Cusco)
* **Metodología:** Scrum (Guía Scrum 2020)

## 2. Problemática Organizacional
AeeS Acústico gestiona actualmente sus cotizaciones, disponibilidad de equipos y reservas mediante comunicación por WhatsApp, llamadas telefónicas y registros manuales. Esta forma de trabajo genera: 
1. Cotizaciones lentas y heterogéneas.
2. Riesgo de sobreventa de equipos al no existir control de disponibilidad por fecha.
3. Pérdida de trazabilidad de los adelantos cobrados por Yape/Plin.
4. Ausencia de un registro de clientes recurrentes.

## 3. Objetivos
**Objetivo general:** Desarrollar un sistema de información web para AeeS Acústico que automatice el catálogo, la cotización, la verificación de disponibilidad, la reserva con adelanto y la gestión administrativa.
**Objetivos específicos:**
1. Centralizar el catálogo de equipos y precios con disponibilidad por fecha.
2. Reducir el tiempo de elaboración de una cotización a menos de 2 minutos.
3. Permitir al cliente reservar en línea con adelanto mediante Yape o Plin.
4. Dotar al negocio de un panel administrativo con roles.
5. Fidelizar al cliente recurrente mediante autenticación con Gmail + celular.

## 4. Alcance del sistema (MVP)
| Módulo | Descripción | Prioridad |
| :--- | :--- | :--- |
| M1. Catálogo y disponibilidad | Catálogo real de equipos/paquetes con verificación de disponibilidad. | Must (MVP) |
| M2. Cotizador y reservas | Cotización en línea, carrito de evento y reserva con adelanto Yape/Plin. | Must (MVP) |
| M3. Panel administrativo | Gestión de equipos, paquetes, precios, reservas, pagos y clientes. | Must (MVP) |

## 5. Vinculación con los ODS
**ODS 12 — Producción y consumo responsables:** El modelo de alquiler alarga la vida útil de los equipos audiovisuales y evita compras innecesarias. 
**ODS 8 — Trabajo decente y crecimiento económico:** La digitalización formaliza las operaciones de una MYPE cusqueña.
**Métricas de impacto:**
* Digitalización de reservas: Reservas web / reservas totales (Meta: ≥ 70%).
* Eficiencia en cotización: Minutos por cotización (Meta: ≤ 2 min).
* Sobreventa: Reservas con conflicto de equipo (Meta: 0).
