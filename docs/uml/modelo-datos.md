# MODELO DE DATOS (DIAGRAMA ENTIDAD-RELACIÓN)

A continuación se presenta el modelo de datos relacional diseñado para AeeS Acústico:

```mermaid
erDiagram
    CLIENTE ||--o{ RESERVA : realiza
    CLIENTE ||--o{ PUNTO : acumula
    RESERVA ||--|{ DETALLE_RESERVA : contiene
    EQUIPO ||--o{ DETALLE_RESERVA : es_alquilado
    RESERVA ||--o{ PAGO : genera
    PAQUETE ||--o{ DETALLE_PAQUETE : contiene
    EQUIPO ||--o{ DETALLE_PAQUETE : pertenece

    CLIENTE {
        int id_cliente PK
        string nombre
        string gmail
        string celular
        int puntos_totales
    }
    EQUIPO {
        int id_equipo PK
        string nombre
        string categoria
        float precio_dia
        int stock_total
    }
    RESERVA {
        int id_reserva PK
        int id_cliente FK
        date fecha_evento
        string estado
        float total
        float adelanto
    }
    DETALLE_RESERVA {
        int id_detalle PK
        int id_reserva FK
        int id_equipo FK
        int cantidad
        float subtotal
    }
    PAGO {
        int id_pago PK
        int id_reserva FK
        string metodo
        float monto
        datetime fecha_pago
    }
